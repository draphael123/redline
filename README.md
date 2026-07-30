# REDLINE

*Don't cook your guns.*

A 3rd-person, on-rails arcade space shooter. Fly deeper toward a swollen red sun, blasting waves of enemy fighters — but your gun has no ammo, only **heat**.

## The hook
- Hold fire and your guns climb toward the **redline**. Cook them fully and you **overheat** — locked out and defenseless for a scary second.
- So you **vent** (`Space`): a cyan shockwave that clears nearby enemy bullets and staggers foes.
- Vent while your heat is *in the redline* for an **overcharged perfect vent** — a bigger, screen-shaking blast.

Offense and defense share one gauge. Every fight is a tension-and-release rhythm on the edge of the redline.

## Controls
| Action | Keys |
|---|---|
| Steer | `W` `A` `S` `D` / arrows |
| Fire | hold `J` or click |
| Vent | `Space` |
| Barrel roll | `K` or the HUD control |
| Lock target | `L` or the HUD control |
| Pause / resume | `P` or `Escape` |

The game also pauses automatically when its window loses focus.

The opening menu includes persistent flight settings for master audio, separate music and effects volume, camera shake, glow effects, screen flashes, particle density, render quality, and HUD brightness.

First-time pilots enter a guided, playable training flight. Six verified objectives teach steering, firing, heat buildup, perfect-vent timing, barrel rolls, lock-on, and hostile attack telegraphs before handing control directly into the campaign. Training can be skipped and replayed from the title screen; completion is saved locally.

Combat readability is reinforced with distance-scaled enemy brackets, visible attack-charge warnings, damage health bars, Warden warning frames, and high-contrast hostile projectiles.
Environmental debris stays outside the central combat corridor and uses muted rust tones, leaving bright red-white motion exclusively for hostile attacks.

The finished presentation uses protected cockpit-style HUD panels, a dedicated Warden integrity display, soft layered solar particles, controlled bloom and exposure, responsive layouts, and a shared solar-aperture language across title, pause, and failure states.

Multi-part procedural models give the player swept wings, armor, engine pods, intakes, and gun housings; enemy archetypes use distinct interceptor, bomber, turret, and shield chassis; and Wardens feature themed pylons with independently rotating armor rings.

## Structure
Each sector contains three named levels and nine authored encounters—three per level—followed by a themed **Warden** boss, including a guaranteed Warden at the end of Ember Reach. The outer approach emphasizes mobile interceptors and asteroid hazards, the fortified interior adds bombers, gun platforms, and structural debris, and the Warden threshold fields elite shield formations around moving gate blades.

REDLINE uses permanent ship progression rather than temporary roguelike upgrades. The ship editor fits a reactor, wing frame, and drive; installed parts persist and change damage, cooling, heat efficiency, speed, vent strength, roll recovery, and hull capacity. A persistent level selector unlocks each of the campaign's 15 stages as it is reached.

Level clears now provide route briefings without temporary rewards. Later levels add tougher enemies, distinct obstacle families, larger landmarks, cinematic entrances, visible damage sparks, articulated enemy components, and physical armor wreckage.

The campaign arc moves through **Ember Reach**, **Grave Orbit**, **Helioforge Array**, **Corona Scar**, and **Core Threshold**. Each region has its own three-level scenery progression, atmosphere, and Warden palette.

All 15 levels have their own environment kit. Within a sector, the approach, interior, and Warden threshold use different silhouettes, landmarks, fog, exposure, particle density, movement speed, obstacle materials, and lighting accents. Examples include Ember Reach's beacon field, dead signal forest, and furnace gate; Grave Orbit's convoy, carrier ribs, and tomb ring; and Helioforge's mirrors, coolant pipes, and foundry crown. Environmental contrast remains below hostile attack contrast to preserve combat readability.

Clearing Core Threshold ends the 15-level campaign with a dedicated completion state rather than recycling the final sector.

Each sector also has its own looping score: open ambience in Ember Reach, ominous drift through Grave Orbit, an industrial pulse in Helioforge Array, urgent momentum in Corona Scar, and a dark transmission motif at Core Threshold. The title screen, transitions, combat, vents, impacts, bosses, and sector clears have dedicated audio cues.

## Audio credits

- Music and UI cues: [Dark Sci-Fi Audio Pack by SRG774](https://opengameart.org/content/dark-sci-fi-audio-pack), released under CC0 1.0.
- Combat and system effects: [Sci-Fi Sounds by Kenney](https://opengameart.org/content/sci-fi-sounds), released under CC0 1.0.

Attribution is not required by either license, but the creators deserve the credit.

## Tech
Single-file [Three.js](https://threejs.org/) (r161) with `UnrealBloomPass`. No build step — open `index.html` or serve statically.

Debug hook: `window.__redline` (`.state`, `.god`, `.sim(sec)`, `.killAll()`).

## Run locally
```bash
python -m http.server 5793
# open http://localhost:5793
```
