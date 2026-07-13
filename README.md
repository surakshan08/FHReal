<img width="443" height="254" alt="FHReal Logo" src="https://github.com/user-attachments/assets/60491faf-f06f-47e9-9ab3-c8a490efe5fd" />

# FHReal — Forza Horizon 6 Companion Overlay

> A safe, non-invasive companion app for **Forza Horizon 6** that adds real-world driving features like fuel consumption, oil maintenance, an odometer, and more — all via the game's official telemetry system.

---

## 👋 Welcome

FHReal enhances your Forza Horizon 6 experience by adding immersive driving mechanics that the game itself doesn't include. It works entirely through Forza's built-in **Data Out (UDP telemetry)** system — it never touches game files or memory.

The only "input" it sends to the game is simulating brake key presses to replicate fuel starvation — and only during free roam, never in races.

> 💬 Found a bug or have feedback? Please report it! This project is actively developed, and your feedback helps improve future updates.

## ❤️ Support

If you enjoy my work and would like to support future projects, you can buy me a coffee via PayPal:

https://paypal.me/surakshanCheckala

---

## ✨ Features

| Feature | Description |
|---|---|
| ⛽ **Fuel Consumption** | Simulated fuel usage based on RPM and throttle input, with a live HUD gauge |
| 🛑 **Fuel Starvation** | Engine stutters and dies when you run out of fuel (free roam only) |
| 🔧 **Oil Maintenance** | Oil degrades over distance — visit workshops to top it up |
| 📏 **Odometer** | Per-car odometer that tracks real distance driven |
| 🚀 **Boost Gauge** | Live boost readout for turbocharged and supercharged vehicles |
| 🗺️ **Navigation** | Displacement radar pointing toward the nearest gas station or workshop |
| 🚗 **Vehicle Info Card** | See your car name, next oil service distance, and session trip distance |
| ⚙️ **Configurable Settings** | Adjust fuel rate, oil rate, brake key, units, and more |

---

## 🚀 Getting Started

### Step 1 — Enable Telemetry in Forza
1. Open Forza Horizon 6
2. Go to **Settings → HUD & Gameplay**
3. Scroll all the way down and turn **Data Out** → **ON**
4. Note the **Data Out IP Port** (you'll need it in Step 3)

### Step 2 — Launch FHReal
Run **FHReal.exe** (or `FHReal.py` if running from source).

### Step 3 — Configure the App
1. Double-click or right-click the **pink H icon** in your system tray
2. Set the **Telemetry Port** to match the port from Forza's Data Out setting
3. Set the **Brake Key** to match your in-game brake input
   - Find it in Forza: **Settings → Controls → Change Input Mapping → Keyboard**

### Step 4 — In-Game Controls

| Key | Action |
|---|---|
| `L` | Open / close the FHReal menu |
| `;` (Semicolon) | Navigate menu **down** |
| `'` (Quote) | Navigate menu **up** |
| `Enter` | Select menu item |
| `Escape` | Go back / close menu |
| `Insert` | Toggle HUD visibility |
| `F` | Emergency refill to 50% *(only works when fuel is at 0%)* |
| Hold `Ctrl` | Drag HUD to reposition it |

---

## 📍 Registering Locations

To use fuel stations and workshops you need to register them yourself:

1. Drive to a gas station or workshop in-game
2. Open the FHReal menu (`L`)
3. Select **Register Location** and choose the type

Once registered, the navigation radar will point you toward the nearest one.

---

## ❓ FAQ

**Why doesn't the in-game fuel gauge match FHReal's HUD?**
> Forza doesn't allow any external app to write data into the game. FHReal tracks fuel independently using its own simulation — it can't sync with the in-game gauge.

**I have two of the same car — do they share fuel and odometer data?**
> Yes, unfortunately. Forza's telemetry doesn't expose a unique identifier per vehicle instance, only the car model ID. Two identical cars will share the same stats.

**Why not use the fuel level directly from telemetry?**
> Forza only reports real fuel levels when **damage simulation** is enabled. Most players use no damage or cosmetic-only damage, which keeps fuel permanently at 100% in telemetry. FHReal simulates fuel independently so everyone can enjoy it regardless of damage settings.

**One of the gas station attendants is kind of rude...**
> That's Reina. We tried. She's just like that.

---

## ⚠️ Known Issues

- **Wheel / controller inputs:** Only keyboard and XInput gamepads are currently supported. If you test a steering wheel, please let us know if it works!
- **Display modes:** The overlay currently requires the game to be in **fullscreen mode** with the **analog HUD** enabled.
- **Ultrawide monitors:** Not yet tested. If you encounter issues, please report with a screenshot.
- **Fuel gauge not visible?** Report with a screenshot, your Windows display resolution, and the resolution set in-game.
- **Eliminator / Hide & Seek modes:** Fuel consumption is currently active in these modes. Telemetry race-status data is unreliable, making detection tricky — a fix is in progress.
- **Language:** The developer is not a native English (or Japanese) speaker. If you spot any text errors, please report them!

---

## 🛡️ Legal & Fair Play

### Anti-Cheat Compliance
FHReal is a **100% safe and compliant** companion app. It uses only the official **UDP Telemetry "Data Out"** feature built into Forza's own settings.

- ✅ Does **not** modify game files
- ✅ Does **not** inject code into the game process
- ✅ Does **not** read or write to game memory (RAM)
- ✅ Key simulation (brake only) is **disabled during races** — no competitive advantage is possible

### Trademark Disclaimer
FHReal is an unofficial fan-made project. It is **not** affiliated with, endorsed by, or connected to **Microsoft Corporation**, **Playground Games**, or **Turn 10 Studios**.

"Forza", "Forza Horizon", and "Forza Motorsport" are registered trademarks of Microsoft Corporation. Car brand names within vehicle data profiles are used for simulation and immersion purposes only.

---
