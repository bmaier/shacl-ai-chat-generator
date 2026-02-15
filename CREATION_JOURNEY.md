# Die Entstehung des BSG-Moduls: Ein Protokoll

Dieses Dokument zeichnet den Weg von der ersten Idee bis zum fertigen BMAD-Modul **BSG (BAMF Semantic SHACL Generator)** nach.

---

## Evolution der Methode

### Phase 1 bis 4: Aufbau der Struktur
[... wie zuvor beschrieben ...]

### Phase 5: Das Robustheits-Update (Der "Berthold"-Fix)
Während des Testlaufs wurde eine kritische Schwachstelle identifiziert: Die Methode verließ sich auf die *Annahme* erfolgreicher Aktionen (z.B. Downloads).
- **Korrektur:** Einführung des **Action-Verification-Protocols**. Jeder Schritt, der Dateien manipuliert, muss nun physisch prüfen (`test -f` / `ls`), ob die Operation erfolgreich war.
- **Ontologie-Governance:** Die Einbindung externer Standards (schema.org) wurde um eine automatisierte URL-Validierung und Mime-Type-Prüfung erweitert.

---

## How-To: Reproduktion für neue Nutzer

1.  **Modul-Briefing:** `/bmad_bmb_create_module_brief` (Vision der Semantic Bridge).
2.  **Modul-Bau:** `/bmad_bmb_create_module` (Standalone, Code 'bsg').
3.  **Agenten-Bau:** `/bmad_bmb_create_agent` (Lex, Mia, Victor, Gaby mit Sidecars).
4.  **Workflow-Bau:** `/bmad_bmb_create_workflow` (Fokus auf physische Verifikation in den Schritten).
5.  **Governance-Init:** `/configure-governance` (Auto-Init für BAMF nutzen).

---
*Dokumentation aktualisiert am 15.02.2026*
