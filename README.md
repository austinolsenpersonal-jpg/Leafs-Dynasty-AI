# 🏒 Toronto Maple Leafs Dynasty AI  
**Franchise Control System — NHL 25 (Old-Gen & Next-Gen)**  

[![Canon v4.1](https://img.shields.io/badge/Canon-v4.1-blue)](https://github.com/austinolsenpersonal-jpg/Leafs-Dynasty-AI/releases/tag/v4.1-Full-Franchise)  
[![Ops v4.2](https://img.shields.io/badge/Ops-v4.2--mobile--baseline%2Bops--overrides-green)](https://github.com/austinolsenpersonal-jpg/Leafs-Dynasty-AI/releases/tag/v4.2-mobile-baseline%2Bops-overrides)  
[![Status](https://img.shields.io/badge/Mode-Dual--Ops%20Active-success)](https://github.com/austinolsenpersonal-jpg/Leafs-Dynasty-AI)

---

### 📘 Overview  
This repository maintains the **Canon**, **Operational Seeds**, and **Matchup Overrides** for  
_Austin Olsen’s Toronto Maple Leafs Franchise in NHL 25_.  

- Architect Config: **v6.1**  
- Canon Version: **v4.1 (Full Franchise)**  
- Operational Branch: **v4.2 (Mobile Baseline + Ops Overrides)**  
- Current Phase: Regular Season — November Segment  
- Dual-Ops Mode: **Enabled (Gameplay + Front Office)**  

---

### 📂 Repository Structure  

```
Architect/                  → Core Canon + Strategy Config  
LeafsAI/                    → Dynasty Ops & Game Data  
 ├── Canon_v4.1_Full_Franchise.json  
 ├── LeafsSeeds_Master_v4.1.json  
 ├── Season1/Operations/     → Ops delta & segment data  
 ├── Matchups/               → Game-by-game scouting / strategies  
 ├── GoaliePlan/             → Rotation / fatigue plans  
 ├── LeafsContracts_seed_v1.1.json  
 ├── Finance_seed.json  
 └── AHLDev_tracker_v1.1.json  
```

---

### 🧭 Canon State  

- Verified Canon v4.1 (unchanged)  
- Active Ops Version: **v4.2-mobile-baseline+ops-overrides**  
- Latest Snapshot: `Matchup_EDM_Prep_2024-11-16`  
- QA Integrity: ✅ **PASS** (Roster / Cap / Systems / Finance)  

---

### 🏷️ Tags  

| Tag | Description |  
|-----|--------------|  
| [v4.1-Full-Franchise](https://github.com/austinolsenpersonal-jpg/Leafs-Dynasty-AI/releases/tag/v4.1-Full-Franchise) | Original Canon baseline |  
| [v4.2-mobile-baseline+ops-overrides](https://github.com/austinolsenpersonal-jpg/Leafs-Dynasty-AI/releases/tag/v4.2-mobile-baseline%2Bops-overrides) | Ops updates (WSH lock + EDM prep + goalie plan) |  

---

### 🧰 Commands Reference  

```
/resync_baseline --from "v4.1-Full-Franchise"  
/apply_matchup --source "Matchup_WSH_FullLock_2024-11-13" --format json  
/verify_strategies && /lock_strategies  
```

---

### 📈 Changelog Summary  

**v4.2 (Mobile Baseline + Ops Overrides)**  
- Added WSH full-lock and EDM prep files  
- Integrated goalie rotation plan  
- Canon v4.1 preserved, verified QA integrity  
- Added Dual-Ops mobile support for GitHub and iPhone sync  

**v4.1 (Full Franchise Baseline)**  
- Original Canon + Architect Config v6.1  
- LeafsSeeds Master merged (Finance, Scouting, AHL Dev)  
- All legacy seeds removed, 6-file baseline created  

---

### 🧑‍💼 Maintained By  

**Austin Olsen**  
Toronto Maple Leafs — Dynasty AI Project  
📦 Canon v4.1 • Architect v6.1 • Ops v4.2  