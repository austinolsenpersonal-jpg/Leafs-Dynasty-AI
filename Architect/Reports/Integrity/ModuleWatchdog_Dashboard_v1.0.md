# Module Watchdog – Integrity Dashboard (v1.0)

Environment: Leafs Dynasty Architect  
Canon: v4.1 • PatchSuite: NHL 25 v1.6.0  
Watchdog Config: `Architect/Config/ModuleWatchdog_v1.0.json`  
Latest Alerts:  
- JSON → `Architect/Reports/Integrity/ModuleWatchdog_Alerts_latest.json`  
- MD   → `Architect/Reports/Integrity/ModuleWatchdog_Alerts_latest.md`  

---

## 🔍 Overview

This dashboard summarizes the health of all core planner/config modules that power Leafs Dynasty AI.

**Status legend:**

- ✅ Healthy – version + checksum match expected, no drift detected  
- ⚠️ Warning – non-critical drift or version mismatch; review recommended  
- ❌ Critical – missing file, corrupted JSON, or drift in a critical module  

Status values are sourced from:

- `/watchdog scan --config "Architect/Config/ModuleWatchdog_v1.0.json" --output "latest"`  
- DailyOps Integrity section (if enabled)

---

## 🧩 Core Modules – Current Integrity Snapshot

> For detailed, machine-generated alerts, see  
> `Architect/Reports/Integrity/ModuleWatchdog_Alerts_latest.md`.

### Cap / Contracts / Trades / Deadline

| Module            | Path                                            | Expected Version | Status | Notes |
|-------------------|-------------------------------------------------|------------------|--------|-------|
| CapFlex           | `Architect/Config/CapFlex_v2.2.json`           | v2.2             | ✅ / ⚠️ / ❌ | Cap buffer, daily accrual, bonus overage, retentions. |
| TradePlanner      | `Architect/Config/TradePlanner_v2.1.json`      | v2.1             | ✅ / ⚠️ / ❌ | Value bands, FoW discounts, buyer/seller modes. |
| ContractPlanner   | `Architect/Config/ContractPlanner_v2.0.json`   | v2.0             | ✅ / ⚠️ / ❌ | Offer laddering, clauses, agent personas. |
| DeadlinePlanner   | `Architect/Config/DeadlinePlanner_v2.1.json`   | v2.1             | ✅ / ⚠️ / ❌ | Win-Now vs Futures-Guard, retention & cap guards. |

---

### Roster / AHL / Waivers / Injuries

| Module                | Path                                                       | Expected Version | Status | Notes |
|-----------------------|------------------------------------------------------------|------------------|--------|-------|
| PromotionThresholds   | `Architect/Config/PromotionThresholds_v1.2.json`          | v1.2             | ✅ / ⚠️ / ❌ | AHL→NHL readiness, TOI%, morale, form. |
| Waivers & Call-Up     | `Architect/Config/Waivers_CallUp_Planner_v2.0.json`       | v2.0             | ✅ / ⚠️ / ❌ | Waiver eligibility, emergency recalls, depth matrix. |
| Injury Insurance Tie-In | `Architect/Config/InjuryInsurance_TieIn_v1.1.json`      | v1.1             | ✅ / ⚠️ / ❌ | M91 Monte Carlo injury readiness + replacement logic. |

---

### Scouting / Draft / Opponent

| Module             | Path                                                   | Expected Version | Status | Notes |
|--------------------|--------------------------------------------------------|------------------|--------|-------|
| DraftBoard Planner | `Architect/Config/DraftBoard_Planner_v1.9.json`       | v1.9             | ✅ / ⚠️ / ❌ | Tiered board, round weights, risk scores. |
| ScoutingCycle      | `Architect/Config/ScoutingCycle_v2.0.json`            | v2.0             | ✅ / ⚠️ / ❌ | Monthly allocations + FoW discounts, Focus List. |
| OpponentMemory     | `Architect/Config/OpponentMemory_v2.0.json`           | v2.0             | ✅ / ⚠️ / ❌ | Last 6 games tendencies, pre-tilts matchup/bench cards. |

---

## 🧠 Watchdog Behaviour

**Config:** `Architect/Config/ModuleWatchdog_v1.0.json`  

Key settings:

- `checksum_drift_allowed: 0` → any unexpected change is flagged  
- `version_mismatch_alert: true` → version field must match expected  
- `max_critical_drift_before_red: 1` → more than one critical module drifting = ❌ red status  

**On drift detected:**

- Logs details to:  
  - `ModuleWatchdog_Alerts_latest.json`  
  - `ModuleWatchdog_Alerts_latest.md`  
- Marks affected module(s) ⚠️ or ❌ in the alerts report  
- Suggests snapshot restore (see Snapshots section below)

---

## 🕒 Automation Hooks

Active automation (recommended):

- **Title:** `Module Watchdog (Post-Commit)`  
- **Behaviour:**  
  - Runs `/watchdog scan` on a schedule.  
  - Notifies if any drift is detected.  

Example command used to create it:

```text
/automation create --title "Module Watchdog (Post-Commit)" --prompt "Run /watchdog scan --config 'Architect/Config/ModuleWatchdog_v1.0.json' --output 'latest' and notify me if any drift is detected." --schedule "BEGIN:VEVENT
RRULE:FREQ=HOURLY;INTERVAL=1;BYMINUTE=0,15,30,45;BYSECOND=0
END:VEVENT"