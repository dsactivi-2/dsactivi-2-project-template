# Codex CLI Regeln für dieses Projekt

> Diese Regeln gelten für OpenAI Codex CLI und alle AI Agents die in diesem Repo arbeiten.

---

## Projekt-Kontext

Dieses Projekt verwendet das **Activi-AI Template**. Alle Regeln aus `CLAUDE.md` gelten auch hier.

---

## Pflicht-Dateien (NICHT löschen)

```
README.md
PROJECT_STATE.md
MASTER_RUNBOOK.md
PRODUCTION_CHECKLIST.md
capabilities.yml
CONTRACTS/api_contract.md
CONTRACTS/data_contract.md
ops/POLICY.md
```

---

## Vor jeder Änderung

1. **Lies zuerst:**
   - `PROJECT_STATE.md` - aktueller Status
   - `CONTRACTS/*.md` - API/DB Definitionen

2. **Bei API-Änderungen:**
   - Contract ZUERST aktualisieren
   - Dann Code ändern

3. **Bei neuen Features:**
   - In `capabilities.yml` registrieren
   - Tests hinzufügen

---

## Workflow

```
INTAKE_PROMPT.md → MASTER_PROMPT_1.md → MASTER_PROMPT_2.md
     ↓                    ↓                    ↓
  Anfrage            Ziel-Plan            Step-by-Step
  verstehen          erstellen            ausführen
```

---

## Tests sind PFLICHT

- Jede Funktion braucht Tests
- Test-Regeln in `capabilities.yml`
- Vor Commit: Tests ausführen

---

## Verboten

- Pflicht-Dateien löschen
- Contracts ohne Dokumentation ändern
- Code ohne Tests
- Production ohne Checklist
