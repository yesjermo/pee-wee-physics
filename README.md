<div align="center">

<a href="https://yesjermo.github.io/pee-wee-physics/?splash"><img src="assets/splash.svg" alt="pee-wee-physics splash: click to enter" width="100%"></a>

<sub>▲ click the board to enter: the splash plays, then the simulator</sub>

# 💛 pee-wee-physics 💛
### HydroSim 3D: the world's most over-engineered pee simulator

*Real-time bladder physics. Procedural pee acoustics. Spatial audio. Nobody asked for this.*

[![Play it now](https://img.shields.io/badge/▶_PLAY-splash_→_simulator-f5c14b?style=for-the-badge)](https://yesjermo.github.io/pee-wee-physics/?splash)
[![Simulator](https://img.shields.io/badge/skip_the_intro-straight_to_the_toilet-4fd6e8?style=for-the-badge)](https://yesjermo.github.io/pee-wee-physics/simulator.html)

![Blender](https://img.shields.io/badge/Blender-modelling-F5792A?logo=blender&logoColor=white)
![Three.js](https://img.shields.io/badge/three.js-r160-000000?logo=threedotjs&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES_modules-F7DF1E?logo=javascript&logoColor=black)
![Web Audio API](https://img.shields.io/badge/Web_Audio-100%25_synthesized-4fd6e8)
![WebGL](https://img.shields.io/badge/WebGL-2.0-990000?logo=webgl&logoColor=white)
![Build](https://img.shields.io/badge/build_step-none,_just_vibes-success)
![Dependencies](https://img.shields.io/badge/npm_install-not_required-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)

![Hydration](https://img.shields.io/badge/hydration-optimal-f6f1c2)
![Pee reviewed](https://img.shields.io/badge/pee_reviewed-✓_approved-f0b84a)
![Stream pressure](https://img.shields.io/badge/stream_pressure-24_mL%2Fs-f5c14b)
![Bladder](https://img.shields.io/badge/bladder-500_mL_capacity-orange)
![Flush status](https://img.shields.io/badge/flush_status-PLEASE-ff5d6c)
![Toilet](https://img.shields.io/badge/toilet-rendered_in_4K_feelings-white)
![Pee ball](https://img.shields.io/badge/pee_ball_mode-unlocked-yellow)
![Aim](https://img.shields.io/badge/aim-better_than_your_roommate-blueviolet)
![Splash zone](https://img.shields.io/badge/splash_zone-you-red)
![Seat](https://img.shields.io/badge/toilet_seat-left_up_(sorry)-lightgrey)
![Tests](https://img.shields.io/badge/tests-0_passed,_0_failed,_1_flooded-orange)
![Uptime](https://img.shields.io/badge/stream_uptime-until_empty-success)

</div>

---

> *"I spent 40 hours building procedural urine acoustics with HRTF spatialization so you can hear exactly which side of the bowl you missed."*
> — the developer, probably dehydrated

> *"10/10 would void again."* — my bladder

> *"Why is the porcelain stain shader better than my company's entire frontend?"* — a concerned senior engineer

> *"Mom said it's my turn on the toilet simulator."* — a kid in 2026

> *"I asked for a physics engine and they gave me Newtonian urine. Still a physics engine. Technically."* — a game dev, staring into the void

> *"Finally, a simulator where missing the bowl has consequences."* — the bathroom floor

> *"The trajectory preview is the most useful thing I've seen this year and I hate that."* — someone who just learned what a parabola is

---

## 🤔 What is this

A single-file, no-build, browser-only **3D hydration + bladder physics + liquid audio simulator**, written in vanilla Three.js and the Web Audio API.

It started as a serious educational demo about hydration and urine color.
Then feature creep happened. Now there's a slime target range and you can turn into a sentient ball of pee.

**No audio files. No npm. No regrets.** (Some regrets.)

## ✨ Features nobody needed but everybody deserves

### 🚽 Physics & physiology
- **Bladder model:** kidneys fill it based on hydration and diuretics. Pressure drives flow (peaks around a realistic ~24 mL/s) and exit velocity.
- **Ballistic particle stream** with sub-frame emission, splash droplets, ripples and floor puddles that **stay where they land**, grow, take your pee color and slowly dry up
- **Toilet bowl fills up.** Don't flush and it **overflows**, floods the bathroom, and the flood **dissolves you** into a pee ball. Actions have consequences.
- **Porcelain stains** take on your current pee color. Flush to clean ~65%, or mop & scrub to clean all of it.
- **Stream control:** aim angle, power (distance), timed duration, a trajectory preview and predicted range

### 🎨 Color science (the actually educational part)
15 foods & drinks, each changing hydration, fill rate and color:

| You consumed | Your stream says |
|---|---|
| 💧 Water / 🍉 Watermelon | Pale & proud |
| ☕ Coffee / 🍺 Beer | Speedrun mode (diuretic) |
| ⚡ Energy drink / 💊 B-vitamins | **NEON YELLOW.** Visible from space. |
| 🔴 Beetroot / 🫐 Blackberries | Pink. Don't panic. (Beeturia is harmless.) |
| 🥕 Carrots | Orange |
| 🍬 Blue candy | Green-blue (yes, really) |
| 🫘 Fava beans | Brown (if you didn't eat these, see a doctor) |
| 🍟 Salty fries / 🍜 Ramen | Dehydrated & concentrated |

### 🔊 Procedural audio, 0 bytes of samples
- **Stream hiss:** pink noise goes through a band-pass filter, swept by a slow LFO. Pitch, brightness and volume all scale with bladder pressure.
- **Impact voices**, triggered by **actual particle collisions**:
  - **Ceramic tap:** a resonant triangle "tink"
  - **Water plink:** a bubble sine with rising pitch
  - **Tile patter:** filtered noise bursts
  - **Campfire sizzle:** a high-passed hiss
- **HRTF spatial audio:** orbit the camera and the stream pans around your head. Truly immersive. Unfortunately.

### 🧍 Characters
- A rigged, animated human with a **pixel-mosaic censor** (we're classy here)
- **Figures:** **skeleton man** (every male version: a ghost-glass body with skull, ribcage, spine, pelvis and limb bones following every animation, kidneys and bladder inside, pixel censor) · female (sitting on the toilet, her own textures) · or load your own `.glb` (it becomes a skeleton too)
- **Poses:** idle, sad slump, sneaky crouch, nodding, head shake, walk, run
- **Expressions** for the beagle and the fountain statue: auto (reacts to what's happening), neutral, happy, relieved, surprised, angry, strained, embarrassed. The beagle uses ears, eyelids, brows, tongue and tail; the bronze statue uses eyelids, brows and five mouth shapes.
- **Each figure eats different things:** humans get the drinks-and-pigments menu, the beagle gets dog food and water bowls (and refuses chocolate and grapes, which are toxic to dogs), and the fountain gets mains water, rain, festival beer, coin wishes and dye pranks.
- 🐶 **Beagle:** tricolour coat, floppy ears, wagging white-tipped tail. **Lifts a hind leg** when it goes, tongue out when it's desperate. The camera presets shrink to dog height.
- ⛲ **Brussels fountain statue:** a chubby bronze toddler (big round head, full cheeks, short dimpled arms and legs) on a stone pedestal over a fountain basin, always dressed in a red smock with gold trim. The water leaves a fountain spout, and the basin slowly takes on the colour.
- **11 skins** for the standing figure: 💀 X-ray skeleton · 🧊 glass (bones inside) · 🪩 liquid chrome · 🏆 gold statue · 🏛️ marble statue · 🏺 terracotta clay · 🎨 cel-shaded toon · 🛰️ hologram (scanlines + rim glow) · ⚡ neon rim glow · 🟢 slime jelly (bones inside) · 🌋 molten lava with glowing cracks. Pick one in **Character → Skin**, or link straight to one with `?skin=chrome`.

### 🎬 Rendering
- **Render quality** setting: *Fast* (plain), *High* (default: HDR pipeline, 4× MSAA, bloom, lens vignette, film grain and subtle chromatic aberration) or *Ultra* (+ GTAO ambient occlusion). Phones default to *Fast*. Link with `?quality=ultra`.
- Built entirely from three.js add-ons: `EffectComposer`, `UnrealBloomPass`, `GTAOPass`, `ShaderPass`, `OutputPass`, `RoomEnvironment` image-based lighting, plus a Fresnel rim-glow shader patch for the glowing skins
- Bloom is tuned per scene (Tokyo neon and the campfire glow the most) and an HDR clamp keeps chrome highlights from turning into a supernova
- **Female figure** sitting on the toilet (clothed)
- **Drag to spin.** Left/right turns, up/down flips them head-over-heels. Flick it and they keep spinning. The stream follows. Chaos ensues.
- **Load your own rigged `.glb`.** Mixamo rigs get the skeleton skin and stream placement for free.

### 🎯 "Pee as a weapon" (against cartoon objects only, we have standards)
- 💧 **Drips:** little water-drop mascots with googly eyes who wander the outdoor scenes, **run away from where you're aiming**, fill up yellow when hit and pop into a puddle. Auto-target hunts them too. Click one and it hops.
- 🖱️ **Click things:** flush the toilet, knock cans and ducks over, squish slimes, relight the campfire, wobble or rebuild the snowman
- 🟢 **Slime target range:** creeping slimes, purple one-eyed **Gloop** monsters, tin cans, rubber ducks, traffic cones
- 🔥 **Campfire:** put it out (sizzle + steam)
- ⛄ **Snowman:** turns yellow, then melts. Yellow snow lingers. As it should.
- 🌾 **Grass field:** 22,000 wind-swept grass blades, rolling hills, utility poles. Where the front page fades in.
- 🌳 **Park:** tree + fire hydrant (classic)
- 🗽 **New York street:** brick walk-ups with fire escapes, a parked yellow cab, hydrant, trash cans
- 🏮 **Tokyo neon alley:** neon signs, a glowing vending machine, paper lanterns (crank the power to reach them)
- 🥐 **Paris boulevard:** Haussmann façades, café table with wine bottles, wicker chairs, a distant iron tower
- 🎯 **Auto-target mode** aims *and* fires by itself: it judges reach at full pressure, **leads moving targets**, turns the stream power up when nothing is in reach, prefers targets you're already facing, and aims into the bowl in the bathroom. Turning it on also stops any spin and stands you back upright, so it works even after you've been twirling.
- 🎯 **Aim trainer:** a training room with glowing orbs and 60 s rounds. **Move the mouse to aim, hold the button to pee.** Shows a live time / pops / accuracy / avg time-to-kill bar, a landing reticle, and saves your best score.
- 🎯 **Auto-aim** solves the ballistic equation for you:
  $$\theta = \arctan\left(\frac{v^2 - \sqrt{v^4 - g(gd^2 + 2\,\Delta y\, v^2)}}{g\,d}\right)$$
  *(Yes, there's a physics equation in a pee simulator README. You're welcome.)*

### ⚡ Overdrive
Unlimited bladder. 1.8× pressure. Drains your body water until you **become the pee ball**. 💛
It has eyes. It bounces. It's honestly the best character in the game.

## 📊 Benchmarks (very scientific)

| Scenario | Result |
|---|---|
| Fresh bladder, aim -24° | Bullseye 🎯 |
| 3 AM, half asleep | Hits the seat. Seat was up. Hits the floor anyway |
| Overdrive in a small bathroom | Dissolved into a pee ball in 35 s |
| Ate beets, forgot | Briefly called an ambulance |
| Paris, café table | 3 wine bottles down, 0 regrets |
| Tokyo, lanterns at power 1.0× | Physically impossible. Crank it to 1.6× |
| Auto-target mode vs. 6 slimes | 45 knockdowns in 20 s, zero mercy |

## ❓ FAQ

**Why?**
Because "why not" stopped being a question somewhere around the procedural toilet flush sound.

**Is this educational?**
The urine color chart is legit. The pee ball is not.

**Can I pee on people?**
No. We have a beagle, a fountain statue, Drips, slimes, Gloops, rubber ducks, cones, trash cans, a cab, a campfire and a snowman. Have some self-respect.

**Does the toilet overflow if I don't flush?**
Yes. Then the flood dissolves you. Flush your toilet. This is the one real life lesson in here.

**Why is the sound so good?**
Pink noise, band-pass filters, LFOs and per-surface impact voices, all spatialized with HRTF. Nobody stopped me.

**Can I load my own character?**
Yes. Drop in any rigged `.glb`. Mixamo rigs get the skeleton skin and stream placement for free.

## 🐛 Known issues

- Stream does not respect personal space
- Pee ball has no known cure besides the Respawn button
- Snowman files a complaint every 9 seconds, then rebuilds and forgives you
- If you flip the character upside down and release, that's on you
- Drips are faster than they look. Lead your shots.

## 🚀 Run it locally

ES modules don't load from `file://`, so serve the folder with literally anything:

```bash
git clone https://github.com/yesjermo/pee-wee-physics.git
cd pee-wee-physics
python3 -m http.server 8765
```

Then open <http://localhost:8765> (splash, then the simulator) or <http://localhost:8765/simulator.html> (straight to business).

## 🎮 Controls

| Input | Does |
|---|---|
| `Space` | Release / stop |
| Drag the person | Spin (←→) & flip (↑↓), flick for inertia |
| Drag elsewhere | Orbit camera |
| Click an object | Flush / knock over / squish / relight / poke |
| Right-drag / scroll | Pan / zoom |
| `← → ↑ ↓` | Rotate the body |
| 🚽 Flush / 🧽 Mop & scrub | Your responsibilities |

## 📁 What's in the box

```
index.html         front page: black & white message-board splash, then the full simulator
simulator.html     the entire simulator: one file, ~2000 lines, zero build step
GAME_ROADMAP.md    plans to turn this into an actual game (god help us)
```

## 🗺️ Roadmap

See [GAME_ROADMAP.md](GAME_ROADMAP.md). Highlights: wave survival, drinks-as-ammo, a timed toilet-keeper mode, and a **pee ball rolling mini-game**.

## 🛠️ Built with

| Tool | What it's used for |
|---|---|
| **Blender** | Modelling, posing and previewing the characters and props |
| **[three.js](https://threejs.org) r160** | The 3D engine: scenes, materials, shadows, instanced grass, skinned characters |
| three.js add-ons | `GLTFLoader` (rigged characters), `OrbitControls` (camera), `EffectComposer` + `UnrealBloomPass` + `GTAOPass` + `ShaderPass` + `OutputPass` (post-processing), `RoomEnvironment` (image-based lighting), `RoundedBoxGeometry` |
| **Web Audio API** | Every sound is synthesized live: pink noise, filters, LFOs, HRTF spatial audio |
| **JavaScript (ES modules)** | All the simulation, physics, UI and HUD, loaded through an import map with no build step |
| [jsDelivr](https://www.jsdelivr.com) | CDN for three.js and the example characters |
| [Google Fonts](https://fonts.google.com) | Inter, JetBrains Mono and Noto Serif JP |
| [Shields.io](https://shields.io) | The badges up top |
| **GitHub Pages** | Hosting |

## 🙏 Credits

- [three.js](https://threejs.org) (MIT)
- The **Xbot** and **Michelle** characters are loaded at runtime from the official three.js examples. They're not bundled in this repo, and their licenses are theirs.
- Pink noise uses Paul Kellet's refined filter

## ⚠️ Disclaimer

This is an educational toy. The urine color chart is general information, **not medical advice**.
If your pee is persistently red, brown or cloudy and you did *not* just eat beets, fava beans or blue candy, please close this tab and call a doctor.

Stay hydrated. 💧 Flush the toilet. 🚽

<div align="center">

**If this made you laugh, drop a ⭐. If it made you thirsty, drink some water.**

</div>
