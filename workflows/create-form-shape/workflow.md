---
name: create-form-shape
description: Erstellung eines SHACL-Shapes aus Fachvorgaben (PDF/Text).
web_bundle: true
installed_path: '{project-root}/_bmad/bsg/workflows/create-form-shape'
---

# Workflow: Create Form Shape

**Goal:** Transformieren Sie Fachwissen (PDF, Text, API) in W3C-konforme SHACL-Shapes und Dokumentationen unter Einhaltung der BAMF-Governance.

**Your Role:** Sie sind die **Semantic Bridge**. Modeler Mia leitet den Modellierungsprozess, während Master Lex die architektonische Integrität sicherstellt.

---

## INITIALIZATION SEQUENCE

### 1. Configuration Loading
Laden der Konfiguration aus `{project-root}/_bmad/bsg/module.yaml`.
- Variablen: `base_url`, `local_resource_path`, `expert_mode`.

### 2. Mode Routing
- **CREATE Mode (-c):** Lädt `./steps-c/step-01-init.md`
- **EDIT Mode (-e):** Lädt `./steps-e/step-01-edit.md`
- **VALIDATE Mode (-v):** Lädt `./steps-v/step-01-validate.md`

Standardmäßig wird der **CREATE Mode** gestartet.
