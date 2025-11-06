# 🏒 Toronto Maple Leafs Dynasty AI
**Architect v6.1 | Canon v4.1 (Adaptive Lock)**  

Franchise Control System — NHL 25 (Old-Gen & Next-Gen)

---

## 📘 Overview
This repository contains the full operational canon and configuration for  
**Austin Olsen’s Toronto Maple Leafs Franchise in NHL 25.**

It unifies:
- Architect Config v6.1 – core AI systems and schema  
- Canon v4.1 – immutable franchise baseline  
- Adaptive Planner v6.0 – opponent AI / strategy engine  
- FullLock 2024-12-04 – verified sync (roster + lines + contracts + special teams)

---

## 📂 Repository Structure

Architect  
│  Architect_Config_v6.1.json  
│  Canon_v4.1_Full_Franchise.json  
│  OldGen_Strategy_Canon_v4.1.txt  
│  
├─ Patches  
│   ├ RepoHealth_v2.1.json  
│   ├ QA_Integrity_v3.0.json  
│   ├ TelemetrySync_v2.0.json  
│   ├ EliteOps_Patch_v4.4.json  
│   └ ExecutiveOps_Patch_v4.5.json  
│  
├─ Data  
│   ├ LeafsRoster_master_v1.4.json  
│   ├ LeafsContracts_seed_v1.6.json  
│   ├ LeafsSeeds_Master_v5.1.json  
│   ├ Finance_seed.json  
│   └ TradeDeadlinePlanner_seed_v1.3.json  
│  
└─ Lines  
  ├─ NHL  
  │   ├ NHL_Lines_2024-12-04.json  
  │   ├ NHL_SpecialTeams_2024-12-04.json  
  │   └ NHL_Template_Standard_FullGamePlan.json  
  │  
  └─ AHL  
      ├ AHL_Lines_2024-12-04.json  
      ├ AHL_SpecialTeams_2024-12-04.json  
      └ AHL_DevTracker_v1.1.json  

---

## 🎯 Canon & Ops Status
| Layer | Version | Description |
|:--|:--|:--|
| Canon | v4.1 | Immutable strategy & schema baseline |
| Architect Config | v6.1 | Core system architecture |
| Adaptive Planner | v6.0 | Opponent & matchup AI engine |
| Elite-Ops Patch | v4.4 | Predictive analytics / trade AI |
| Executive-Ops Patch | v4.5 | Automation tier – QA / snapshots |
| QA Integrity | ✅ PASS | Roster / Lines / Contracts verified |

---

## ⚙️ Canon-Locked Source Map (Active)
| Type | Source | Description |
|:--|:--|:--|
| Roster | Architect/Data/LeafsRoster_master_v1.4.json | Current NHL/AHL roster |
| Contracts | Architect/Data/LeafsContracts_seed_v1.6.json | Contract matrix |
| NHL Lines | Architect/Lines/NHL/NHL_Lines_2024-12-04.json | Even-strength units |
| AHL Lines | Architect/Lines/AHL/AHL_Lines_2024-12-04.json | Even-strength units |
| NHL Special Teams | Architect/Lines/NHL/NHL_SpecialTeams_2024-12-04.json | PP/PK logic |
| AHL Special Teams | Architect/Lines/AHL/AHL_SpecialTeams_2024-12-04.json | PP/PK formation |

**Source Priority:** primary = GitHub  |  fallback = none  
**Roster Guard:** STRICT  **Strategy Guardrails:** ENABLED  
**Savepoint:** Lines + Contracts FullLock Adaptive v6.0  

---

## 🧩 Core Modules
M67 – Advanced Analytics Engine (5v5 xG + HD chance tracking)  
M80 – Game Systems Registry (ICE-Q / Vision Control / AI movement)  
M81 – Control Map (Total Control / Skill Stick / Goalie mapping)  
M86 – Tactics Translator (Maps in-game systems → AI planning)  
M87 – Sliders Philosophy (All-Star realism baseline)  
M91 – Injury Forecast Matrix (100-run injury simulation)  
M92 – Offer Laddering Engine (Smart extensions + clauses)  
M93 – Agent Personality Model (Negotiation tone + PR)  
M95 – Goalie Book (Heatmap of high-danger shots)  
M96 – Mentorship Pairing (Vet-prospect growth)  
M100 – Risk Controls (Cap + retention guardrails)  
M121 – Analytics Expansion (Live xG / Entry-Exit tracking)  

---

## 🧠 About
Built and maintained by **Austin Olsen** using ChatGPT Architect + Leafs Dynasty AI Suite.  
Designed for full GM + Coach simulation control with analytics, morale, and adaptive AI.  

---

📂 **Primary Repository:**   
https://github.com/austinolsenpersonal-jpg/Leafs-Dynasty-AI