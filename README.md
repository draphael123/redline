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

## Structure
Sectors of escalating waves — darters, orb-lobbing bombers, debris turrets, and shielded elites — each capped by a **Warden** boss. Clear a sector, patch a hull point, push deeper. Chase the high score.

## Tech
Single-file [Three.js](https://threejs.org/) (r161) with `UnrealBloomPass`. No build step — open `index.html` or serve statically.

Debug hook: `window.__redline` (`.state`, `.god`, `.sim(sec)`, `.killAll()`).

## Run locally
```bash
python -m http.server 5793
# open http://localhost:5793
```
