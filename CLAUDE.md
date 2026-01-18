# Claude CLI Regeln für dieses Projekt

> Diese Regeln gelten für Claude Code CLI und alle AI Agents die in diesem Repo arbeiten.

---

## PFLICHT: Template Compliance

Dieses Projekt basiert auf dem **Activi-AI Template**. Folgende Regeln sind PFLICHT:

### 1. Pflicht-Dateien NIEMALS löschen

Diese Dateien dürfen NICHT gelöscht oder umbenannt werden:
- `README.md`
- `PROJECT_STATE.md`
- `MASTER_RUNBOOK.md`
- `PRODUCTION_CHECKLIST.md`
- `capabilities.yml`
- `CONTRACTS/api_contract.md`
- `CONTRACTS/data_contract.md`
- `ops/POLICY.md`

### 2. Contracts-First

**VOR jeder Backend-Änderung:**
1. Lies `CONTRACTS/api_contract.md`
2. Lies `CONTRACTS/data_contract.md`
3. Änderungen an API/DB → ZUERST Contract aktualisieren
4. DANN erst Code ändern

### 3. Single Source of Truth

`PROJECT_STATE.md` ist die **einzige Wahrheit** über den Projekt-Status.
- Bei Statusänderungen → `PROJECT_STATE.md` aktualisieren
- Bei Unklarheiten → `PROJECT_STATE.md` lesen

### 4. Capabilities mit Tests

Jede neue Funktion MUSS:
1. In `capabilities.yml` registriert werden
2. Tests haben (gemäß `capabilities.yml` Test-Regeln)
3. Keine Funktion ohne Test!

### 5. Production Checklist

**VOR Go-Live:**
- Lies `PRODUCTION_CHECKLIST.md`
- Alle Punkte MÜSSEN abgehakt sein
- Keine Ausnahmen

---

## Workflow

1. **Neues Feature:**
   - Lies `MASTER_RUNBOOK.md` für Steps
   - Folge dem 3-Stufen Workflow in `PROMPTS/`

2. **Bug Fix:**
   - Prüfe ob Contract betroffen
   - Update `capabilities.yml` wenn neue Tests nötig

3. **Vor Commit:**
   - `./scripts/check_template_compliance.sh` ausführen
   - Tests ausführen

---

## Verbotene Aktionen

❌ Pflicht-Dateien löschen
❌ Contracts still ändern (ohne Dokumentation)
❌ Code ohne Tests
❌ Production-Deploy ohne Checklist
❌ `PROJECT_STATE.md` ignorieren

---

## Bei Fragen

1. Lies `ops/OPEN_QUESTIONS.md`
2. Dokumentiere neue Fragen dort
3. Lies `ops/DECISIONS.md` für Architektur-Entscheidungen
