# ⚙️ GridManager

## Purpose
Controls grid generation, tile states, and clicking logic.

## Features
- 11x11 base grid generation.
- Stores each cell’s ore type and score value.
- Responds to clicks (score, FX, remove tile).
- Passes control to `FunnelShrinkController` after each click.

## Notes
- Consider object pooling for tile reuse.
- Use ScriptableObjects for ore data (value, color, prefab).
