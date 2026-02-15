---
name: 'step-02-capture-logic'
description: 'Intelligente Erfassung und semantisches Mapping'
nextStepFile: './step-03-completion.md'
outputFile: '{output_folder}/instance-data-{{form_name}}.jsonld'
---

# Step 2: Intelligente Datenerfassung

## STEP GOAL:
Erfassung der Informationen durch den Nutzer und automatisches Mapping auf SHACL-Felder basierend auf Semantik.

## MANDATORY EXECUTION RULES:
- 🎯 **Semantic Matching:** Vergleiche jede Nutzereingabe mit den Labels der Ontologie und den Properties des SHACL-Shapes.
- 💬 **Confirmation:** Frage bei Übereinstimmungen freundlich nach: "Ich habe verstanden, dass [Info] zu [Feld] gehört. Richtig?"

## MANDATORY SEQUENCE
1. Falls **Extraktion** gewählt wurde: Nutze `markitdown`, um das Dokument vorzuverarbeiten und erste Felder vorzuschlagen.
2. Falls **Geführte Eingabe** gewählt wurde: Fordere den Nutzer auf, Informationen in freier Textform einzugeben (z.B. "Der Antragsteller ist Max Mustermann").
3. Analysiere den Text live:
   - Identifiziere Entitäten.
   - Suche passende SHACL-Properties.
   - Bestätige das Mapping mit dem Nutzer.
4. Zeige dem Nutzer jederzeit an, welche Felder bereits "erkannt" wurden.

## MENU OPTIONS
[A] Advanced Elicitation (bei komplexen Angaben) [C] Weiter zum Vollständigkeits-Check
