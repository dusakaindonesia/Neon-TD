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

- ⚡ **Delta-Time Frame Normalization:** Game loop decoupled dari refresh rate layar—berjalan konsisten pada display 60Hz, 90Hz, 120Hz, hingga 144Hz.
- ♻️ **Zero-GC Object Pooling:** Proyektil peluru dan sistem partikel menggunakan fixed-size memory pool untuk mengeliminasi micro-stuttering akibat Garbage Collection.
- 🚀 **O(1) Spatial Bitmask Grid:** Validasi penempatan tower secepat kilat tanpa perlu iterasi array jalur.
- 👆 **Hybrid Touch/Mouse Controls:** Dilengkapi *drag threshold* adaptif untuk mencegah mis-click saat seleksi atau relokasi tower di layar sentuh.
- 🧠 **Strategic Pacing:** Musuh tidak akan bergerak di awal level/wave baru sebelum tower pertama ditempatkan.
- ⏸️ **Auto-Pause on Resize:** Otomatis pause saat layar HP diputar (*rotation*) atau ukuran jendela browser berubah.
- 🔊 **Procedural Web Audio Engine:** Efek tembakan, ledakan, dan upgrade di-synthesize secara native langsung di browser (tanpa aset audio `.mp3`/`.wav` eksternal).
- ⚖️ **Dynamic Economy:** Manajemen gold terstruktur dengan pengembalian 70% saat tower dijual (*sell refund*).
- ❤️ **Second Chance Mechanism:** Diberikan 1x kesempatan retry board reset ketika wave gagal untuk merancang ulang strategi.

---

## 🗼 Towers

| Tower | Type | Cost | Range | Attributes & Tactical Role |
| :--- | :---: | :---: | :---: | :--- |
| **BLASTER** | `Cyan` | 50G | Medium | Damage dan jarak seimbang. Pilihan utama untuk pembuka wave awal. |
| **RAPID** | `Yellow` | 100G | Short | Fire-rate sangat tinggi, jarak pendek. Paling efektif di sudut tikungan path. |
| **SNIPER** | `Purple` | 150G | Extreme | Single-target heavy burst damage. Khusus eliminasi boss dari jarak jauh. |

---

## 🕹️ How to Play

1. **Build Tower:** Klik/tap tipe tower di panel bawah, lalu klik/tap pada area grid kosong di luar jalur musuh.
2. **Move Tower:** Tekan dan tahan tower yang sudah berdiri, lalu drag ke slot kosong lain untuk reposisi.
3. **Upgrade & Sell:** Tap tower yang aktif untuk membuka action panel (Upgrade stats level 1–5 atau Sell untuk refund gold).
4. **Targeting Priority:**
   - **Blaster & Sniper:** Mengunci Boss terlebih dahulu; jika tidak ada, menarget musuh yang posisinya paling depan.
   - **Rapid:** Selalu memprioritaskan musuh terdepan dalam jangkauan tembaknya.
5. **Survive:** Kalahkan Boss setiap kelipatan wave ke-3 dan adaptasi strategi Anda di layout peta baru setiap 5 wave.

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

Kontribusi terbuka untuk pengembangan fitur baru maupun optimasi:

1. Fork repository ini
2. Buat branch fitur baru (`git checkout -b feature/NamaFitur`)
3. Commit perubahan (`git commit -m 'feat: Add some feature'`)
4. Push ke branch (`git push origin feature/NamaFitur`)
5. Ajukan **Pull Request**

---

## 👨‍💻 Author

Developed with ❤️ by **Dusaka Game Indonesia**
