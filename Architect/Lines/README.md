# 🧩 Leafs Dynasty AI – Lines Directory (v6.0 Canon)

This directory contains all active and historical lineup JSONs for the Toronto Maple Leafs franchise.

---

## 🏒 Purpose
This folder serves as the **source of truth** for all line configurations used by the Leafs Dynasty AI (Architect v6.1 and later).  
It replaces the deprecated lowercase `/lines/` directory to eliminate roster drift between AHL and NHL sets.

---

## 📁 Structure
```
Architect/Lines/
├── NHL/
│   ├── NHL_Lines_2024-12-04.json        ← Active NHL lineup (post-Dumba trade)
│   └── (Archive)                        ← Older NHL line files for reference
│
├── AHL/
│   ├── AHL_Lines_2024-12-04.json        ← Active AHL lineup (Steeves–Abruzzese–Järnkrok top line)
│   └── (Archive)
│
└── README.md                            ← This file
```

---

## 🔒 Sync Rules
1. **This directory is locked under**  
   `/roster_guard --mode strict`
   - All live roster operations reference only these JSONs.  
   - Older lowercase `/lines/` folders are ignored.

2. **Each new lineup change must include**
   - Updated `NHL_Lines_YYYY-MM-DD.json` and/or `AHL_Lines_YYYY-MM-DD.json`
   - Version bump note in commit message (e.g., `v6.0 → v6.1`)

3. **Adaptive Strategy Compatibility**
   - Fully compatible with Adaptive Engine v6.0  
   - Strategy drift prevention handled by `template_guardrails` and `strategy_bounds`

---

## 🧩 Command Reference
```
/roster_guard set --mode strict \
  --nhl "Architect/Lines/NHL/NHL_Lines_2024-12-04.json" \
  --ahl "Architect/Lines/AHL/AHL_Lines_2024-12-04.json" \
  --contracts "Architect/Data/LeafsContracts_seed_v1.5.json"

/dynasty_savepoint --tag "RosterContracts_LinesLocked_StrategyAdaptive_v6.0"
```

---

## 🧠 Notes
- Capitalization matters — only `/Lines/` is valid.  
- Each JSON is validated automatically during `/qa_pre_game` or `/matchup`.  
- To archive older versions, move them into dated subfolders (e.g., `/Archive/Nov2024/`).

---

**Maintainer:** Austin Olsen  
**Project:** Leafs Dynasty AI  
**Version:** Canon v6.0  
**Last Updated:** December 4 2024