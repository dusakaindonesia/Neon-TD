# 🏯 Neon Tower Defense

A fast-paced, cyberpunk-themed Tower Defense game built purely with HTML5 Canvas and native Web APIs. Zero external asset dependencies.

---

## 🎮 Play Now!

Play instantly in your browser (Mobile & Desktop supported) or download the Android build:

- 🌐 **Web Build:** [Play in Browser (No Install)](https://dusakaindonesia.github.io/Neon-TD/)
- 📱 **Android APK:** [Download .APK File (v1.0.0)](https://github.com/dusakaindonesia/Neon-TD/releases/download/v1.0.0/Neon.TD.apk)

---

## 📸 Screenshots

<p align="center">
  <img width="900" alt="Neon TD Gameplay 1" src="https://github.com/user-attachments/assets/89647cd1-3a16-421f-b431-af43da47e7e1" />
  <img width="900" alt="Neon TD Gameplay 2" src="https://github.com/user-attachments/assets/9c1166f2-c219-48b1-af2a-4df98c2d248a" />
</p>
<p align="center">
  <img width="900" alt="Neon TD Gameplay 3" src="https://github.com/user-attachments/assets/2ddb2623-5484-4257-aa00-a33d01b8243d" />
  <img width="900" alt="Neon TD Gameplay 4" src="https://github.com/user-attachments/assets/b07bfb36-ca66-4423-98a4-5fe5e7e08d0a" />
</p>

---

## ✨ Features

- ⚡ **Delta-Time Frame Normalization:** Game loop is decoupled from display refresh rates—runs at a uniform pace across 60Hz, 90Hz, 120Hz, and 144Hz displays.
- ♻️ **Zero-GC Object Pooling:** Bullets and particle systems utilize fixed-size memory pools to eliminate micro-stutters caused by Garbage Collection spikes.
- 🚀 **O(1) Spatial Bitmask Grid:** Instantaneous tower placement validation without iterating through path segment arrays.
- 👆 **Hybrid Touch/Mouse Controls:** Features adaptive drag threshold logic to prevent accidental placements during selection or relocation on touch screens.
- 🧠 **Strategic Pacing:** Enemies will not advance at the start of a level/wave until your first tower is placed.
- ⏸️ **Auto-Pause on Resize:** Automatically halts gameplay when rotating devices or resizing the browser window to avoid desync.
- 🔊 **Procedural Web Audio Engine:** Sound effects (shooting, explosions, upgrades) are synthesized natively via the browser audio context—no external `.mp3` or `.wav` files required.
- ⚖️ **Dynamic Economy:** Strategic resource allocation with a 70% gold refund rate upon selling towers.
- ❤️ **Second Chance Mechanism:** Grants 1 free board-reset retry per run when a wave is breached.

---

## 🗼 Towers

| Tower | Type | Cost | Range | Attributes & Tactical Role |
| :--- | :---: | :---: | :---: | :--- |
| **BLASTER** | `Cyan` | 50G | Medium | Balanced damage and range. Primary baseline tower for initial waves. |
| **RAPID** | `Yellow` | 100G | Short | Extremely high fire rate, lower range. Most effective along tight path bends. |
| **SNIPER** | `Purple` | 150G | Extreme | Single-target heavy burst damage. Tailored for taking down armored bosses. |

---

## 🕹️ How to Play

1. **Build Tower:** Click/tap a tower icon from the bottom panel, then click/tap any empty grid tile outside the enemy route.
2. **Move Tower:** Press and hold an active tower, then drag it to a valid empty slot to reposition.
3. **Upgrade & Sell:** Tap an existing tower to display the action panel (Upgrade stats up to Lv5 or Sell for a gold refund).
4. **Targeting Priority:**
   - **Blaster & Sniper:** Target Boss units first; if none are present, target the lead enemy on the path.
   - **Rapid:** Always focuses on the first enemy within reach.
5. **Survive:** Defeat Boss encounters every 3 waves and adjust defenses to shifting map paths every 5 waves.

---

## 🛠️ Architecture & Tech Stack

- **Core Engine:** Vanilla HTML5 Canvas API & ES6+ JavaScript (Monolithic single-file architecture)
- **Audio Engine:** Native Web Audio API (`OscillatorNode`, `GainNode`, Procedural White Noise Buffer)
- **State & Storage:** LocalStorage API (Wave persistence, autosave, & high-score tracking)
- **Styling:** Tailwind CSS (CDN) + Orbitron Neon Cyberpunk Typography
- **Mobile Container:** Native Android Kotlin WebView wrapper (`.apk`)

---

## 🗺️ Roadmap

- [x] Engine performance optimization (Delta-Time, Pooling, Grid Bitmask, Squared Distance)
- [ ] New Enemy Types: Stealth / Shielded fast runners
- [ ] Tower Status Effects: Slow-down aura & Splash damage
- [ ] Screen-shake visual feedback on critical hits / Boss defeats
- [ ] Custom map array generator / in-game Level Editor

---

## 🤝 Contributing

Contributions for new features, balance adjustments, or engine enhancements are welcome:

1. Fork this repository
2. Create your feature branch (`git checkout -b feature/NewFeature`)
3. Commit your changes (`git commit -m 'feat: Add some feature'`)
4. Push to the branch (`git push origin feature/NewFeature`)
5. Open a **Pull Request**

---

## 👨‍💻 Author

Developed with ❤️ by **Dusaka Game Indonesia**
