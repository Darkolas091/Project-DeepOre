latform:** PC (Windows)  
**Engine:** Unity  
**Team:**  
- 👨‍💻 Programmer: Donnie 
- 🎨 Artist: Vermilion
**Duration:** 2 Months (6 Weeks Dev + 2 Weeks Polish)

---

## 🎯 High Concept
**Deepcore** is a roguelike mining game where every click takes you deeper into the earth.  
You play as a dwarven miner striking through layers of rock to uncover precious ores and earn points.  
Each click causes the mine to collapse in a **funnel shape**, forcing you to dig strategically.  
Meet score deadlines to earn **upgrade cards** that change your strategy every run, and use your total haul to unlock **meta upgrades** for future expeditions.

---

## 🪓 Core Gameplay Loop
1. **Start Run**
   - Begin on an **11×11 grid** of ore tiles.
   - Each tile has a type and score value.
2. **Click to Mine**
   - Click a tile → earn its score.
   - After each click, the mine **shrinks downwards** (funnel shape).
3. **Depth Progression**
   - The playable area narrows, representing descent.
   - Camera pans downward slightly each shrink.
4. **Deadline Check**
   - Meet score target → pick 1 of 3 upgrades.
   - Fail → run ends.
5. **Meta Progression**
   - Earn gold nuggets based on total score.
   - Spend nuggets on permanent unlocks (rerolls, maps, bonuses).

---

## ⛏️ Core Mechanics

### ⚙️ Mining & Funnel Shrink
- Grid: 11×11 base → shrinks to a 1×1 core.
- Shrink removes:
  - 2 rows from the top
  - 1 column from each side
- Visual effect: looks like a **descending mine shaft**.
- Random offset adds natural variation.
- Each shrink level = new “depth layer” with unique visuals and ores.

---

### 💎 Ores & Scoring

| Tier | Ore | Points | Rarity | Description |
|------|------|--------|---------|-------------|
| 1 | Stone | 1 | Common | Plain gray rock |
| 2 | Copper | 3 | Common | Warm orange metal |
| 3 | Iron | 5 | Uncommon | Cool metallic blue |
| 4 | Gold | 8 | Rare | Bright yellow sparkle |
| 5 | Ruby | 10 | Very Rare | Deep red gem |
| 6 | Diamond | 15 | Legendary | Blue-white crystal |

**Optional Special Tiles**
- 💣 **Explosive Ore:** Breaks nearby tiles.
- 🗿 **Relic:** Random buff or curse.
- 🪨 **Dirt/Empty:** Non-clickable cell after collapse.

---

### 🃏 Upgrades (In-Run)
Each score milestone gives 1 of 3 upgrade cards to pick from.

| Type    | Name                   | Effect                               |
| ------- | ---------------------- | ------------------------------------ |
| Score   | **Refined Technique**  | +25% points from Iron+ ores          |
| Utility | **Reinforced Pickaxe** | Reduces next shrink step             |
| Chance  | **Vein Sense**         | +10% chance for high-tier ores       |
| Chain   | **Explosive Charge**   | Every 3rd click mines adjacent cells |
| Wild    | **Prospector’s Luck**  | Next layer starts with 1 gold ore    |

*Short flavor text example:*  
> “The old pick still hums with runic power.”

---

### 🪙 Meta Progression
**Currency:** Gold Nuggets (earned from total score)

| Unlock | Description |
|---------|-------------|
| 🌀 **Reroll Permit** | Reroll upgrade choices once per run |
| 🧱 **Banish License** | Remove one upgrade type from pool |
| 🗺️ **Tunnel Map** | Unlocks alternate mine layouts (blocked cells) |
| ⚒️ **Gear Tier I** | Start runs with +5% score multiplier |
| 💰 **Guild Membership** | +10% gold nuggets earned per run |

Persistent unlocks saved via JSON file or PlayerPrefs.

---

## 🌌 Depth Progression

