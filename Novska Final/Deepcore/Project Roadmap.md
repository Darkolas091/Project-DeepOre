---
sticker: emoji//1f5fa-fe0f
---

### **MILESTONE 1 – CORE FOUNDATION (Week 1–2)**

> Get the game loop running in a barebones prototype.

**1. Setup & Base Systems**

- Setup version control & backup (Git or manual ZIPs)
    
- Setup Log Manager & Bug Log sheet
    
- Create GameManager (scene flow)
    
- Create GridManager (generate 11×11 grid, handle tiles)
    
- Create OreTile data structure (type, score, states)
    
- Create ClickController (cursor + tile interaction)
    
- Create DwarfController (basic click feedback / animation trigger)
    
- Create ScoreManager (update & display points)
    
- Create RunManager (rounds, deadlines, basic progression)
    
- Hook up AudioManager with placeholders
    
- Add Save/Load basics (PlayerPrefs or JSON)
    
- Validate Save Data (fallback defaults if broken)
    

🟩 **Milestone Goal:** Clickable grid works, score updates, runs start & end properly.

---

### **MILESTONE 2 – GAMEPLAY MECHANICS (Week 3–4)**

> Add all mining logic, tile types, and round flow.

**2. Core Tile Behaviors**

- Implement Cracked Boulder logic (2-state reveal)
    
- Implement Endless Vein (regeneration & cap)
    
- Implement Dynamite Ore (AOE & chain handling)
    
- Implement Mushroom Cluster (spread rules)
    
- Implement Support Beam (skip shrink, durability)
    
- Implement optional hazards (gas, collapse)
    

**3. Funnel & Depth Mechanics**

- Create FunnelShrink system (reduce grid rows/cols per depth)
    
- Add collapse FX + camera pan when shrinking
    
- Add random variation per depth for organic feel
    

🟩 **Milestone Goal:** One full playable run from start to finish (no upgrades yet).

---

### **MILESTONE 3 – TEMPORARY UPGRADES (Week 5)**

> Add upgrade cards, reroll, and integration with gameplay.

**4. Run Upgrades System**

- Create UpgradeManager
    
- Define categories (score, spawn, crew, utility, chain)
    
- Add 10–15 upgrade cards with descriptions & balance numbers
    
- Implement card pool rules (rarity, reroll)
    
- Build Upgrade Card UI & reroll flow
    
- Implement floating popups, visual feedback for chosen upgrades
    

🟩 **Milestone Goal:** End of run → select upgrade → next round works.

---

### **MILESTONE 4 – META PROGRESSION (Week 6)**

> Add permanent unlocks and meta loop.

**5. MetaManager & Forge**

- Implement MetaManager (persistent data + upgrades)
    
- Add meta upgrade logic (reroll license, banish rune, etc.)
    
- Create pricing & scaling curve
    
- Implement save/load of meta progress
    
- Add simple UI for purchasing and applying unlocks
    
- Add safe data validation for meta save
    

🟩 **Milestone Goal:** After a run → Forge screen → buy upgrade → next run starts with changes.

---

### **MILESTONE 5 – POLISH SYSTEMS & USER EXPERIENCE (Week 7)**

> Clean visuals, usability, and feedback loops.

**6. UI & UX**

- Add tooltips for tiles (hover info)
    
- Improve highlight states & accessibility options
    
- Add First Run Guide / Onboarding popup
    
- Add Results screen (score, credits, upgrades)
    
- Add settings persistence (audio, fullscreen, language)
    

**7. Feedback Systems**

- Add camera shake (explosions)
    
- Add smooth transitions between depths
    
- Add combo counter feedback
    
- Add achievement tracker (optional)
    

🟩 **Milestone Goal:** Game feels complete and readable, playable start to finish.

---

### **MILESTONE 6 – STABILITY, TESTING & POLISH (Week 8–9)**

> Ensure it’s stable, smooth, and ready for build.

**8. Testing & Debug**

- Build developer debug UI (spawn ore, skip depth, etc.)
    
- Add performance profiling pass
    
- Add object pooling
    
- Add early exit handling (abort run safely)
    
- Run full QA checklist with bug log tracking
    

**9. Final Polish**

- Tune spawn rates & score balance in config file
    
- Add localization hooks
    
- Add final SFX & sound mix
    
- Verify save/load stability across sessions
    
- Build & test release version
    

🟩 **Milestone Goal:** Fully functional, balanced, and stable build.

---

### **MILESTONE 7 – DEPLOY & WRAP-UP (Week 10)**

> Final deployment, submission, and presentation prep.

**10. Build & Deploy**

- Create final build
    
- Test across resolutions
    
- Record footage or screenshots for showcase
    
- Backup all project files