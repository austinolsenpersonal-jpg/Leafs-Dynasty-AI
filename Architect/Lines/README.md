# 🏒 Architect Lines Layer (Canon v4.1 – December 2024)

This folder defines the **active on-ice configurations** for both the NHL and AHL teams.  
All line JSONs, formations, and special-teams strategies in this directory represent the *current* verified state of the Toronto Maple Leafs Dynasty AI environment.

---

### 📂 Directory Layout

| File | Level | Purpose | Date |
|------|--------|----------|------|
| **NHL/NHL_Lines_2024-12-04.json** | NHL | Official Toronto Maple Leafs lines, pairings, and goalie plan (post-Dumba trade). | 2024-12-04 |
| **AHL/AHL_Lines_2024-12-04.json** | AHL | Toronto Marlies active lines and development deployment. | 2024-12-04 |
| **Templates/MatchupTemplate_Standard_FullGamePlan.json** | NHL | Default matchup template (Rielly active, rivalry tuning). | v1.0 |
| **Templates/MatchupTemplate_Rotation_Myerson_v1.0.json** | NHL | Rotation / workload template (Myers in, Rielly rest). | v1.0 |
| **Templates/MatchupTemplate_Default_RiellyActive_v1.0_Lock.json** | NHL | Locked Canon template baseline for rivalry and playoff games. | v1.0 |
| **Templates/README.md** | — | Explanation of matchup template logic and usage. | — |

---

### ⚙️ Update Procedure

1. **Export current in-game lines**  
   From NHL 25 → Team Management → Lines / Special Teams → Take screenshots or export JSONs.

2. **Regenerate the JSONs**  
   (use Architect or your Dynasty AI import scripts)  
   - NHL → `Architect/Lines/NHL/NHL_Lines_YYYY-MM-DD.json`  
   - AHL → `Architect/Lines/AHL/AHL_Lines_YYYY-MM-DD.json`

3. **Re-sync and lock inside Dynasty AI**
   ```bash
   /lines_import "Architect/Lines/NHL/NHL_Lines_YYYY-MM-DD.json"
   /lines_import "Architect/Lines/AHL/AHL_Lines_YYYY-MM-DD.json"
   /roster_guard set --mode strict \
     --nhl "Architect/Lines/NHL/NHL_Lines_YYYY-MM-DD.json" \
     --ahl "Architect/Lines/AHL/AHL_Lines_YYYY-MM-DD.json" \
     --contracts "Architect/Data/LeafsContracts_seed_v1.6.json"
   /qa_pre_game --focus "lines_schema,roster_guard,pp_one_timer_map"
   /dynasty_savepoint --tag "Lines_RosterContracts_Locked_vYYYY-MM-DD"