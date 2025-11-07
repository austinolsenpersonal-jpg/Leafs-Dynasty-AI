# 🏒 NHL Lines – Toronto Maple Leafs (Canon v4.1 · Updated Dec 7 2024)

This folder stores all **NHL line and special-teams configurations** for the Toronto Maple Leafs under the Leafs Dynasty AI environment.

---

### 📂 Files
| File | Purpose | Date |
|------|----------|------|
| NHL_Lines_2024-12-07.json | Even-strength lines + defensive pairs + goalies | Dec 7 2024 |
| NHL_SpecialTeams_2024-12-07.json | Power Play and Penalty Kill formations | Dec 7 2024 |

---

### ⚙️ Update Process
1. Capture in-game NHL lines and special teams.  
2. Regenerate and replace the two JSONs above with new dates.  
3. Re-link in `Architect/Config/source_map.json`.  
4. Run the following commands:

/config verify source_map  
/qa_pre_game --focus "lines_sync,pp_one_timer_map"  
/dynasty_savepoint --tag "NHL_Lines_YYYY-MM-DD"

---

**Maintained By:** Austin Olsen | Canon v4.1 | Architect v6.2