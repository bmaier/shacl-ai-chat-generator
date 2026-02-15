---
name: 'step-06-generation'
description: 'Generierung der SHACL-Dateien und Dokumentation'

# File references
outputFile: '{output_folder}/shacl-modeling-{{form_name}}.md'
shapeOutputFile: '{output_folder}/{{form_name}}.ttl'
templateFile: '../templates/shape-template.ttl'
---

# Step 6: Abschluss & Artefakt-Generierung

## STEP GOAL:
Erstellung der finalen W3C-konformen SHACL-Datei und der fachlichen Dokumentation.

## MANDATORY SEQUENCE

### 1. Datei-Erzeugung
"**Alles bereit! Ich generiere nun deine Artefakte.**"

**Aktion:**
1. Erzeuge die `shapeOutputFile` (.ttl) basierend auf dem Modell und dem `templateFile`.
2. Finalisiere die `outputFile` (.md) als vollständige Dokumentation.

### 2. Zusammenfassung & Download
"✓ **SHACL-Shape erstellt:** {shapeOutputFile}
✓ **Dokumentation erstellt:** {outputFile}"

Gib Hinweise zum Deployment als Static Content (Static Publish).

### 3. Nächste Schritte
"Was möchtest du als Nächstes tun?"
- Test-Suite generieren (Victor).
- In ein anderes Format exportieren (Export Format).

## MENU OPTIONS
**Select an Option:** [V] Test-Suite starten [D] Fertig

#### MENU HANDLING:
- IF D: Markiere Workflow als abgeschlossen und beende die Sitzung.
