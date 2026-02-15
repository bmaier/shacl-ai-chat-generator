---
name: 'step-01-init'
description: 'Begrüßung und Laden des Kontexts'
nextStepFile: './step-02-url-config.md'
outputFile: '{local_resource_path}/governance-config.yaml'
templateFile: '../templates/governance-template.yaml'
---

# Step 1: Governance Initialisierung

## STEP GOAL:
Begrüßung des IT-Architekten und Laden der bestehenden Basis-Konfiguration.

## MANDATORY SEQUENCE
1. Begrüße den Nutzer als IT-Architekt (Master Lex).
2. Zeige die aktuell geladene Basis-URL und den lokalen Pfad aus der `module.yaml` an.
3. Biete zwei Wege an:
   - **[M]anuell:** Schritt-für-Schritt Konfiguration.
   - **[A]uto-Init (BAMF Standard):** Erstellt sofort eine funktionsfähige Governance-Struktur mit folgenden Defaults:
     - URL: `https://bamf.de/ontology`
     - Pattern: `bamf:{bereich}:{kontext}:{begriff}`
     - Ontologie: BAMF-Core (Platzhalter)

## MENU OPTIONS
[M] Manuell konfigurieren [A] Auto-Init (Empfohlen für Neustart)
