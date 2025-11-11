# 🏒 Toronto Maple Leafs Dynasty AI  
**Architect v6.2 | Canon v4.1 (Adaptive Lock)**  

Franchise Control System — NHL 25 (Old-Gen & Next-Gen)

<!-- ARCHITECT-STATUS:START -->
## 🧩 Leafs Dynasty AI – System Status

**Integrity:** 100%  |  **Canon:** v4.1  |  **PatchSuite:** v1.6.0  
**Architect:** v6.2  |  **Dynasty:** v5.0.1  
**Last Sync:** (pending first auto-update)  |  **Next QA:** (pending)

*This banner auto-updates after each Daily Ops run.*
<!-- ARCHITECT-STATUS:END -->


---

## 📘 Overview
This repository maintains the full operational canon, configuration, and adaptive matchup intelligence for  
**Austin Olsen’s Toronto Maple Leafs Franchise in NHL 25.**

It unifies and automates all systems governing roster, contracts, strategies, analytics, and gameplay adaptation.  

- Architect Config → **v6.2 (Enhanced Stability + SourceLock)**
- Canon Version → **v4.1 (Full Franchise Baseline)**
- Patch Suite → **v6.2 (QA, Repo Health, SourceLock, Matchup Intelligence)**
- Opponent Model → **v6.3 (Adaptive Strategies + Goalie + Line Sliders)**
- Environment → **EliteOps v5.4 (Stable)**

---

## 📂 Repository Structure

```
Architect/
│  Architect_Config_v6.2.json
│  Canon_v4.1_Full_Franchise.json
│  OldGen_Strategy_Canon_v4.1.txt
│
├─ Config/
│   ├ source_map.json
│   └ OpponentModel_v6.3.json
│
├─ Patches/
│   ├ QA_Integrity_v5.5.json
│   ├ RepoHealth_v2.2.json
│   ├ SourceLock_v6.2.json
│   ├ MatchupIntelligence_v6.2.json
│   ├ EliteOps_Patch_v4.4.json
│   └ ExecutiveOps_Patch_v4.5.json
│
├─ Data/
│   ├ LeafsRoster_master_v1.5.json
│   ├ LeafsContracts_seed_v1.7.json
│   ├ LeafsSeeds_Master_v5.1.json
│   ├ Finance_seed.json
│   └ TradeDeadlinePlanner_seed_v1.3.json
│
├─ Lines/
│   ├ NHL/
│   │   ├ NHL_Lines_2024-12-04.json
│   │   ├ NHL_SpecialTeams_2024-12-04.json
│   │   └ NHL_Template_Standard_FullGamePlan.json
│   │
│   └ AHL/
│       ├ AHL_Lines_2024-12-04.json
│       ├ AHL_SpecialTeams_2024-12-04.json
│       └ AHL_DevTracker_v1.1.json
│
├─ Matchups/
│   └ NHL/
│       └ Generated/
│           ├ MatchupCard_<TEAM>_<DATE>.md
│           └ MatchupRuntime_<TEAM>_<DATE>.json
│
├─ QA/
│   ├ QA_Report_2024-12-06.md
│   ├ QA_Report_2024-12-06.pdf
│   ├ QA_Verify_After_Upgrade.md
│   └ Release_Notes_SourceMap_2024-12-06.md
│
└─ Reports/
    └ GameRecap_2024-12-06_07.md
```

---

## 🎯 Canon & Ops Status

| Layer | Version | Description |
|:--|:--|:--|
| **Canon** | v4.1 | Immutable strategy & schema baseline |
| **Architect Config** | v6.2 | Core system architecture with SourceLock |
| **Patch Suite** | v6.2 | QA, Repo Health, SourceLock, Matchup Intelligence |
| **Opponent Model** | v6.3 | Adaptive strategies, goalie logic, and sliders |
| **Elite-Ops Patch** | v4.4 | Predictive analytics / trade AI |
| **Executive-Ops Patch** | v4.5 | Automation tier – QA / snapshots |
| **QA Integrity** | ✅ PASS | Roster / Lines / Contracts verified |

---

