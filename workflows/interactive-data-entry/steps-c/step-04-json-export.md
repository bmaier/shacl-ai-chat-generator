---
name: 'step-04-json-export'
description: 'Finalisierung und Export der JSON-LD Instanz'
outputFile: '{output_folder}/instance-data-{{form_name}}.jsonld'
---

# Step 4: Finalisierung & Export

## STEP GOAL:
Erzeugung des finalen maschinenlesbaren JSON-LD Dokuments.

## MANDATORY SEQUENCE
1. Frage den Nutzer nach dem gewünschten JSON-LD Format:
   - **Compact:** Kürzer und besser lesbar für Menschen.
   - **Extended:** Vollständige Tripel-Struktur (ideal für Systeme).
2. Generiere das Dokument basierend auf den erfassten Daten und den Ontologie-Referenzen.
3. Bestätige den Speicherort: `{outputFile}`.
4. "✓ Dein Datenpaket ist fertig und bereit für die weitere Verarbeitung im BAMF!"

## MENU OPTIONS
[D] Erfassung abgeschlossen
