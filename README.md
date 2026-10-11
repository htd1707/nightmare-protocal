# Nightmare Protocol

A first-person survival horror game that runs in the browser, built with Three.js and the Web Audio API. Every texture, model, light, sound and piece of music is generated in code — there are no asset files.

## Play locally

It is a static site with no build step. Serve the folder with any static server, for example:

```
npx serve .
```

or open `index.html` directly. Three.js loads from cdnjs, so an internet connection is needed.

## Deploy

On Vercel, import this repository and keep the defaults: Framework Preset **Other**, no build command, output directory = repository root.

## Controls

| Key | Action |
| --- | --- |
| WASD | Move |
| Mouse | Look |
| Shift | Sprint |
| Ctrl or C | Crouch |
| E | Interact / hide |
| F | Flashlight |
| R | Swap batteries |
| Tab | Objective |
| Esc | Pause |

## Optional audio overrides

Put sound files in `audio/` and list them in `audio/manifest.json`, e.g. `{"stinger_hit": "hit.ogg", "chase": "chase.mp3"}`. Anything not listed uses the built-in synthesized sound.

## Project layout

- `index.html` — page, menus, HUD and styles
- `js/core.js` — settings, saving, timers, input
- `js/textures.js` — procedural PBR textures
- `js/level.js` — map, geometry, baked lighting, doors, collision
- `js/props.js` — furniture, machinery and light fixtures
- `js/player.js` — first-person controller and flashlight
- `js/creature.js` — The Patient and the mannequins
- `js/ai.js` — monster pathfinding and state machine
- `js/audio.js` — procedural sound and music
- `js/fx.js` — post-processing and particles
- `js/world.js` — items, puzzles, lockers, mirror, CCTV
- `js/scares.js` — scare director and scripted scares
- `js/ui.js` — interface
- `js/game.js` — game flow, story, checkpoints
