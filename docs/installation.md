# Installations- & Setup-Guide: BSG Methode (KORRIGIERT)

Dieser Guide führt Sie durch die manuelle Einrichtung der BSG-Methode in einer bestehenden BMAD-Umgebung.

---

## 1. Voraussetzungen (Prerequisites)

1.  **Node.js & npm:** Installiert (via nvm empfohlen).
2.  **Gemini CLI:** Installiert (`npm install -g @google/gemini-cli`).
3.  **Projekt-Struktur:** Ein bestehendes Verzeichnis mit einem `_bmad/` Ordner.

---

## 2. Manuelle "Installation" des BSG-Moduls

Da BSG ein lokales Modul ist, erfolgt die Einbindung manuell:

1.  **Code kopieren:**
    Kopieren Sie den gesamten Ordner `bsg` in das Verzeichnis `_bmad/` Ihres Zielprojekts.
    Pfad: `{projekt-root}/_bmad/bsg/`

2.  **Befehle registrieren (CLI Neustart):**
    Die Gemini-CLI scannt beim Start den `_bmad/` Ordner. Da im BSG-Ordner eine `module-help.csv` liegt, werden die Befehle (wie `/bsg_configure_governance`) automatisch geladen.
    *Tipp: Starten Sie die CLI im Projekt-Root neu.*

3.  **Manuelle Registrierung (Falls Befehle nicht erscheinen):**
    Sollten die Befehle nicht automatisch erscheinen, öffnen Sie die Datei `_bmad/_config/bmad-help.csv` im Hauptprojekt und fügen Sie den Inhalt der `_bmad/bsg/module-help.csv` am Ende hinzu.

---

## 3. MCP-Server einrichten (Zwingend für PDF/Web)

Die KI benötigt "Sinne", um Dokumente zu lesen.

1.  **Installieren:**
    ```bash
    npm install -g @modelcontextprotocol/server-markitdown @modelcontextprotocol/server-playwright
    ```
2.  **In der CLI registrieren:**
    Stellen Sie sicher, dass Ihre `config.json` der Gemini-CLI diese Server kennt. Fragen Sie die CLI im Zweifel: *"Wie registriere ich einen MCP Server?"*

---

## 4. Erster Start

1. Öffnen Sie die CLI im Projektverzeichnis.
2. Geben Sie `/bsg_configure_governance` ein.
3. Wählen Sie **[A] Auto-Init**, um die BAMF-Pfade und Ontologien (schema.org) initial zu laden.
