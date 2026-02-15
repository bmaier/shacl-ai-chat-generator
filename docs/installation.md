# Installations- & Setup-Guide: BSG Methode (PRODUKTION)

Dieser Guide führt Sie durch die manuelle Einrichtung der BSG-Methode in Ihrer BMAD-Umgebung.

---

## 1. Voraussetzungen (Prerequisites)

1.  **Node.js & npm:** Installiert (via nvm empfohlen).
2.  **Gemini CLI:** Installiert (`npm install -g @google/gemini-cli`).
3.  **BMAD Struktur:** Ein bestehendes Verzeichnis mit einem `_bmad/` Ordner.

---

## 2. Schritt-für-Schritt Installation

### Schritt A: Code kopieren
Kopieren Sie den gesamten Ordner `bsg` in das Verzeichnis `_bmad/` Ihres Zielprojekts.
Zielpfad: `{projekt-root}/_bmad/bsg/`

### Schritt B: Befehle registrieren (Wichtig!)
Damit die CLI die Befehle erkennt, müssen diese in die zentrale Hilfe-Datei eingetragen werden:

1. Öffnen Sie die Datei `_bmad/_config/bmad-help.csv` in Ihrem Hauptprojekt.
2. Kopieren Sie den Inhalt der Datei `_bmad/bsg/module-help.csv` (ohne die Kopfzeile).
3. Fügen Sie diese Zeilen am Ende der `_bmad/_config/bmad-help.csv` ein.
4. **Ergebnis:** Die Befehle wie `/bsg_configure_governance` sind nun nach einem CLI-Neustart verfügbar.

---

## 3. Infrastruktur-Setup (MCP Server)

Die BSG-Methode benötigt zwei MCP-Server für den vollen Funktionsumfang:

1.  **Installation:**
    ```bash
    npm install -g @modelcontextprotocol/server-markitdown @modelcontextprotocol/server-playwright
    ```
2.  **Registrierung:** Tragen Sie die Server in Ihre `config.json` der Gemini-CLI ein. Ohne diese Server können Dokumente (PDF) und Webseiten nicht analysiert werden.

---

## 4. Erster Start & Initialisierung

1. Starten Sie die CLI neu.
2. Führen Sie den Befehl `/bsg_configure_governance` aus.
3. Wählen Sie **[A] Auto-Init (BAMF Standard)**.
   *   Dies erstellt automatisch die `governance-config.yaml`.
   *   Es lädt die `schema.org` Ontologie physisch herunter.
   *   Es verifiziert alle Pfade.

---

## 5. Wartung & Erweiterung

*   **Updates:** Änderungen an Agenten oder Workflows werden sofort wirksam, da die CLI die Dateien zur Laufzeit liest.
*   **Neue Befehle:** Wenn Sie einen neuen Workflow hinzufügen, vergessen Sie nicht, ihn ebenfalls in der `_bmad/_config/bmad-help.csv` nachzutragen.
