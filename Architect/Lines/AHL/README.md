# 🏒 AHL Lines – Toronto Marlies (Canon v4.1 · Updated Dec 7 2024)

This folder contains all active and historical **AHL line configurations** used by the Toronto Marlies under the Leafs Dynasty AI system.

---

### 📂 Files
| File | Purpose | Date |
|------|----------|------|
| AHL_Lines_2024-12-07.json | Even-strength lines, defensive pairs, goalies | Dec 7 2024 |
| AHL_SpecialTeams_2024-12-07.json | Power Play / Penalty Kill formations | Dec 7 2024 |

---

### ⚙️ Update Process
1. Capture in-game AHL lines and special teams screenshots.  
2. Regenerate JSONs via Architect (`/lines_export ahl`).  
3. Replace files in this folder with the same naming pattern:  
   `AHL_Lines_YYYY-MM-DD.json` and `AHL_SpecialTeams_YYYY-MM-DD.json`.  
4. Run inside Dynasty AI:
   ```bash
   /config verify source_map
   /qa_pre_game --focus "lines_sync,ahl_dev_gate"
   /dynasty_savepoint --tag "AHL_Lines_YYYY-MM-DD"
Maintained By: Austin Olsen  |  Canon v4.1  |  Architect v6.2