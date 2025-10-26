![Validate JSON](https://github.com/austinolsenpersonal-jpg/Leafs-Dynasty-AI/actions/workflows/validate.yml/badge.svg)

# Leafs Dynasty AI

This repo tracks the **Canon** (locked baselines), **Roster/Contracts sync**, and **release bundles** for Austin Olsen’s NHL 25 Toronto Maple Leafs Dynasty AI.

---

## 📁 Project Structure

**Architect/**
- `Architect_Config_v6.1.json` – base instructions + Canon link  
- `OldGen_Strategy_Canon_v4.1.txt` – official strategy rulebook  

**LeafsAI/**
- `LeafsSeeds_Master_v4.1.json` – merged Seeds (GoaliePlan, PP, Scouting, Deadline, Finance, AHL Dev)  
- `LeafsRoster_master_v1.2.json` – active roster baseline  
- `LeafsContracts_seed_v1.1.json` – contracts + cap snapshot  
- `Finance_seed.json` – arena and promotion data  

---

## 🧭 Usage

- The **Architect GPT** builds and validates Canon files and Seeds.  
- The **Leafs Dynasty Suite AI** operates day-to-day franchise logic using Canon v4.1.  
- Run `/verify_strategies` after any roster or system change to maintain sync.

---

## 🏁 Current Baseline

**Season 1 Baseline (Oct 2025)**  
- Canon v4.1 Locked  
- Architect_Config v6.1 active  
- LeafsSeeds_Master v4.1 merged  
- Six total active files (under 10 limit)

---

## 🧾 Version History

| Version | Date | Changes |
|:--------:|:----:|:--------|
| **v4.1** | Oct 26 2025 | Merged Seeds, added Architect_Config v6.1, removed legacy Seeds & Link Config. |
| **v4.0** | Sep 2025 | Initial Canon release with separate Seeds structure. |
