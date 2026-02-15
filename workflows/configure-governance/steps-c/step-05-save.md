---
name: 'step-05-save'
description: 'Speichern und hybrider Export (YAML + RDF)'
outputFile: '{local_resource_path}/governance-config.yaml'
rdfOutputFile: '{local_resource_path}/governance.ttl'
yamlTemplate: '../templates/governance-template.yaml'
rdfTemplate: '../templates/governance-template.ttl'
---

# Step 5: Abschluss & Hybrid-Export

## STEP GOAL:
Finale Erzeugung der operativen YAML-Konfiguration und des semantischen RDF-Exports.

## MANDATORY SEQUENCE
1. Generiere die `governance-config.yaml` basierend auf den Eingaben.
2. Generiere parallel die `governance.ttl` zur semantischen Selbst-Beschreibung.
3. Master Lex gibt eine kurze architektonische Zusammenfassung und schließt die Sitzung.

## MENU OPTIONS
[D] Konfiguration abgeschlossen