## 🧠 Adaptive Matchup Intelligence (OpponentModel v6.3)
Opponent Model v6.3 integrates tactical opponent awareness with dynamic lineup optimization.

**Core Capabilities**
- Real-time opponent recognition (last 5-game telemetry)
- Adaptive team strategies (forecheck, neutral zone, DZ pressure, breakout)
- Automatic **starting goalie recommendation** (form + fatigue)
- **Starting lines (F1–F4, D1–D3)** suggested per matchup
- **Authentic NHL25 line sliders (0–10 scale)**  
  - *Offense:* Strategy + Carry/Dump, Cycle/Shoot, Efficiency/Energy, Don’t Block/Block  
  - *Defense:* Hold Line/Pinch, Cycle/Shoot  
- Outputs full **Matchup Cards** and runtime JSONs

**Output Files**
```
Architect/Matchups/NHL/Generated/
├ MatchupCard_<OPPONENT>_<DATE>.md
└ MatchupRuntime_<OPPONENT>_<DATE>.json
```

---

## 🧩 Core Modules

| Module | Function |
|:--|:--|
| **M67** | Advanced Analytics Engine (5v5 xG + HD chance tracking) |
| **M80** | Game Systems Registry (ICE-Q, Vision Control, AI movement) |
| **M81** | Control Map (Total Control / Skill Stick / Goalie mapping) |
| **M86** | Tactics Translator (Maps in-game systems → AI planning) |
| **M87** | Sliders Philosophy (All-Star realism baseline) |
| **M91** | Injury Forecast Matrix (100-run simulation) |
| **M92** | Offer Laddering Engine (Smart extensions + clauses) |
| **M93** | Agent Personality Model (Negotiation tone + PR) |
| **M95** | GoalieBook 2.0 (High-danger shot heatmaps) |
| **M96** | Mentorship Pairing (Vet-prospect growth tracking) |
| **M100** | Risk Controls (Cap + retention guardrails) |
| **M110** | AutoRecovery (Smart self-repair for config corruption) |
| **M121** | Analytics Expansion (Live WAR, TOI%, PPxG tracking) |
| **M220** | TradeBoard AI v2.3 (Morale + WAR-weighted trade advisor) |

---

## ⚙️ Patch Suite v6.2 Summary

| Patch | Version | Description |
|:--|:--|:--|
| **QA Integrity** | v5.5 | Dual-verification checksum, 40% fewer validation errors |
| **Repo Health** | v2.2 | Detects duplicate/orphan JSONs, adds cleanup guard |
| **SourceLock** | v6.2 | Two-factor verification (timestamp + checksum) |
| **Matchup Intelligence** | v6.2 | Expanded xGF/xGA & forecheck counters |
| **Opponent Model** | v6.3 | Adaptive strategy + sliders + goalie rotation logic |

---

## 🧾 Current Canon Tags

| Tag | Description |
|:--|:--|
| **CanonSync_2024-12-07_OPS-DISC-5.4.1** | QA & Reports governance rule (Ops Discipline) |
| **SourceMap_2024-12-06_Locked** | Verified source alignment (Roster v1.5 / Contracts v1.7 / Lines Dec 4) |
| **PatchSuite_v6.2_Upgrades** | Integrated QA, RepoHealth, SourceLock, Matchup Intelligence |
| **OpponentModel_v6.3_Enabled** | Adaptive planner fully activated |

---

## 🧭 Governance & Integrity
- **Canon Integrity:** 100% (Drift: 0.00)  
- **QA Discipline Lock:** Active (v5.4.1)  
- **SourceLock:** Enabled (v6.2)  
- **AutoRecovery:** Active (M110)  
- **Analytics Engine:** Expanded (M121 v6)  
- **TradeBoard Advisor:** Operational (M220 v2.3)

---

## 🧠 About
Built and maintained by **Austin Olsen** using ChatGPT Architect + Leafs Dynasty AI Suite.  
Designed for full GM + Coach simulation control with analytics, morale, and adaptive AI intelligence.  

---

📂 **Primary Repository:**  
[https://github.com/austinolsenpersonal-jpg/Leafs-Dynasty-AI](https://github.com/austinolsenpersonal-jpg/Leafs-Dynasty-AI)