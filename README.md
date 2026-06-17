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

# Windows
start index.html
```

Or serve it locally if you prefer:

```bash
npx serve .
# then visit http://localhost:3000
```

---

## Project Structure

```
3d-car-game/
└── index.html      # Everything — game logic, rendering, NPCs, all in one file
```
The entire game lives in a single HTML file. Three.js is loaded via CDN (`r128`).

---

## Tech Stack
- [Three.js r128](https://threejs.org/) — 3D rendering
- Vanilla JavaScript (ES Modules)
- No frameworks, no bundler, no install
---

## How It Works

| System | Details |
|--------|---------|
| **Rendering** | `WebGLRenderer` with PCF soft shadow maps |
| **Car physics** | Velocity + friction model; speed-sensitive steering with turn damping |
| **Collision** | Circle-based collision using per-object `collisionRadius` |
| **NPCs** | State-machine AI — wander → chase on contact (chaser); walk → fall on contact (pedestrians) |
| **Camera** | Offset vector rotated by car's world matrix, lerped each frame |
| **Lights** | Material `emissiveIntensity` toggled based on car state |
---

## Possible Improvements

- [ ] Mobile touch / joystick controls
- [ ] Score counter (pedestrians hit, distance driven)
- [ ] Sound effects and engine audio
- [ ] Road network and buildings
- [ ] Multiple chasers scaling in difficulty
- [ ] Minimap


---

## License

MIT — do whatever you want with it.
