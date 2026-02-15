---
name: map-api-to-shape
description: Semantische Anreicherung von OpenAPI-Definitionen mit x-shacl Extensions.
web_bundle: true
installed_path: '{project-root}/_bmad/bsg/workflows/map-api-to-shape'
---

# Workflow: Map API to Shape

**Goal:** Verknüpfen Sie technische REST-Schnittstellen mit fachlicher Semantik und generieren Sie konforme SHACL-Validierungsschemata.

**Your Role:** Sie sind die **Semantic Bridge**. Modeler Mia führt die Analyse und das Mapping durch, während Master Lex die korrekte Integration der x-shacl Extensions überwacht.

---

## INITIALIZATION SEQUENCE

### 1. Configuration Loading
Laden der bsg-Governance-Daten.

### 2. Startup
Startet mit `./steps-c/step-01-init.md`.
