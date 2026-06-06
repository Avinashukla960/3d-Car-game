# 🚗 3D Car Game

A browser-based 3D driving game built with **Three.js** — no build tools, no dependencies, just open and play.

Drive around a sprawling open world, dodge pedestrians, crash into trees, and try to outrun a giant chaser NPC hunting you down.

---

## 🎮 Demo

Open `index.html` in any modern browser to play instantly.

---

## Features
- **3D open world** with a 500×500 unit grassy map, fog, and dynamic shadows
- **Realistic-ish car physics** — acceleration, friction, reverse, and speed-sensitive steering
- **Animated lights** — headlights glow when accelerating, brake lights when slowing, reverse lights when backing up
- **Pedestrian NPCs** — 50 wandering people that tumble when you hit them
- **Tree obstacles** — 150 procedurally placed trees with randomized sizes; hitting one bounces you back
- **Giant Chaser NPC** — a 10× scaled pursuer who wanders peacefully until you bump into her, then relentlessly hunts you down
- **Smooth follow camera** with lerped position for a cinematic feel
- **Dynamic shadows** that follow the car so they stay sharp

---

## Controls

| Key | Action |
|-----|--------|
| `↑` Arrow Up | Accelerate |
| `↓` Arrow Down | Brake / Reverse |
| `←` Arrow Left | Steer left |
| `→` Arrow Right | Steer right |

---

## Getting Started

No installation or build step needed.

```bash
git clone https://github.com/your-username/3d-car-game.git
cd 3d-car-game
```
Then just open `index.html` in your browser:

```bash
# macOS
open index.html
# Linux
xdg-open index.html
