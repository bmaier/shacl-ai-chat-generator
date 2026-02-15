# BSG: BAMF Semantic SHACL Generator & Governance Suite

**Die intelligente Brücke zwischen Fachdomäne und Semantic Web.**

Das BSG-Modul (BAMF Semantic SHACL Generator) ist ein hochspezialisiertes BMAD-Framework zur automatisierten Transformation unstrukturierter Informationen in maschinenlesbare W3C-Standards. Es ermöglicht die nahtlose Integration von Fachwissen in eine kontrollierte, semantische Datenlandschaft.

---

## 🏗️ Architektur-Übersicht

Die Methode basiert auf einem **Multi-Agenten-System**, das strikt nach dem **Tri-Modalen Design-Muster** (Create, Edit, Validate) arbeitet.

### Die drei Säulen der BSG-Architektur:
1.  **Semantic Bridge:** Ein spezialisierter Extraktions-Layer, der unstrukturierte Quellen (PDF, E-Mail, API) analysiert und auf formale Ontologien mappt.
2.  **Hybrid Governance:** Ein duales Speichersystem, das operative Konfigurationen (YAML) mit semantischer Selbstbeschreibung (RDF/Turtle) kombiniert.
3.  **Action-Verification-Protocol:** Ein Sicherheits-Layer, der jede Systemoperation physisch auf Datenebene verifiziert, um Datenintegrität zu garantieren.

---

## 🛠️ Technische Spezifikationen

Das Modul erzwingt die Einhaltung modernster Industriestandards:

*   **Kern-Standards:** W3C SHACL (Shapes Constraint Language), RDF, RDFS, OWL.
*   **Vokabulare:** Unterstützung für SKOS (Codelisten), schema.org (Globaler Standard) und BAMF-Core-Ontologien.
*   **Ausgabeformate:** 
    *   **Turtle (.ttl):** Der Standard für Modellierung.
    *   **JSON-LD:** Inklusive Unterstützung für *Compact* und *Extended* Profile.
    *   **XML/RDF:** Für Legacy-System-Kompatibilität.
*   **Tooling-Integration:**
    *   `markitdown`: Deep-Parsing von PDF, DOCX und Mail-Formaten.
    *   `playwright`: Dynamische Analyse und Befüllung von Web-Interfaces.

---

## 🎯 Primäre Anwendungsfälle (Use Cases)

### 1. Digitalisierung von PDF-Formularen
Transformation von statischen Papier- oder PDF-Vorlagen in dynamische SHACL-Shapes. Die KI erkennt Eingabefelder, Datentypen und logische Abhängigkeiten.

### 2. Semantische API-Anreicherung
Erweiterung bestehender REST-Schnittstellen (OpenAPI) um `x-shacl` Extensions. Dies ermöglicht es Systemen, Schnittstellen-Daten nicht nur technisch, sondern auch inhaltlich (semantisch) zu validieren.

### 3. Intelligente Datenerfassung (Text-to-Data)
Anwender können Daten in natürlicher Sprache (E-Mails, Chat) eingeben. Das System mappt diese Informationen live auf den zugrunde liegenden SHACL-Bauplan und erzeugt fertige JSON-LD Instanzen.

### 4. Test-Driven Semantic Development (TDD)
Automatisierte Generierung von Test-Suiten mittels **Gherkin (BDD)**. Jede Datenstruktur wird bereits während des Designs gegen positive und negative Test-Szenarien validiert.

---

## 👥 Ihr Experten-Team

| Agent | Rolle | Funktion |
| :--- | :--- | :--- |
| **⚖️ Master Lex** | Architekt | Überwacht Governance, Naming und physische Verifikation. |
| **🎨 Modeler Mia** | Fachadmin | Führt die Transformation von PDF/API zu SHACL durch. |
| **🔍 Validator Victor** | Tester | Erstellt Test-Suiten (TDD) und sichert die Datenqualität. |
| **🙋 Guide Gaby** | Support | Unterstützt Endanwender bei der intuitiven Datenerfassung. |

---

## 🚀 Workflows (Slash Commands)

*   **`/bsg_configure_governance`**: Initialisierung des semantischen Rahmens und Auto-Init der BAMF-Infrastruktur.
*   **`/bsg_create_form_shape`**: Der Kern-Workflow zur Modellierung von Shapes aus Fachdokumenten.
*   **`/bsg_map_api_to_shape`**: Spezielle Logik zur semantischen Beschreibung von REST-Schnittstellen.
*   **`/bsg_generate_test_suite`**: Automatisierte Qualitätssicherung mittels BDD/Gherkin.
*   **`/bsg_interactive_data_entry`**: Intelligente Benutzeroberfläche zur Erfassung von Instanzdaten.

---

## 📦 Installation & Schnellstart

Bitte folgen Sie dem umfassenden **[Installations- & Setup-Guide](docs/installation.md)** für eine schrittweise Einrichtung.

1.  Ordner nach `_bmad/bsg/` klonen.
2.  Befehle in `_bmad/_config/bmad-help.csv` mergen.
3.  Slash-Commands aus `_bmad/bsg/data/system/commands/*.toml` nach `.gemini/commands/` kopieren.
4.  `/bsg_configure_governance` ausführen.

---

## 📂 Modul-Struktur
```
bsg/
├── module.yaml          # Modul-Konfiguration
├── module-help.csv      # Befehls-Registry
├── agents/              # Experten-Definitionen (Lex, Mia, Victor, Gaby)
├── workflows/           # Schritt-für-Schritt Prozesse (5 Workflows)
├── data/
│   ├── ontologies/      # Lokaler semantischer Tresor (BAMF, schema.org)
│   └── system/commands/ # TOML-Vorlagen für Slash-Commands
├── dist/                # Static Content für Web-Deployment (Mirroring)
├── docs/                # Umfassende Dokumentation (Installation, Overview)
└── output/              # Generierte Ergebnisse (Shapes, JSON-LD, Tests)
```

---
*Status: Produktionsreif | Version: 1.0.0 | Autor: BAMF Digitalization Team*
