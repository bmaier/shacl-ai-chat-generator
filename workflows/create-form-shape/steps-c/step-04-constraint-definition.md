---
name: 'step-04-constraint-definition'
description: 'Festlegen der Feld-Regeln (Constraints)'

# File references
nextStepFile: './step-05-expert-review.md'
outputFile: '{output_folder}/shacl-modeling-{{form_name}}.md'

# Tasks
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 4: Regel-Modellierung (Constraints)

## STEP GOAL:
Definition der technischen und fachlichen Einschränkungen (Pflichtfelder, Datentypen, Logik) für jedes Feld.

## MANDATORY EXECUTION RULES:
- 🎯 **Skill-Level Anpassung:** Ändere die Fragestellung basierend auf dem in Step 1 gewählten Level.
- 📋 Modeler Mia führt den Dialog.

## MANDATORY SEQUENCE

### 1. Regeln festlegen
"Lass uns nun festlegen, was in die Felder eingetragen werden darf..."

**Aktion (Einsteiger):** Frage nach "Pflichtfeld?", "Nur Zahlen?", "Maximale Länge?".
**Aktion (Experte):** Frage nach `sh:minCount`, `sh:datatype`, `sh:pattern`.

### 2. Komplexe Logik (Optional)
"Gibt es Abhängigkeiten zwischen den Feldern? (z.B. 'Wenn A, dann muss B ausgefüllt sein')."

**Interaktion:** Nutze **Advanced Elicitation**, um die Wenn-Dann-Logik präzise zu erfassen.

### 3. MENU OPTIONS
**Select an Option:** [A] Advanced Elicitation [P] Party Mode [C] Weiter zum Governance-Gate

#### MENU HANDLING:
- IF C: Speichere die Constraints im `outputFile` und lade `nextStepFile`.
- IF Any other: help user, then redisplay menu. After other menu items execution, return to this menu.
