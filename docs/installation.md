# Installations- & Setup-Guide: BSG Methode (GIT-RELEASE)

Dieser Guide führt Sie durch die vollständige Einrichtung der BSG-Methode (BAMF Semantic SHACL Generator) – von der Framework-Installation bis zum Modul-Klon.

---

## 1. Voraussetzungen (Prerequisites)

Stellen Sie sicher, dass folgende Komponenten auf Ihrem System installiert sind:
1.  **Node.js & npm:** [Download von nodejs.org](https://nodejs.org) (LTS empfohlen).
2.  **Gemini CLI:** Installieren via:
    ```bash
    npm install -g @google/gemini-cli
    ```

---

## 2. Schritt 1: BMAD Framework initialisieren

Falls Sie noch kein BMAD-Projekt haben, erstellen Sie ein neues Verzeichnis und initialisieren Sie die Struktur:

```bash
mkdir mein-semantik-projekt
cd mein-mein-semantik-projekt
# Initialisieren Sie die BMAD-Struktur manuell oder durch Kopieren der Basis-Konfiguration
mkdir _bmad
mkdir _bmad/_config
```

---

## 3. Schritt 2: BSG Modul via Git klonen

Navigieren Sie in Ihren `_bmad` Ordner und klonen Sie das Modul direkt aus dem Repository:

```bash
cd _bmad
git clone https://github.com/ihr-organisation/bsg-module.git bsg
```
*Hinweis: Der Ordner muss zwingend `bsg` heißen, damit die Pfade in den Workflows korrekt aufgelöst werden.*

---

## 4. Schritt 3: Befehle registrieren

Damit die Gemini-CLI die neuen Befehle erkennt, müssen diese manuell in die zentrale Hilfe-Datei gemergt werden:

1.  Öffnen Sie die Datei `{projekt-root}/_bmad/_config/bmad-help.csv`. (Falls nicht vorhanden, erstellen Sie diese mit der Standard-Kopfzeile).
2.  Kopieren Sie alle Zeilen aus `_bmad/bsg/module-help.csv` (außer der Kopfzeile).
3.  Fügen Sie diese am Ende der zentralen `bmad-help.csv` ein.

---

## 5. Schritt 4: Infrastruktur (MCP Server)

Die KI benötigt "Sinne" für Dokumente und Webseiten. Installieren und registrieren Sie diese global:

```bash
npm install -g @modelcontextprotocol/server-markitdown @modelcontextprotocol/server-playwright
```
*Registrieren Sie diese Server anschließend in Ihrer Gemini-CLI Konfiguration (`config.json`).*

---

## 6. Schritt 5: Erster Start & Auto-Init

1.  Starten Sie die Gemini-CLI im Projekt-Root.
2.  Führen Sie den Befehl aus:
    ```bash
    /bsg_configure_governance
    ```
3.  Wählen Sie **[A] Auto-Init**. Master Lex wird nun:
    *   Die Governance-Dateien (`.yaml` & `.ttl`) lokal anlegen.
    *   Die `schema.org` Ontologie physisch via Git/Curl herunterladen.
    *   Einen System-Check durchführen.

---

## 7. Entwicklung & Anpassung
Um das Modul zu erweitern, nutzen Sie die integrierten BMB-Workflows:
- `/bmad_bmb_edit_agent` (für Agenten-Logik)
- `/bmad_bmb_edit_workflow` (für Prozess-Änderungen)
