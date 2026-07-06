# Uchiha Itachi: Visual Jutsu Engine 👁️🔥

![Itachi](https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExbXozanQwcmV1a3YzOWpmdHF3aTQ4dnRxdDNwam5iejQyeWg0bHF1YyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/3fNmJ20ErpkjK/giphy.gif)

A high-fidelity, interactive, and visually stunning web application that uses your **webcam and real-time hand-sign tracking** (or manual deck controls) to unleash powerful Uchiha clan jutsu. Built using Three.js, MediaPipe Hands, and high-performance GPU particle simulation.

---

## 🌟 Features

*   **25,000 Particle GPU Simulation**: Dynamic, mathematical morphing of particles to represent different energy states.
*   **MediaPipe Hand Sign Tracking**: Real-time webcam tracking that recognizes traditional Uchiha hand seals and gestures.
*   **Anime-Style Visual Effects**: UnrealBloom post-processing, screen-shaking, film grain, and high-fidelity custom-colored structures.
*   **Hybrid Controls**: Smoothly switches between webcam gesture tracking and manual click buttons without control conflicts.
*   **Zero Installation Setup**: Lightweight, runs directly in any modern web browser via CDNs.

---

## ⚡ The Jutsu Deck & Gestures

| Jutsu Technique | Gesture Command | Description | Visual Output |
| :--- | :--- | :--- | :--- |
| **Chakra Neutral State** | *No Hands / Default* | Calm rest state of Itachi's chakra. | Swirling crimson and charcoal ash mist. |
| **Fire Style: Fire Ball Jutsu** | **Tiger Seal** (Both hands raised up close) | Katon: Gōkākyū no Jutsu! | A roaring, rapid-rising golden-orange fire vortex cone. |
| **Kekkei Genkai: Tsukuyomi** | **One-Handed Sign** (Index + Middle up) | Ultimate hypnotic time-space illusion. | Concentric crimson rings casting deep hypnotic space-time ripples. |
| **Illusion: Genjutsu Anime Seal** | **Genjutsu Finger** (Index up only) | Trap target in a powerful energetic seal. | A majestic spinning **Kanji 「幻」** (Illusion) seal surrounded by an orange pentagram and vibrating violet rings. |
| **Mangekyō Sharingan Activated** | **Pinch Gesture** (Thumb + Index pinched) | Unleashes the legendary Mangekyō. | Itachi's three-bladed pinwheel revolves majestically in a flat flat iris ring. |

---

## 🚀 Running the Project

Since this project runs entirely in the browser using HTML5 and modern CDNs, **no complex compilation or setup is required!** However, to use your webcam, modern browsers require the file to be served over `http://localhost` (or HTTPS).

Here are the simplest ways to start the project:

### Option 1: VS Code Live Server (Recommended)
1. Open the project folder in **Visual Studio Code**.
2. Install the **Live Server** extension (by Ritwick Dey) if you haven't already.
3. Click the **"Go Live"** button in the bottom right status bar of VS Code.
4. The application will launch automatically at `http://127.0.0.1:5500/index.html`.

### Option 2: Using Node.js (Terminal)
If you have Node.js installed, run this command in your terminal inside the project directory:
```bash
# Serves the directory on localhost:3000
npx serve
```
Or:
```bash
# Serves the directory on localhost:8080
npx http-server
```

### Option 3: Using Python (Terminal)
If you have Python installed, run:
```bash
# For Python 3
python3 -m http.server 8000
```
Then navigate to `http://localhost:8000` in your web browser.

---

## 🛠️ Code Structure & Architecture

*   **Three.js Renderer (`index.html`)**: Sets up the WebGL environment, Perspective Camera, and an `EffectComposer` with `UnrealBloomPass` to give the particles a gorgeous neon glow.
*   **MediaPipe Hands SDK**: Tracks up to 2 hands simultaneously, retrieving 21 coordinates per hand in a normalized `(x, y, z)` space.
*   **State Morpher (`updateState`)**: Orchestrates transitions between states by shifting `targetPositions`, `targetColors`, and `targetSizes` for the 25,000 distinct particles.
*   **Dynamic Jitter (Vibration)**: Injected on top of the interpolated points in the render loop to give specific jutsu (like the Genjutsu Seal) high-frequency anime style vibration.

---

## 👤 Credits

Created as a homage to **Itachi Uchiha** from *Naruto*. Uses Open Source tools:
*   [Three.js](https://threejs.org/) for WebGL 3D rendering.
*   [MediaPipe Hands](https://google.github.io/mediapipe/solutions/hands.html) for hand tracking.
