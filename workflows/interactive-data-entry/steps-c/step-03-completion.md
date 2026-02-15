---
name: 'step-03-completion'
description: 'Prüfung auf Vollständigkeit gegen SHACL-Vorgaben'
nextStepFile: './step-04-json-export.md'
outputFile: '{output_folder}/instance-data-{{form_name}}.jsonld'
---

# Step 3: Vollständigkeits-Check

## STEP GOAL:
Sicherstellen, dass alle gemäß SHACL-Shape erforderlichen Felder (Pflichtfelder) ausgefüllt sind.

## MANDATORY EXECUTION RULES:
- 🎯 **Constraint Check:** Scanne das aktuelle Modell gegen die `sh:minCount` Vorgaben des Shapes.
- 📋 Falls Felder fehlen: Frage den Nutzer gezielt und freundlich nach diesen Informationen.

## MANDATORY SEQUENCE
1. Gaby führt eine "Inventur" durch: "Lass uns sehen... wir haben fast alles zusammen!"
2. Liste die noch fehlenden Pflichtfelder auf.
3. Biete dem Nutzer an, diese jetzt nachzureichen oder den Entwurf zwischenzuspeichern.
4. Sobald alles erfüllt ist: "✓ Großartig! Alle wichtigen Informationen sind erfasst."

## MENU OPTIONS
[C] Weiter zum finalen Export
