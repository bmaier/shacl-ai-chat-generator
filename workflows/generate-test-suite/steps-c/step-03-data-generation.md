---
name: 'step-03-data-generation'
description: 'Erzeugung der JSON-LD Testdaten'
nextStepFile: './step-04-execution.md'
dataFolder: '{output_folder}/tests/data/'
---

# Step 3: Testdaten-Generierung

## STEP GOAL:
Erstellung der technischen JSON-LD Instanzen, die den Gherkin-Szenarien entsprechen.

## MANDATORY EXECUTION RULES:
- 💾 **Data Separation:** Speichere die JSON-LD Daten separat vom Gherkin-Text, aber verlinke sie eindeutig.
- 🛠️ **Synthetik:** Nutze KI-Fähigkeiten, um plausible BAMF-Testdaten (Namen, Daten, IDs) zu erzeugen.

## MANDATORY SEQUENCE
1. "Ich baue jetzt die passenden Datenpakete für unsere Szenarien."
2. Generiere für jedes Szenario aus Step 2 eine entsprechende `.jsonld` Datei.
3. Zeige dem Nutzer eine Vorschau der Daten und frage nach Korrekturwünschen.
4. "Die Daten liegen bereit in {dataFolder}. Du kannst sie dort jederzeit erweitern."

## MENU OPTIONS
[C] Weiter zum Testlauf
