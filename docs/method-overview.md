# Die BSG-Methode: BAMF Semantic SHACL Generator

## 1. Einleitung: Die Vision der Semantic Bridge
In der BAMF-Verwaltung ist wertvolles Wissen oft in unstrukturierten oder rein technischen Silos gefangen. Die BSG-Methode wurde entwickelt, um dieses Wissen für KI-Systeme und automatisierte Prozesse nutzbar zu machen. Sie baut eine intelligente Brücke von unstrukturierten Fachanforderungen zu maschinenlesbaren W3C-Standards.

### Eingabequellen der Methode:
*   **Dokumente:** Analyse von PDF-Formularen, Office-Dokumenten und E-Mails.
*   **Texte:** Extraktion aus Freitexten und manuellen Beschreibungen.
*   **Schnittstellen:** Semantische Anreicherung von REST-APIs (OpenAPI).
*   **Web:** Scannen und Befüllen von Webformularen.

## 2. Der Mehrwert (Nutzen)
*   **Demokratisierung der Modellierung:** Modellierung ohne technisches Expertenwissen durch geführte Dialoge.
*   **Integrierte Governance:** Erzwingung von BAMF-Namenskonventionen (`bamf:bereich:kontext:begriff`) und Vermeidung semantischer Redundanzen.
*   **Test-Driven Development (TDD):** Qualitätssicherung ist kein Anhang, sondern Teil des Designprozesses. Wir nutzen BDD (Gherkin), um Datenstrukturen vorab zu definieren und gegen Testdaten zu validieren.
*   **Höchste Robustheit:** Das **Action-Verification-Protocol** stellt sicher, dass jede Operation (Download, Import, Generierung) physisch geprüft wird.

## 3. Das Experten-Team (Agenten)
1.  **⚖️ Master Lex (Architekt):** Der Hüter der Spielregeln. Er prüft die Governance, registriert Ontologien über das **Verified-Import-Protokoll** und erklärt jede Entscheidung sokratisch ("Das Warum").
2.  **🎨 Modeler Mia (Modellierung):** Die kreative Fach-Übersetzerin. Sie nutzt `markitdown`, um Quellen zu analysieren, schlägt Ontologie-Verknüpfungen vor und passt ihre Sprache dem Skill-Level (Einsteiger/Experte) an.
3.  **🔍 Validator Victor (Tester):** Der Qualitätswächter. Er setzt auf **TDD und BDD**. Er erstellt Gherkin-Szenarien und JSON-LD Testdaten, um die Robustheit der Shapes sicherzustellen.
4.  **🙋 Guide Gaby (Support):** Die Begleiterin für Endanwender. Sie ermöglicht eine intuitive Datenerfassung aus Texten oder E-Mails direkt in die semantische Zielstruktur.

## 4. Die Werkzeug-Suite (Workflows)
*   **Strategie (`configure-governance`):** Festlegen des semantischen Rahmens (Basis-URLs, Codelisten). Unterstützt Auto-Init für BAMF-Standards.
*   **Modellierung (`create-form-shape`):** Transformiert Dokumente/Texte in SHACL-Shapes mit integriertem Ontologie-Abgleich (z.B. schema.org).
*   **API-Brücke (`map-api-to-shape`):** Erweitert OpenAPI um `x-shacl` Extensions für eine nahtlose IT-Integration.
*   **Qualitätssicherung (`generate-test-suite`):** Ermöglicht testgetriebene Entwicklung durch automatisierte BDD-Tests und Validierungs-Reports.
*   **Anwender-Schnittstelle (`interactive-data-entry`):** KI-gestützte Datenerfassung mit semantischem Auto-Mapping.

## 5. Technische Standards
*   **W3C-Konformität:** Erzeugt valide Turtle (.ttl), JSON-LD (Compact/Extended) und XML Artefakte.
*   **Hybrid-Storage:** Operative Flexibilität in YAML, semantische Wahrheit in RDF.
*   **Local-First:** Priorisierung lokaler Verzeichnisse (`_bmad/bsg/data/ontologies/`) vor externen Web-Ressourcen.
