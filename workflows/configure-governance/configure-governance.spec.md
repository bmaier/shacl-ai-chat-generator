# Workflow Specification: configure-governance

**Module:** bsg
**Status:** Placeholder — To be created via create-workflow workflow
**Created:** 2026-02-14

---

## Workflow Overview

**Goal:** Festlegen der zentralen Architektur-Vorgaben.

**Description:** Dieser Workflow erlaubt es dem Architekten, Basis-URLs, Ontologie-Quellen und Namenskonventionen für das gesamte Modul zu definieren.

**Workflow Type:** Configuration

---

## Workflow Structure

### Entry Point

```yaml
---
name: configure-governance
description: Festlegen der zentralen Architektur-Vorgaben.
web_bundle: true
installed_path: '{project-root}/_bmad/bsg/workflows/configure-governance'
---
```

### Mode
- [x] Create-only (steps-c/)

---

## Planned Steps

| Step | Name | Goal |
|------|------|------|
| 1 | Load Context | Aktuelle Config laden |
| 2 | Define URLs | Basis-URLs festlegen |
| 3 | Map Ontologies | Erlaubte Ontologien listen |
| 4 | Set Naming | Namenskonventionen definieren |
| 5 | Save & Apply | Config aktualisieren |

---

## Workflow Inputs

### Required Inputs
- Basis-URL
- Pfade zu .owl Dateien

---

## Workflow Outputs

### Output Format
- [x] Document-producing (governance-config.yaml)

---

## Agent Integration

### Primary Agent
Master Lex

---

## Implementation Notes
**Nutzen Sie den create-workflow Workflow, um diesen Workflow final zu bauen.**
