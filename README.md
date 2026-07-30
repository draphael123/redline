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
| Pause / resume | `P` or `Escape` |

The game also pauses automatically when its window loses focus.

The opening menu includes persistent flight settings for sound, camera shake, glow effects, screen flashes, particle density, render quality, and HUD brightness.

Combat readability is reinforced with distance-scaled enemy brackets, visible attack-charge warnings, damage health bars, Warden warning frames, and high-contrast hostile projectiles.
Environmental debris stays outside the central combat corridor and uses muted rust tones, leaving bright red-white motion exclusively for hostile attacks.

The finished presentation uses protected cockpit-style HUD panels, a dedicated Warden integrity display, soft layered solar particles, controlled bloom and exposure, responsive layouts, and a shared solar-aperture language across title, pause, and failure states.

Multi-part procedural models give the player swept wings, armor, engine pods, intakes, and gun housings; enemy archetypes use distinct interceptor, bomber, turret, and shield chassis; and Wardens feature themed pylons with independently rotating armor rings.

## Structure
Each sector contains three named levels of escalating waves — darters, orb-lobbing bombers, debris turrets, and shielded elites — followed by a themed **Warden** boss. Clear a sector, patch a hull point, and push into the next region.

The campaign arc moves through **Ember Reach**, **Grave Orbit**, **Helioforge Array**, **Corona Scar**, and **Core Threshold**. Each region has its own three-level scenery progression, atmosphere, and Warden palette.

## Tech
Single-file [Three.js](https://threejs.org/) (r161) with `UnrealBloomPass`. No build step — open `index.html` or serve statically.

Debug hook: `window.__redline` (`.state`, `.god`, `.sim(sec)`, `.killAll()`).

## Run locally
```bash
python -m http.server 5793
# open http://localhost:5793
```
