# Lines Lock – Canon v4.1

This folder stores the active line files Architect reads at startup.

- **NHL lines file:** `NHL_Lines_2024-11-28.json`
- **AHL lines file:** `AHL_Lines_2024-11-28.json`

## Structure
Each file contains:
- `forwards` – even strength forward lines  
- `defense` – defensive pairings  
- `pp` – power play units  
- `pk` – penalty kill units  
- `extras` – scratches, shootout, and special units  

## If Architect Flags a Missing Lines Error
1. Confirm both files exist with these exact names.  
2. Open `Architect_Config_v6.1.json` and verify the paths:
   ```json
   "paths": {
     "lines": {
       "nhl": "LeafsAI/Architect/lines/NHL_Lines_2024-11-28.json",
       "ahl": "LeafsAI/Architect/lines/AHL_Lines_2024-11-28.json"
     }
   }