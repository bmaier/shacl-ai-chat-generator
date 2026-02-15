---
name: 'step-03-ontology-mapping'
description: 'Mapping der erlaubten Ontologien'
nextStepFile: './step-04-naming-policy.md'
outputFile: '{local_resource_path}/governance-config.yaml'
---

# Step 3: Ontologie-Mapping

## STEP GOAL:
Erfassung der lokalen Pfade und Präfixe für alle erlaubten Ontologien (z.B. BAMF-Core).

## MANDATORY SEQUENCE
1. Fordere den Nutzer auf, die Pfade zu den `.owl` oder `.ttl` Dateien anzugeben.
2. Definiere für jede Datei ein Präfix (z.B. `bamf-core`).
3. Master Lex validiert kurz, ob die Dateien lokal lesbar sind.

## MENU OPTIONS
[C] Weiter zur Naming Policy
