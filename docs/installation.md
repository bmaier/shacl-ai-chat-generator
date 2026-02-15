# Installations- & Setup-Guide: BSG Methode (Full-Stack)

Dieser Guide führt Sie von einem leeren Verzeichnis bis zur ersten Modellierung. Er deckt sowohl die BMAD-Basis als auch das BSG-Spezialmodul ab.

---

## 1. Voraussetzungen (Prerequisites)

Stellen Sie sicher, dass folgende Software installiert ist:
1.  **Node.js (LTS):** [nodejs.org](https://nodejs.org)
2.  **Gemini CLI:** Global installieren via: `npm install -g @google/gemini-cli`

---

## 2. Schritt 1: BMAD Core initialisieren (Das Fundament)

1. Erstellen Sie einen neuen Projektordner: `mkdir mein-projekt && cd mein-projekt`
2. Erstellen Sie die Basis-Struktur: `mkdir -p _bmad/_config .gemini/commands`
3. Erstellen Sie die zentrale `_bmad/_config/bmad-help.csv` mit der Standard-Kopfzeile:
   ```csv
   module,phase,name,code,sequence,workflow-file,command,required,agent-name,agent-command,agent-display-name,agent-title,options,description,output-location,outputs
   ```

---

## 3. Schritt 2: BSG Modul via Git klonen

Navigieren Sie in den `_bmad` Ordner und klonen Sie das BSG-Modul:
```bash
cd _bmad
git clone https://github.com/ihr-organisation/bsg-module.git bsg
```

---

## 4. Schritt 3: Befehls-Registrierung (Kritisch!)

Damit die Gemini-CLI die Befehle erkennt, sind zwei Registrierungsschritte notwendig:

### A. Hilfe-System (CSV)
Fügen Sie die BSG-Befehle der zentralen Liste hinzu:
```bash
tail -n +2 _bmad/bsg/module-help.csv >> _bmad/_config/bmad-help.csv
```

### B. Slash-Commands (TOML)
Die CLI führt Befehle nur aus, wenn sie im Ordner `.gemini/commands/` registriert sind. Kopieren Sie die bereitgestellten Registrierungsdateien:
```bash
# Kopieren Sie alle TOML-Dateien aus dem Modul in Ihr Systemverzeichnis
cp _bmad/bsg/data/system/commands/*.toml .gemini/commands/
```
*(Falls Sie das Modul frisch klonen, finden Sie Muster-TOMLs im Ordner `docs/templates/` oder erstellen diese gemäß der Dokumentation).*

---

## 5. Schritt 4: KI-Werkzeuge (MCP Server) einrichten

Installieren Sie die benötigten Schnittstellen:
```bash
npm install -g @modelcontextprotocol/server-markitdown @modelcontextprotocol/server-playwright
```
*Registrieren Sie diese Server in Ihrer Gemini-CLI `config.json`.*

---

## 6. Schritt 5: Erster Start & Initialisierung

1. Starten Sie die CLI neu.
2. Führen Sie `/bsg_configure_governance` aus.
3. Wählen Sie **[A] Auto-Init**, um die BAMF-Infrastruktur physisch zu initialisieren.
