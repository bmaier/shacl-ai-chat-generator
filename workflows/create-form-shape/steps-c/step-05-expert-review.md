---
name: 'step-05-expert-review'
description: 'Governance-Gate durch Master Lex'

# File references
nextStepFile: './step-06-generation.md'
outputFile: '{output_folder}/shacl-modeling-{{form_name}}.md'

# Tasks
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 5: Governance-Gate (Expert Review)

## STEP GOAL:
Finale Prüfung des Modell-Entwurfs durch Master Lex auf Einhaltung der BAMF-Namenskonventionen und Ontologie-Integrität.

## MANDATORY EXECUTION RULES:
- 📋 **Rollenwechsel:** Master Lex übernimmt die Führung.
- ⚖️ **Sokratische Begründung:** Jede Korrektur muss architektonisch begründet werden.

## MANDATORY SEQUENCE

### 1. Übergabe an Lex
"**Mia hat die Vorarbeit geleistet. Nun prüfe ich die architektonische Konformität.**"

**Aktion:** Master Lex scannt das Modell auf:
- Korrekte Namenskonventionen (`bamf:bereich:kontext:begriff`).
- Semantische Validität der Neuvorschläge.
- Vollständigkeit der Basis-Attribute.

### 2. Dialog bei Konflikten
"Ich sehe eine Abweichung bei [Begriff]. In der BAMF-Governance ist [Regel] vorgesehen. Ich schlage vor, wir ändern dies in [Vorschlag], weil..."

**Interaktion:** Nutzer akzeptiert Korrekturen oder diskutiert (via Party Mode).

### 3. MENU OPTIONS
**Select an Option:** [A] Advanced Elicitation [P] Party Mode [C] Weiter zum Export

#### MENU HANDLING:
- IF C: Speichere den Review-Status im `outputFile` und lade `nextStepFile`.
- IF Any other: help user, then redisplay menu. After other menu items execution, return to this menu.
