# 📊 Architect Daily Ops Reports

This directory contains the **daily automated operation summaries** for the Leafs Dynasty Architect system.  
Each report is generated and committed automatically by the `/dailyops generate` process.

---

### 📂 Folder Structure
| File | Purpose |
|------|----------|
| **INDEX.md** | Master list of all DailyOps reports |
| **Architect_DailyOps_YYYY-MM-DD.json** | Machine-readable structured report |
| **Architect_DailyOps_YYYY-MM-DD.md** | Human-readable Markdown summary |

---

### 🔄 Automation Details
- All commits use the tag: **Architect Daily Ops Summary**
- Generated once every day (or on manual `/dailyops generate`)
- Mirrors JSON → Markdown, and updates both `INDEX.md` and the repo’s main README banner.

---

### 🧩 Example Report Cycle
1. `/repo_guard temp_unlock --duration "10m"`  
2. `/dailyops generate --force --mirror md --overwrite true --update_readme true --update_index true`  
3. `/ops_verify --target "DailyOps Summary" --window "24h" --retry 1`  

---

_Last updated automatically by Architect GPT (v6.2) — Canon v4.1 — PatchSuite v1.6.0_