---
name: 'step-03-concept-mapping'
description: 'Feld-Mapping auf die BAMF-Ontologie'

# File references
nextStepFile: './step-04-constraint-definition.md'
outputFile: '{output_folder}/shacl-modeling-{{form_name}}.md'

# Tasks
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 3: Concept Mapping (The Semantic Bridge)

## STEP GOAL:
Verknüpfung der identifizierten Datenfelder mit bestehenden Begriffen der BAMF-Ontologie oder Kennzeichnung als neue Begriffe.

## MANDATORY EXECUTION RULES:
- 🎯 Nutze **Pattern 3 (Data Operations)**: Durchsuche die Ontologie-Dateien (`.owl`, `.ttl`) in einem Subprozess nach Übereinstimmungen.
- 💬 Der Subprozess gibt nur die Treffer (Label, URI) zurück, nicht den gesamten Dateiinhalt.
- ⚙️ FALLBACK: Suche manuell in den geladenen Kontexten, falls Subprozesse nicht verfügbar sind.

## MANDATORY SEQUENCE

### 1. Ontologie-Abgleich
"Ich vergleiche nun die gefundenen Felder mit unserem BAMF-Wörterbuch (Ontologie)..."

**Aktion:** Starte Subprozess zur Suche. Markiere Felder:
- **[Gefunden]:** `bamf:LastName` -> 95% Match mit 'Nachname'.
- **[Neu]:** 'Biometrisches Merkmal' (Kein direkter Treffer).

### 2. Bestätigung durch Nutzer
"Hier sind meine Vorschläge für die Verknüpfung. Bist du einverstanden?"

**Interaktion:** Nutzer bestätigt oder korrigiert die Zuweisungen. Bei neuen Begriffen erfolgt ein Hinweis auf den späteren Governance-Check durch Lex.

### 3. MENU OPTIONS
**Select an Option:** [A] Advanced Elicitation [P] Party Mode [C] Weiter zu den Regeln

#### MENU HANDLING:
- IF C: Speichere das Mapping im `outputFile` und lade `nextStepFile`.
- IF Any other: help user, then redisplay menu. After other menu items execution, return to this menu.
