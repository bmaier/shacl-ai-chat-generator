# Installations- & Setup-Guide: BSG Methode (Full-Stack)

Dieser Guide führt Sie von einem leeren Verzeichnis bis zur ersten Modellierung. Er deckt sowohl die BMAD-Basis als auch das BSG-Spezialmodul ab.

---

## 1. Voraussetzungen (Prerequisites)

Stellen Sie sicher, dass folgende Software installiert ist:
1.  **Node.js (LTS):** [nodejs.org](https://nodejs.org)
2.  **Gemini CLI:** Global installieren via:
    ```bash
    npm install -g @google/gemini-cli
    ```

---

## 2. Schritt 1: BMAD Core initialisieren (Das Fundament)

Bevor Sie ein Modul nutzen können, benötigen Sie die BMAD-Ordnerstruktur.

1. Erstellen Sie einen neuen Projektordner:
   ```bash
   mkdir mein-semantik-projekt && cd mein-semantik-projekt
   ```
2. Erstellen Sie die Basis-Struktur für BMAD:
   ```bash
   mkdir -p _bmad/_config
   ```
3. Erstellen Sie die zentrale Befehls-Datei `_bmad/_config/bmad-help.csv` mit dieser Kopfzeile:
   ```bash
   echo "module,phase,name,code,sequence,workflow-file,command,required,agent-name,agent-command,agent-display-name,agent-title,options,description,output-location,outputs" > _bmad/_config/bmad-help.csv
   ```

---

## 3. Schritt 2: BSG Modul via Git klonen

Navigieren Sie in den `_bmad` Ordner und klonen Sie das BSG-Modul:

```bash
cd _bmad
git clone https://github.com/ihr-organisation/bsg-module.git bsg
```
*Nach diesem Schritt existiert der Ordner `_bmad/bsg/` und darin finden Sie auch die Datei `module-help.csv`.*

---

## 4. Schritt 3: Befehle im System registrieren

Damit die Gemini-CLI weiß, welche Befehle das BSG-Modul bietet, müssen wir die Modul-Befehle in die zentrale Datei (aus Schritt 2.3) kopieren:

1.  Wechseln Sie zurück in den Projekt-Root.
2.  Fügen Sie die BSG-Befehle der zentralen Liste hinzu:
    ```bash
    # Kopiert alle Zeilen aus der Modul-Hilfe (außer Kopfzeile) in die zentrale Hilfe
    tail -n +2 _bmad/bsg/module-help.csv >> _bmad/_config/bmad-help.csv
    ```

---

## 5. Schritt 4: KI-Werkzeuge (MCP Server) einrichten

BSG benötigt "Augen" zum Lesen von Dokumenten. Installieren Sie diese Server:

```bash
npm install -g @modelcontextprotocol/server-markitdown @modelcontextprotocol/server-playwright
```
*Wichtig: Registrieren Sie diese Server in Ihrer Gemini-CLI Konfiguration (`config.json`).*

---

## 6. Schritt 5: Erster Start & Initialisierung

1.  Starten Sie die Gemini-CLI im Hauptverzeichnis Ihres Projekts.
2.  Geben Sie den Befehl ein:
    ```bash
    /bsg_configure_governance
    ```
3.  Wählen Sie **[A] Auto-Init**. Master Lex wird nun die lokale Governance-Datei erstellen und schema.org physisch herunterladen.

---

## 7. Zusammenfassung der Verzeichnisstruktur
So sollte Ihr Projekt nach der Installation aussehen:
```
mein-semantik-projekt/
├── _bmad/
│   ├── _config/
│   │   └── bmad-help.csv    <-- Die zentrale Befehlsliste (gemergt)
│   └── bsg/                 <-- Das geklonte Modul
│       ├── module.yaml
│       ├── module-help.csv  <-- Die Quelle für die Registrierung
│       ├── agents/
│       └── workflows/
```
