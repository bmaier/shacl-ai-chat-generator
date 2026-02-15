# Workflow Specification: create-form-shape

**Module:** bsg
**Status:** Placeholder — To be created via create-workflow workflow
**Created:** 2026-02-14

---

## Workflow Overview

**Goal:** Erstellung eines SHACL-Shapes aus Fachvorgaben.

**Description:** Führt den Administrator durch den Prozess der Definition von Datenstrukturen und Constraints, basierend auf Dokumenten (PDF/Text) oder manueller Eingabe.

**Workflow Type:** Creative/Modeling

---

## Workflow Structure

### Entry Point

```yaml
---
name: create-form-shape
description: Erstellung eines SHACL-Shapes aus Fachvorgaben.
web_bundle: true
installed_path: '{project-root}/_bmad/bsg/workflows/create-form-shape'
---
```

### Mode
- [x] Tri-modal (steps-c/, steps-e/, steps-v/)

---

## Planned Steps

| Step | Name | Goal |
|------|------|------|
| 1 | Source Analysis | PDF/Text via Markitdown einlesen |
| 2 | Concept Mapping | Begriffe mit Ontologie verknüpfen |
| 3 | Constraint Definition | Regeln festlegen (Pflichtfelder etc.) |
| 4 | Expert Review | Technische Prüfung (SHACL-Syntax) |
| 5 | Generation | Turtle/JSON-LD exportieren |

---

## Workflow Inputs

### Required Inputs
- Quell-Dokument oder Text
- Ziel-Kontext (z.B. /asyl/antrag)

---

## Workflow Outputs

### Output Format
- [x] Document-producing (shape.ttl, documentation.md)

---

## Agent Integration

### Primary Agent
Modeler Mia

### Other Agents
Master Lex (Governance-Check)

---

## Implementation Notes
**Nutzen Sie den create-workflow Workflow, um diesen Workflow final zu bauen.**
