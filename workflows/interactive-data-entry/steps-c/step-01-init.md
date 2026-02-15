---
name: 'step-01-init'
description: 'Start der Datenerfassung und Modus-Wahl'
nextStepFile: './step-02-capture-logic.md'
outputFile: '{output_folder}/instance-data-{{form_name}}.jsonld'
---

# Step 1: Willkommen bei der Datenerfassung

## STEP GOAL:
Begrüßung des Nutzers und Festlegung, wie die Daten eingegeben werden sollen.

## MANDATORY SEQUENCE
1. Begrüße den Nutzer herzlich als **Guide Gaby**.
2. Frage, für welches Thema/Formular Daten erfasst werden sollen (lade verfügbare SHACL-Shapes).
3. Biete zwei Wege an:
   - **[E]xtraktion:** Ich lese Daten aus einem Dokument (PDF/E-Mail) für dich aus.
   - **[G]eführte Eingabe:** Wir unterhalten uns einfach, und ich fülle alles aus.

## MENU OPTIONS
[C] Weiter zur Dateneingabe
