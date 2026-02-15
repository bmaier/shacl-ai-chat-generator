---
name: 'step-01b-continue'
description: 'Fortsetzung einer bestehenden Modellierungs-Sitzung'

workflowFile: '../workflow.md'
nextStepOptions:
  step-01-init: './step-01-init.md'
  step-02-source-analysis: './step-02-source-analysis.md'
  step-03-concept-mapping: './step-03-concept-mapping.md'
  step-04-constraint-definition: './step-04-constraint-definition.md'
  step-05-expert-review: './step-05-expert-review.md'
  step-06-generation: './step-06-generation.md'
---

# Step 1b: Workflow Fortsetzen

## STEP GOAL:
Wiederaufnahme der Modellierung an der Stelle, an der sie unterbrochen wurde.

## MANDATORY SEQUENCE

### 1. Willkommen zurück
"**Willkommen zurück!** Ich lade deinen letzten Stand..."

### 2. Status auslesen
Lade das aktuelle Modellierungs-Dokument und lies das Array `stepsCompleted` aus der Frontmatter.

### 3. Routing
Bestimme den nächsten Schritt basierend auf dem letzten abgeschlossenen Step und lade die entsprechende Datei.

## MENU OPTIONS
Zeige den aktuellen Fortschritt an und biete an, fortzufahren. [C] Fortfahren
