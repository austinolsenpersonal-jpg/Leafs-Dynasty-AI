# Leafs Dynasty AI — Product Folder

Status: **Active workspace** for Austin’s Toronto Maple Leafs Franchise (NHL 25, Series X|S via Cloud on Xbox One S).  
This folder is the **single source of truth** for new Leafs Dynasty AI chats.

---

## 1. What this folder is for

The `Product` folder replaces old “chat memory” with **stable files**.

Any *new* Leafs Dynasty AI chat should load its state from here instead of relying on past conversations.

Core goals:

- Keep systems, sliders, and strategies **canon-accurate**.
- Let any new chat **rebuild everything** with a single bootstrap command.
- Avoid losing work when a chat history fills up.

---

## 2. Key files

### 2.1 Master Bootstrap

- **File:**  
  `Architect/Config/Leafs_Dynasty_MasterBootstrap_v1.0.json`

**Purpose:**  
Defines the entire Leafs Dynasty environment:

- Canon version, Architect version, PatchSuite version  
- Current NHL & AHL lines file paths  
- Slider rules (0–10 scale, trap 0–6)  
- Gameplay defaults (systems, PP/PK base, breakouts)  
- Active modules (CapFlex, DevPulse, Trade/Contract/Deadline, Opponent Memory, Energy Model, etc.)  
- Automation rules (DailyOps, Auto-Heal, Modules Auto-Verify)  
- Trade & roster philosophy  
- Goalie rotation and B2B logic  
- Matchup & gameplan output behaviour  
- Alerts & guardrails

Use this when starting any new Leafs Dynasty AI chat.

---

### 2.2 Full Export (Season Snapshot)

- **File:**  
  `Architect/Exports/LeafsDynasty_FullExport_v1.0.json`

**Purpose:**  
A heavier snapshot that includes:

- Lines + sliders + systems  
- Opponent Memory data  
- Gameplan behaviour  
- Module settings  
- Trade history (Foerster trade, etc.)  
- Extra context for deeper analysis

Use this if you want **maximum continuity** with previous seasons / chats.

---

## 3. How to start a NEW Leafs Dynasty AI chat

When you open a fresh Leafs Dynasty AI GPT:

1. Paste this command:

   ```text
   /dynasty_bootstrap --config "Architect/Config/Leafs_Dynasty_MasterBootstrap_v1.0.json" --mode full --sync true