| Depth | Visual Theme | Ore Pool | Ambience |
|-------|---------------|-----------|-----------|
| Surface | Light rocks, roots | Stone, Copper | Bright daylight |
| Shallow | Dimmer stone | Iron, Coal | Dripping water |
| Mid | Warm glow | Gold, Ruby | Lantern flicker |
| Deep Core | Dark magma | Ruby, Diamond | Rumbles, sparks |
| Heart of Mountain | Glowing stone | Ancient Core | Deep echoing music |

Each layer darkens the lighting and shifts palette to emphasize depth.

---

## 💥 Feedback & FX
- **Pickaxe Cursor:** Animated swing when clicking.
- **Click FX:** Dust puff + spark particles + score popup.
- **Collapse FX:** Camera shake + falling debris.
- **Depth Transition:** Lighting change + darkening fog.
- **Upgrade Selection:** Hammer impact + metallic ring sound.

---

## 🧱 Technical Systems

| System | Purpose |
|---------|----------|
| `GridManager` | Handles grid generation & tile states |
| `TileController` | Manages ore data & click FX |
| `FunnelShrinkController` | Removes rows/columns per click |
| `ScoreManager` | Tracks points & deadlines |
| `UpgradeManager` | Applies upgrade ScriptableObjects |
| `MetaManager` | Stores unlocks & meta-currency |
| `UIManager` | Displays score, cards, menus |
| `FXManager` | Centralizes visual & sound effects |
| `SaveSystem` | JSON serialization for persistent data |

---

## 🎨 Art Direction

### Style: **Low Poly Dwarven Fantasy**
- Chunky forms, glowing ores, warm lantern light.  
- Readable from top-down camera.
- Focus on material color & lighting contrast.
- Use stylized shaders (rim light or toon).

**References:**  
*Deep Rock Galactic*, *Dome Keeper*, *For The King.*

### Asset Checklist
#### Environment
- [ ] Stone / Copper / Iron / Gold / Ruby / Diamond ores  
- [ ] Dirt & collapsed rubble tiles  
- [ ] Background cave layers  
- [ ] Depth-based lighting gradients  

#### UI
- [ ] Pickaxe cursor animation  
- [ ] Upgrade card icons (15–20 total)  
- [ ] Dwarven-style frames, menus, and runes  
- [ ] Font: stone-carved or medieval  

#### FX
- [ ] Dust puff particles  
- [ ] Ore sparkle burst  
- [ ] Collapse debris  
- [ ] Depth transition fade  

---

## 🔊 Audio Plan
| Event | Sound |
|--------|--------|
| Click | Metallic “clink” (varied per ore) |
| Collapse | Low rumble & falling rocks |
| Upgrade | Forge hammer hit |
| Depth Transition | Rumble + chord hit |
| Background | Subtle cave ambience & pick sounds |

---

## 📆 Development Timeline

| Week | Goals |
|------|--------|
| 1 | Grid + tile mining prototype |
| 2 | Funnel shrink + camera movement |
| 3 | Scoring + upgrade system |
| 4 | Meta system + save/load |
| 5 | Art integration + pickaxe cursor |
| 6 | Balancing + depth transitions |
| 7 | SFX + polish |
| 8 | Final fixes + build |

---

## 🧩 Stretch Goals
- Alternate mine maps (L-shape, blocked tiles)
- Special relic events (bonus/curses)
- Daily challenge mode
- Steam achievements
- Animated dwarf companion HUD

---

## 💾 Save Data Example
```json
{
  "meta": {
    "rerollUnlocked": true,
    "banishUnlocked": false,
    "mapsUnlocked": 1,
    "gearLevel": 2
  },
  "stats": {
    "highestScore": 4820,
    "totalGoldNuggets": 900
  }
}
```

---
## 🪨 Summary

**Deepcore: The Dwarven Descent** is a focused roguelike mining experience built around a unique funnel-shrinking mechanic.  
It combines strategic resource management with procedural upgrades and satisfying visual feedback.  
Designed for a 2-person team over 2 months, it showcases both technical design and art direction in a cohesive, polished project.

