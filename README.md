# BSG: BAMF Semantic SHACL Generator & Governance Suite

Semantic Bridge: Transformieren Sie Fachwissen in W3C-Standards.

Das BSG-Modul ist ein umfassendes Ökosystem zur automatisierten Generierung von SHACL-Shapes und Ontologien aus unstrukturierten (PDF, E-Mail) und technischen (OpenAPI) Quellen unter strikter BAMF-Governance.

---

## Kernkonzepte & Highlights

*   **Semantic Bridge:** Intelligente Transformation von PDFs, E-Mails und APIs in W3C SHACL & JSON-LD.
*   **Test-Driven Development (TDD):** Integrierte BDD-Logik (Gherkin) zur Qualitätssicherung und Bug-Validierung durch Validator Victor.
*   **Action-Verification-Protocol:** Physische Verifikation aller Datei-Operationen für maximale Prozesssicherheit.
*   **Verified-Import:** Automatisierte Prüfung externer Ontologien (z.B. schema.org) vor der Registrierung.
*   **Zwei-Welten-Sprache:** Dynamische Anpassung zwischen einfacher Fachsprache und technischer Semantik-Expertise.

---

## Quick Start

**Neu hier?** Folgen Sie zuerst unserem **[Installations- & Setup-Guide](docs/installation.md)**, um alle Vorbedingungen (Node.js, KI-CLI, MCP-Server) zu erfüllen.

1.  **Init:** `/configure-governance` starten (Auto-Init nutzen).
2.  **Modellierung:** `/create-form-shape` nutzen, um ein PDF oder Text zu analysieren.
3.  **API Mapping:** `/map-api-to-shape` für technische Schnittstellen.
4.  **TDD & QS:** `/generate-test-suite` für automatisierte Qualitätssicherung.
5.  **Anwendung:** `/interactive-data-entry` für die Anwender-Unterstützung.

---

## Ihr Experten-Team

| Agent | Rolle | Kernkompetenz |
| :--- | :--- | :--- |
| **⚖️ Master Lex** | Architekt | Governance, Naming, Sokratische Erklärungen. |
| **🎨 Modeler Mia** | Fachadmin | Modellierung, PDF-Analyse (Markitdown), Ontologie-Mapping. |
| **🔍 Validator Victor** | Tester | TDD, BDD (Gherkin), Testdaten-Suiten. |
| **🙋 Guide Gaby** | Support | Endanwender-Führung, intelligente Datenerfassung. |

---

## Module Structure
```
bsg/
├── module.yaml          # Modul-Konfiguration
├── module-help.csv      # Befehls-Registry
├── agents/              # Experten-Definitionen
├── workflows/           # Schritt-für-Schritt Prozesse
├── data/ontologies/     # Lokaler semantischer Tresor
├── dist/                # Static Content für Web-Deployment
└── docs/                # Umfassende Dokumentation (Installation, Overview)
```

---

## Author
Created via BMAD Module workflow for BAMF.
