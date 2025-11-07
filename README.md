# 🏒 Toronto Maple Leafs Dynasty AI
**Architect v6.1 | Canon v4.1 (Adaptive Lock) | Elite Environment v5.4**

Franchise Control System — NHL 25 (Old-Gen & Next-Gen)

---

## 📘 Overview
This repository maintains the **complete operational canon and configuration** for  
**Austin Olsen’s Toronto Maple Leafs Franchise in NHL 25**.

It integrates:
- **Architect Config v6.1** — Core AI system architecture  
- **Canon v4.1** — Immutable franchise baseline  
- **Adaptive Planner v6.0** — Opponent-aware tactical engine  
- **EliteOps v5.4.1 Discipline** — QA & Reports governance separation  
- **SourceMap 2024-12-06 (FullLock)** — Verified sync for roster, lines, and special teams

---

## 📂 Repository Structure
```
Architect/
│  Architect_Config_v6.1.json
│  Canon_v4.1_Full_Franchise.json
│  OldGen_Strategy_Canon_v4.1.txt
│
├─ Canon/
│   ├ Changelog_v4.1.md
│   ├ CanonSync_Log.json
│
├─ Config/
│   ├ source_map.json
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
│   └ AHL/
│       ├ AHL_Lines_2024-12-04.json
│       ├ AHL_SpecialTeams_2024-12-04.json
│       └ AHL_DevTracker_v1.1.json
│
├─ Modules/
│   ├ M110_AutoRecovery.json
│   ├ M121_Analytics_Expansion_v6.json
│   ├ M220_TradeBoard_AI_v2.3.json
│
├─ Patches/
│   ├ RepoHealth_v2.2.json
│   ├ QA_Integrity_v5.5.json
│   ├ SourceLock_v6.2.json
│   ├ MatchupIntelligence_v6.2.json
│
├─ QA/
│   ├ QA_Report_2024-12-06.md
│   ├ QA_Report_2024-12-06.pdf
│   ├ Release_Notes_SourceMap_2024-12-06.md
│
└─ Reports/
    ├ GameRecap_2024-12-06_07.md
    └ future reports…
```

---

## ⚙️ Canon-Locked Source Map (Active)
| Type | Path | Version | Status |
|:--|:--|:--|:--|
| Roster | Architect/Data/LeafsRoster_master_v1.5.json | v1.5 | ✅ Verified |
| Contracts | Architect/Data/LeafsContracts_seed_v1.7.json | v1.7 | ✅ Verified |
| NHL Lines | Architect/Lines/NHL/NHL_Lines_2024-12-04.json | — | ✅ Verified |
| AHL Lines | Architect/Lines/AHL/AHL_Lines_2024-12-04.json | — | ✅ Verified |
| NHL Special Teams | Architect/Lines/NHL/NHL_SpecialTeams_2024-12-04.json | — | ✅ Verified |

**Source Priority:** GitHub (Primary) | None (Fallback)  
**Roster Guard:** STRICT  **Strategy Guardrails:** ENABLED  
**Integrity:** 100%  **Drift:** 0.00  

---

## 🧩 Core Modules
| ID | Name | Function |
|:--|:--|:--|
| M110 | Auto-Recovery | Self-heals bad syncs and restores last good snapshot |
| M121 | Analytics Expansion v6 | Tracks xG, zone entries, and heatmaps |
| M220 | TradeBoard AI v2.3 | Evaluates trades with morale + WAR weighting |
| M91 | Injury Forecast Matrix | Predictive player durability engine |
| M97 | Promotion Thresholds | Auto call-up logic for prospects |
| M100 | Risk Controls | Cap + retention guardrails |
| M409 | Neural Chemistry Mapper *(planned)* | Predicts future chemistry drift |
| M95 | Goalie Book | Visual shot-density tracking |
| M80–M89 | Game Systems & Sliders | Tactics Translator, Strategy Canon, QA gates |

---

## 🧠 About
Built and maintained by **Austin Olsen** using ChatGPT Architect + Leafs Dynasty AI Suite.  
Designed for full GM + Coach simulation control, analytics integration, and automated QA validation.  

📁 **Primary Repository:**  
🔗 https://github.com/austinolsenpersonal-jpg/Leafs-Dynasty-AI