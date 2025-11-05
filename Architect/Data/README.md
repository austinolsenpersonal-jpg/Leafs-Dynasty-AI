# 📘 Architect Data Layer (Canon v4.1 – December 2024)

This folder contains all **core data sources** that define the Toronto Maple Leafs Dynasty AI environment.

| File | Purpose | Version |
|------|----------|----------|
| **Canon_v4.1_Full_Franchise.json** | Global franchise schema and system logic. | v4.1 |
| **LeafsRoster_master_v1.4.json** | Active NHL/AHL roster, post-Dumba trade. | v1.4 |
| **LeafsContracts_seed_v1.6.json** | Full NHL/AHL contracts, terms, clauses, and AAVs. | v1.6 |
| **LeafsSeeds_Master_v5.1.json** | Prospect and draft seed data (for scouting). | v5.1 |
| **ScoutingAssignments_seed_v5.2.json** | Current scouting region coverage and class map. | v5.2 |
| **TradeDeadlinePlanner_seed_v1.3.json** | Active trade targets and negotiation tiers. | v1.3 |
| **AHLDev_tracker_v1.3.json** | Player development and readiness metrics. | v1.3 |
| **Finance_seed.json** | Budget and salary-cap baseline. | v1.0 |

---

### ⚙️ Update Procedure

1. **Update Roster and Contracts together**  
   (to prevent drift and maintain data parity).

2. **Re-run inside Dynasty AI:**
   ```bash
   /contracts_import "Architect/Data/LeafsContracts_seed_v1.6.json"
   /roster_guard set --mode strict \
     --nhl "Architect/Lines/NHL/NHL_Lines_2024-12-04.json" \
     --ahl "Architect/Lines/AHL/AHL_Lines_2024-12-04.json" \
     --contracts "Architect/Data/LeafsContracts_seed_v1.6.json"
   /qa_pre_game --focus "roster_guard,contracts,lines_sync"
   /dynasty_savepoint --tag "RosterContracts_LinesLocked_v1.6"