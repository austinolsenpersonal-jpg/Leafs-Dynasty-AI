# 🏒 Toronto Maple Leafs Dynasty AI  
**Franchise Control System — NHL 25 (Old-Gen & Next-Gen)**  
[![Canon v4.1](https://img.shields.io/badge/Canon-v4.1-blue)](https://github.com/austinolsenpersonal-jpg/Leafs-Dynasty-AI/releases/tag/v4.1-Full-Franchise)
[![EliteOps v4.4](https://img.shields.io/badge/EliteOps-v4.4-orange)](https://github.com/austinolsenpersonal-jpg/Leafs-Dynasty-AI/releases/tag/v4.4-EliteOps%2BTradeSim)
[![ExecOps v4.5](https://img.shields.io/badge/ExecOps-v4.5-success)](https://github.com/austinolsenpersonal-jpg/Leafs-Dynasty-AI/releases/tag/v4.5-ExecutiveOps)
[![Status](https://img.shields.io/badge/Mode-Dual--Ops%20(Elite%2BExec)-brightgreen)](https://github.com/austinolsenpersonal-jpg/Leafs-Dynasty-AI)

---

### 📘 Overview
This repository maintains the **Canon**, **Operational Seeds**, and **Matchup Overrides** for  
_Austin Olsen’s Toronto Maple Leafs Franchise in NHL 25_.  

- Architect Config → **v6.1**  
- Canon Version → **v4.1 (Full Franchise)**  
- Operational Tier → **v4.5 Executive-Ops (Elite + Automation)**  
- Current Phase → Regular Season — November Segment  
- Dual-Ops Mode → **Enabled (Front Office + Gameplay)**  

---

### 📂 Repository Structure
```
Architect/                     → Core Canon + Patches
 ├── Architect_Config_v6.1.json
 ├── OldGen_Strategy_Canon_v4.1.txt
 ├── EliteOps_Patch_v4.4.json
 └── ExecutiveOps_Patch_v4.5.json

LeafsAI/                       → Dynasty Ops & Game Data
 ├── Canon_v4.1_Full_Franchise.json
 ├── LeafsSeeds_Master_v4.1.json
 ├── LeafsRoster_master_v1.2.json
 ├── LeafsContracts_seed_v1.1.json
 ├── Finance_seed.json
 ├── AHLDev_tracker_v1.1.json
 ├── Season1/Operations/ops_delta_*.json
 ├── Matchups/
 ├── GoaliePlan/
 ├── Trades/
 ├── Health/
 ├── Development/
 └── Reports/

elite/                         → Analytics & Visuals
 ├── chemistry_latest.json
 └── visuals/performance_trend_dashboard.json

snapshots/auto/                → Auto-saved baselines & matchups
```

---

### 🧭 Canon & Ops Status
| Layer | Version | Description |
|:------|:--------|:-------------|
| **Canon** | v4.1 | Immutable strategy & schema baseline |
| **Elite-Ops** | v4.4 | Predictive tier – injury forecast, trade AI, dev tracking |
| **Executive-Ops** | v4.5 | Automation tier – weekly QA, auto-snapshots, trend dashboard, finance projection |
| **QA Integrity** | ✅ PASS | Roster / Cap / Systems / Finance |

---

### 📊 Core Modules
| ID | Module | Function |
|:--:|:--------|:----------|
| M67 | Advanced Analytics Engine | 5v5 xG + HD chance tracking |
| M91+ | Injury Forecast Matrix | Weekly player risk simulation |
| M92E | Trade Risk Auditor | Morale + WAR impact before deals |
| M96R | Dev Tracker 2.0 | AHL progress / ETA estimates |
| M97P | Performance Trend Visual | Rolling 10-game xG / chem / injury graph |
| M78F | Finance Projection Model | Promo ROI + morale forecast |
| M100X | Executive Decision Matrix | Win-now vs future value balancing |
| M101G | Governance Guardrails | Enforces Canon rules (cap buffer ≥ $0.5 M) |
| M102F | Finance Horizon Engine | 1-3 year cap & budget forecast |
| M103M | Morale Vector AI | Predicts morale ripple effects |
| M104R | Risk Sentinel Core | Consolidates injury/trade/cap risk |
| M42E | Auto-Snapshot Sync | GitHub backup after each sim |

---

### 🧰 Commands Reference
```
/resync_baseline --from "v4.1-Full-Franchise"
/apply_matchup --source "Matchup_EDM_FullLock_2024-11-16" --format json
/verify_strategies && /lock_strategies
/qa_weekly --auto every_sunday
/snapshot_auto --mode full --interval after_each_sim
/enable_visual "performance_trend" --mode dashboard
/finance_audit
/executive_summary
/risk_audit
/morale_report
/finance_horizon --years 3
```

---

### 🏷️ Tags & Snapshots
| Tag | Description |
|-----|-------------|
| [v4.1-Full-Franchise](https://github.com/austinolsenpersonal-jpg/Leafs-Dynasty-AI/releases/tag/v4.1-Full-Franchise) | Original Canon baseline |
| [v4.4-EliteOps+TradeSim](https://github.com/austinolsenpersonal-jpg/Leafs-Dynasty-AI/releases/tag/v4.4-EliteOps%2BTradeSim) | Predictive tier (M71/M73/M75) |
| [v4.5-ExecutiveOps](https://github.com/austinolsenpersonal-jpg/Leafs-Dynasty-AI/releases/tag/v4.5-ExecutiveOps) | Automation tier – QA + Snapshot + Dashboards |

---

### 🧾 Change Log Highlights
- **v4.5 Executive-Ops:** auto-QA weekly, post-sim snapshots, performance trend visual, finance projection, morale vector, risk sentinel  
- **v4.4 Elite-Ops:** injury forecast, trade AI, AHL dev tracking  
- **v4.3E:** analytics + pattern learning + chemistry visuals  
- **v4.1 Canon:** verified baseline and architect config v6.1  

---

### 📈 Active Visual Dashboards
- **Injury Heatmap Overlay:** color-coded risk zones (🟢 safe → 🔴 high)  
- **Performance Trend Dashboard:** 10-game rolling xG / chem / injury curve  
- **Finance Projection Chart:** forecasted revenue + morale impact  

---

### 🧠 About
Built and maintained by **Austin Olsen** using ChatGPT Architect & Leafs Dynasty AI Suite.  
Designed for full GM + Coach simulation control, analytics tracking, and automated QA for NHL 25 Franchise Mode.