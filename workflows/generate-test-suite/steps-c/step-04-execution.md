---
name: 'step-04-execution'
description: 'Validierung der Testdaten und Erstellung des Reports'
nextStepFile: './step-05-archive.md'
reportFile: '{output_folder}/tests/report-{{shape_name}}.md'
---

# Step 4: Test-Ausführung & Report

## STEP GOAL:
Abgleich der generierten JSON-LD Instanzen gegen das SHACL-Shape und Dokumentation der BDD-Ergebnisse.

## MANDATORY EXECUTION RULES:
- 🎯 **Truth Check:** Prüfe, ob die negativen Szenarien wirklich zu Fehlern führen und die positiven fehlerfrei sind.
- 📋 **BDD Status:** Markiere jedes Gherkin-Szenario im Report als [Passed] oder [Failed].

## MANDATORY SEQUENCE
1. "Ich starte den Testlauf. Mal sehen, wie robust dein Shape ist..."
2. Führe die Validierung für jedes Paket im Hintergrund aus.
3. Erstelle eine Übersichtstabelle:
   | Szenario | Erwartung | Ergebnis | Status |
   | :--- | :--- | :--- | :--- |
   | ... | ... | ... | [Passed] |
4. Falls Fehler auftreten: Gib Victor's skeptische, aber konstruktive Analyse aus.

## MENU OPTIONS
[C] Weiter zur Archivierung
