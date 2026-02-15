---
name: 'step-02-bdd-scenarios'
description: 'Design der Test-Szenarien in Gherkin-Syntax'
nextStepFile: './step-03-data-generation.md'
outputFile: '{output_folder}/tests/{{shape_name}}.feature'
---

# Step 2: BDD Szenario Design (Gherkin)

## STEP GOAL:
Definition von fachlichen Testfällen unter Verwendung von Given/When/Then.

## MANDATORY EXECUTION RULES:
- 🎯 **BDD Logic:** Formuliere jeden Testfall als Gherkin-Szenario.
- 📋 **Victor's Proposals:** Schlage mindestens 3 Standardszenarien vor (Positiv, Negativ, Grenze).
- ➕ **User Extension:** Erlaube dem Nutzer explizit, eigene Szenarien hinzuzufügen (TDD-Ansatz).

## MANDATORY SEQUENCE
1. "Lass uns festlegen, wie sich das System verhalten soll..."
2. Präsentiere die Vorschläge von Victor:
   ```gherkin
   Scenario: Erfolgreiche Validierung
     Given ein valides SHACL-Shape für 'Asylantrag'
     When alle Pflichtfelder korrekt ausgefüllt sind
     Then meldet die Validierung keinen Fehler
   ```
3. Frage den Nutzer: "Möchtest du weitere Szenarien für Bugfixes oder Spezialfälle hinzufügen?"
4. Speichere die Gherkin-Datei.

## MENU OPTIONS
[A] Advanced Elicitation (für komplexe Logik-Tests) [C] Weiter zur Daten-Generierung
