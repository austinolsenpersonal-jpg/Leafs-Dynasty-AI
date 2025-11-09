# 🧭 Promotion Policy — AHL ➜ NHL (Leafs Dynasty)
**Environment:** Architect v6.2 • Canon v4.1 • DevPulse v2.0 • PromotionThresholds v1.1  

This document defines how AHL → NHL promotion readiness is evaluated, exported, and committed so decisions stay traceable and consistent.

---

## 🎯 Objective
Provide clear 21-day windows for safe call-ups that respect:
- Readiness (DevPulse v2.0 score)  
- CapFlex forecast (≥ $0.50 M buffer or paper-down path)  
- Roster fit (role/handedness, PK/PP utility)  
- Morale / Chemistry impact (avoid unnecessary churn)

---

## 📦 Standard Outputs
Each run of `PromotionThresholds v1.1` exports both:

- `PromotionThresholds_latest.json` (machine data)  
- `PromotionThresholds_latest.md` (human summary)

**File paths**
```
Architect/Reports/Promotion/PromotionThresholds_latest.json  
Architect/Reports/Promotion/PromotionThresholds_latest.md
```

**Optional archive (dated history)**
```
Architect/Reports/Promotion/Archive/PromotionThresholds_YYYY-MM-DD.json  
Architect/Reports/Promotion/Archive/PromotionThresholds_YYYY-MM-DD.md
```

---

## 🧮 Readiness Scoring (v2.0)
| Range | Status | Action |
|:--|:--|:--|
| 0.85 – 1.00 | ✅ Green | Call-up viable if slot exists |
| 0.78 – 0.84 | 🟡 Yellow | Track · Re-evaluate in 7-10 days |
| < 0.78 | 🔴 Hold | Keep AHL usage / mentorship active |

**Modifiers**
- Mentor Link active  +0.02 – +0.05  
- Cap buffer < $0.50 M  −0.05  
- NHL vacancy detected  +0.03  

---

## 📋 Run Cadence
Run 2 – 3× weekly and after injuries or paper moves.

**Command block**
```
/enable_module M240_PromotionThresholds_v1.1 --mode monitor  
/promotion_check --team TOR --window "now->+21d" --export both  
/promotion_report --format md,json --out "Architect/Reports/Promotion/PromotionThresholds_latest"  
/dynasty_savepoint --tag "PromotionThresholds_v1.1_Run_$(DATE)"
```

---

## ✅ MD Summary Example
**Summary (Next 21 Days)**  
- Steeves — Status GREEN | Earliest call-up 2024-12-12 | Role L4 W  
- Niemelä — Status YELLOW | Earliest call-up 2024-12-20 | Role RD3  

**Cap & Roster**  
- Cap buffer $145 K (paper-down Yes)  
- SPC count 47 / 50  
- Injuries None  

**Actionables**  
- If RD injury → Call Niemelä (RD3 · pair with OEL)  
- If L4 wing opens → Call Steeves immediately (8-10 EV min)

---

## 🗃 Commit Policy
Commit both files together.

**Commit headline**
```
Dev: PromotionThresholds — latest readiness & 21-day call-up windows
```

**Commit description**
```
- Exported PromotionThresholds_latest.md/.json (DevPulse v2.0 + CapFlex integration)  
- Added readiness scores, earliest call-up dates, cap/SPC checks, and actionables  
- Savepoint: PromotionThresholds_v1.1_Run_$(DATE)
```

---

## 🔒 Governance
- Do **not** store caches or savepoints in repo.  
- Versioned under Canon v4.1 and automation-safe.