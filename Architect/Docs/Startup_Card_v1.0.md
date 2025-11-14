# Leafs Dynasty AI – Startup Card v1.0

Owner: Austin Olsen  
Environment: Architect v6.2 • Canon v4.1 • NHL 25 (Series X|S via Cloud)  
Bootstrap: `Architect/Exports/LeafsDynasty_FullExport_v1.0.json`

---

## 1. NEW CHAT STARTUP

When you open a NEW Leafs Dynasty AI chat:

Step 1 — Tell it what it is:
“You are my Leafs Dynasty AI for NHL 25. Use my Architect export. Do not guess labels.”

Step 2 — Paste this bootstrap command:

```
/dynasty_bootstrap --config "Architect/Exports/LeafsDynasty_FullExport_v1.0.json" --mode full
```

Step 3 — Confirm it loads:
- Canon v4.1  
- Architect v6.2  
- Opponent Memory v2.0  
- DailyOps running  
- Commit prefix = create  

If anything is missing:
“Reload from LeafsDynasty_FullExport_v1.0.json and re-sync everything.”

---

## 2. EARLY HEALTH CHECKS (NEW CHAT)

Run these to ensure the system is synced:

**Watchdog**
```
Run /watchdog scan --config 'Architect/Config/ModuleWatchdog_v1.0.json' --output 'latest' and notify me if any drift is detected.
```

**DailyOps Verify**
```
Run /ops_verify --target 'DailyOps Summary' --window '24h' --retry 1 and notify me of any failure or missing commit.
```

**Matchup QA**
```
/matchup_qa run --config "Architect/Config/MatchupQA_v1.3.json" --latest --verbose
```

If anything fails:
“Auto-heal whatever you can and show me what you fixed.”

---

## 3. HOW TO REQUEST A FULL MATCHUP

Example:
```
Full matchup vs WPG with current exported lines and slider rules. Starter: Stolarz. Show line sliders, D sliders, PP/PK, bench card, toggles.
```

Dynasty AI must use:
- Canon v4.1  
- EA-correct slider directions  
- Files from the export (no guessing)

---

## 4. WHEN YOU UPDATE LINES

If your in-game lines change:

Tell Dynasty AI:
```
My latest NHL lines are in Architect/Lines/NHL/Post_Foerster_Lines_2024-12-12.json and my AHL lines are in Architect/Lines/AHL/AHL_Lines_2024-12-10.json. Re-sync and confirm.
```

Then run:
```
/matchup_qa run --config "Architect/Config/MatchupQA_v1.3.json" --latest --verbose
```

---

## 5. GITHUB OUTPUT RULES

Dynasty AI must ALWAYS output files in this order:

1. **File path block**  
2. **Full file contents block**  
3. **Commit headline block (must start with “create”)**  
4. **Commit description block (2–4 lines, mobile-safe)**  

If it fails:
“Use my GitHub iPhone format.”

---

## 6. QUICK RECOVERY COMMAND

If a new chat seems confused:
```
Use Architect/Exports/LeafsDynasty_FullExport_v1.0.json as the single source of truth. Reload all systems, lines, sliders, modules, and automations from that file and confirm when fully synced.
```

---

## 7. PIN THIS CARD

This is your one-screen reset for ANY future Leafs Dynasty AI chat.