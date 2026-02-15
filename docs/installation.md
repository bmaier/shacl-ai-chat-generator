# Installations- & Setup-Guide: BSG Methode

Dieser Guide führt Sie durch die vollständige Einrichtung der BSG-Methode (BAMF Semantic SHACL Generator), angefangen bei den System-Vorbedingungen bis hin zum ersten Start.

---

## 1. System-Vorbedingungen (Prerequisites)

Die BSG-Methode basiert auf dem BMAD-Framework und benötigt eine moderne Node.js Umgebung.

### 1.1 Node.js & npm (via nvm)
Wir empfehlen die Nutzung von **nvm** (Node Version Manager), um Versionskonflikte zu vermeiden.
1. **nvm installieren:** Folgen Sie den Anweisungen auf [nvm.sh](https://nvm.sh).
2. **Node.js installieren:**
   ```bash
   nvm install --lts
   nvm use --lts
   ```
3. **Prüfen:** `node -v` und `npm -v` sollten nun funktionieren.

### 1.2 KI-Interfaces (CLI)
Die Methode kann über verschiedene KI-CLIs gesteuert werden. Installieren Sie mindestens eine der folgenden:
*   **Gemini CLI:** `npm install -g @google/gemini-cli`
*   **Claude Code:** `npm install -g @anthropic-ai/claude-code`

---

## 2. BMAD Framework Setup

BSG ist ein Modul innerhalb des BMAD-Ökosystems.
1. Erstellen Sie ein neues Projektverzeichnis oder nutzen Sie ein bestehendes.
2. Initialisieren Sie BMAD (falls noch nicht geschehen):
   ```bash
   # Folgen Sie den Anweisungen des BMAD-Installers
   npx @bmad/installer
   ```

---

## 3. BSG Modul Installation (via Git)

1. Navigieren Sie in Ihren Projektordner zu `_bmad/`.
2. Klonen Sie das BSG-Repository:
   ```bash
   git clone https://github.com/ihr-organisation/bsg-module.git bsg
   ```
3. Registrieren Sie das Modul lokal:
   ```bash
   bmad install bsg --local ./bsg
   ```

---

## 4. MCP-Server Konfiguration (Kritisch!)

Die BSG-Methode benötigt spezifische Werkzeuge (Model Context Protocol), um Dokumente zu lesen und Webseiten zu scannen.

### 4.1 Markitdown (PDF/Office Analyse)
Installieren Sie den Markitdown-Server, damit Modeler Mia Dokumente lesen kann:
```bash
npm install -g @modelcontextprotocol/server-markitdown
```

### 4.2 Playwright (Web-Analyse)
Installieren Sie Playwright für die Analyse von Webformularen:
```bash
npm install -g @modelcontextprotocol/server-playwright
```

Stellen Sie sicher, dass beide Server in Ihrer `config.json` (Gemini/Claude) registriert sind.

---

## 5. Erster Start & Verifikation

Starten Sie Ihre CLI (Gemini oder Claude) im Projektverzeichnis.

1. **Infrastruktur prüfen:**
   Führen Sie den Befehl `/bsg_configure_governance` aus. Master Lex wird automatisch prüfen, ob die MCP-Server erreichbar sind.
2. **Governance initialisieren:**
   Wählen Sie im Dialog **[A] Auto-Init**, um die BAMF-Standardkonfiguration zu laden.

---

## 6. Fehlerbehebung (Troubleshooting)

*   **Befehl nicht gefunden:** Stellen Sie sicher, dass das Modul in der `_bmad/bsg/module-help.csv` korrekt registriert ist.
*   **MCP-Fehler:** Prüfen Sie mit `mcp-list` (falls vorhanden), ob die Server aktiv sind.
*   **Berechtigungen:** Stellen Sie sicher, dass die CLI Schreibrechte im Ordner `_bmad/bsg/data/` hat.
