---
name: 'step-02-source-analysis'
description: 'Quelldokument einlesen und Extraktions-Fokus festlegen'

# File references
nextStepFile: './step-03-concept-mapping.md'
outputFile: '{output_folder}/shacl-modeling-{{form_name}}.md'

# Tasks
advancedElicitationTask: '{project-root}/_bmad/core/workflows/advanced-elicitation/workflow.xml'
partyModeWorkflow: '{project-root}/_bmad/core/workflows/party-mode/workflow.md'
---

# Step 2: Dokumenten-Analyse

## STEP GOAL:
Einlesen des Quelldokuments via Markitdown und Definition der zu extrahierenden Informationsbereiche durch den Nutzer.

## MANDATORY EXECUTION RULES:
- 🎯 Nutze das `markitdown` Tool, um PDF- oder Office-Dateien in Markdown zu wandeln.
- 📋 Modeler Mia leitet die Analyse.
- ✅ Sprich in einfacher Sprache (für Einsteiger) oder präziser Fachsprache (für Experten).

## MANDATORY SEQUENCE

### 1. Quelldokument laden
"**Bitte gib den Pfad zum Quelldokument an** (oder kopiere den Text hier hinein)."

**Aktion:** Wandle die Datei/den Text via `markitdown` in strukturiertes Markdown um und zeige eine kurze Zusammenfassung der gefundenen Abschnitte.

### 2. Fokus festlegen (Optionaler Stakeholder Input)
"Möchtest du, dass ich auf bestimmte Informationen besonders achte? (z.B. 'Nur Adressdaten' oder 'Alle Pflichtfelder aus dem PDF')."

**Aktion:** Speichere die Fokus-Themen für die nächsten Schritte.

### 3. Vorschlag der Datenfelder
"Basierend auf dem Dokument habe ich folgende Bereiche identifiziert, die wir in SHACL abbilden können:
- [Liste der Bereiche]"

### 4. MENU OPTIONS
**Select an Option:** [A] Advanced Elicitation [P] Party Mode [C] Weiter zum Mapping

#### MENU HANDLING:
- IF C: Hänge die Zusammenfassung der Analyse an das `outputFile` an, aktualisiere `stepsCompleted` und lade `nextStepFile`.
- IF Any other: help user, then redisplay menu. After other menu items execution, return to this menu.
