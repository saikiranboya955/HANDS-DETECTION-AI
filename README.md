<div align="center">

# ⚡ Neon Aura AR ⚡

### Real-Time AI Hand Interaction

**Move your hands. Create the experience.**

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&duration=3000&pause=1000&color=00E5FF&center=true&vCenter=true&width=600&lines=Real-Time+Hand+Tracking+with+MediaPipe;Gesture-Powered+Visual+Effects;Two-Hand+Interactive+Energy+System;Built+with+HTML5+%2B+CSS3+%2B+JavaScript" alt="Typing SVG" />

<br>

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![MediaPipe](https://img.shields.io/badge/MediaPipe-FF6F00?style=for-the-badge&logo=google&logoColor=white)
![WebAudio](https://img.shields.io/badge/Web%20Audio%20API-8A2BE2?style=for-the-badge&logo=audiomack&logoColor=white)

![Stars](https://img.shields.io/github/stars/your-username/neon-aura-ar?style=for-the-badge&color=FFD700)
![Forks](https://img.shields.io/github/forks/your-username/neon-aura-ar?style=for-the-badge&color=00E5FF)
![License](https://img.shields.io/badge/License-MIT-ff69b4?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-39FF14?style=for-the-badge)

</div>

---

## 🧬 Overview

**Neon Aura AR** is an interactive computer-vision experience that transforms real-time hand movements into dynamic digital visual effects.

Using **MediaPipe Hands**, the application detects hand landmarks through the user's webcam and maps finger movements, gestures, and two-hand interactions onto an interactive HTML Canvas. The experience combines hand tracking, gesture recognition, particle effects, energy waves, animated backgrounds, audio feedback, and multiple visual themes — all running **entirely in the browser**.

> 🖐️ *No installs. No backend. Just your webcam and your hands.*

---

## 🚀 Features

<table>
<tr>
<td width="50%" valign="top">

### 🖐️ Real-Time Hand Tracking
- Detects up to **two hands** simultaneously
- Tracks **21 landmarks per hand**
- Live hand count + FPS in the HUD
- Smooth, low-latency landmark updates

### ✋ Gesture Recognition
- 🤏 **Pinch** → triggers a shockwave + sound
- 🖐️ **Open Hand** → expands effect radius
- ✊ **Fist** → contracts / calms the field

</td>
<td width="50%" valign="top">

### ⚡ Two-Hand Interaction
- Glowing energy lines between fingertips
- Lightning connections on close proximity
- Rotating geometric patterns
- Audio pitch shifts with hand distance

### ✨ Particle & Visual Effects
- Physics-based glowing particles
- Fingertip-driven shockwaves
- Reactive matrix-style animated background

</td>
</tr>
</table>

---

## 🎨 Visual Themes

<div align="center">

| Theme | Preview | Vibe |
|:---:|:---:|:---|
| 🌈 **Rainbow** | ![#FF0000](https://placehold.co/15x15/FF0000/FF0000.png) ![#00FF00](https://placehold.co/15x15/00FF00/00FF00.png) ![#0000FF](https://placehold.co/15x15/0000FF/0000FF.png) | Continuously shifting spectrum |
| ⚡ **Cyberpunk** | ![#FF003C](https://placehold.co/15x15/FF003C/FF003C.png) ![#00FFF7](https://placehold.co/15x15/00FFF7/00FFF7.png) | Neon red & electric cyan |
| 🔥 **Lava** | ![#FF4500](https://placehold.co/15x15/FF4500/FF4500.png) ![#FFA500](https://placehold.co/15x15/FFA500/FFA500.png) | Molten red/orange heat |
| 🌊 **Ocean** | ![#00BFFF](https://placehold.co/15x15/00BFFF/00BFFF.png) ![#1E90FF](https://placehold.co/15x15/1E90FF/1E90FF.png) | Deep blue/cyan calm |
| 🌌 **Galaxy** | ![#8A2BE2](https://placehold.co/15x15/8A2BE2/8A2BE2.png) ![#4B0082](https://placehold.co/15x15/4B0082/4B0082.png) | Cosmic purple depths |

*Switch instantly, live, mid-experience — no reload required.*

</div>

---

## 🧠 How It Works

```text
                     🎥  Webcam Feed
                          │
                          ▼
                 🤖  MediaPipe Hands
                          │
                          ▼
              📍  21 Hand Landmarks (x2)
                          │
        ┌─────────────┬───┴────────┬──────────────┐
        ▼             ▼             ▼              ▼
   Gesture Det.   Finger Pos.   Hand Motion   Two-Hand Logic
        │             │             │              │
        └─────────────┴──────┬──────┴──────────────┘
                              ▼
                  🎨  Canvas Rendering Engine
        ┌──────────┬────────────┬───────────────┐
        ▼          ▼            ▼               ▼
   Particles   Shockwaves   Energy Lines   Dynamic BG
                              │
                              ▼
               ✨  Interactive Visual Experience
```

MediaPipe Hands is initialized with support for up to two hands and configurable detection/tracking confidence values.

---

## 🎯 Gesture System

### 🤏 Pinch Detection

```javascript
// Distance between Thumb Tip (4) and Index Tip (8)
const distance = getDistance(landmarks[4], landmarks[8]);

if (distance < PINCH_THRESHOLD) {
  triggerShockwave(midpoint(landmarks[4], landmarks[8]));
  playPinchSound();
  updateGestureLabel("PINCH");
}
```

### ✋ Open Hand / ✊ Fist

```javascript
// Spread between Index Tip (8) and Pinky Tip (20)
const spread = getDistance(landmarks[8], landmarks[20]);
const spreadPercent = normalize(spread) * 100;

const gesture = spreadPercent > OPEN_THRESHOLD ? "OPEN HAND" : "FIST";
```

---

## 🛠️ Technology Stack

<div align="center">

| Technology | Purpose |
|:---|:---|
| 🟧 **HTML5** | Application structure |
| 🟦 **CSS3** | UI, responsive layout, glassmorphism |
| 🟨 **JavaScript** | Core logic & interaction |
| 🔴 **MediaPipe Hands** | Real-time landmark detection |
| 🎨 **Canvas 2D API** | Visual effects rendering |
| 🔊 **Web Audio API** | Interactive sound feedback |
| 📷 **Web Camera API** | Webcam input stream |
| 🔤 **Google Fonts** | Interface typography |

</div>

No package installation or Node.js build process required — MediaPipe is loaded directly via CDN.

---

## 📁 Project Structure

```text
HANDS-DETECTION-AI/
│
├── 📄 INDEX.HTML          → Landing page, tracking logic, gestures, canvas, audio
├── 🎨 style.css            → HUD, theme selector, glassmorphism, responsive layout
└── 📘 README.md            → You are here
```

---

## 💻 Getting Started

<table>
<tr><td>

**1️⃣ Clone the repository**
```bash
git clone https://github.com/your-username/neon-aura-ar.git
```

**2️⃣ Move into the project**
```bash
cd neon-aura-ar
```

**3️⃣ Start a local server**
```bash
python -m http.server 8080
```

**4️⃣ Open in your browser**
```text
http://localhost:8080
```

</td></tr>
</table>

### 🎮 Using the Experience

| Step | Action |
|:---:|:---|
| 1 | Click **Enter Experience** |
| 2 | Allow camera access |
| 3 | Place your hand in front of the camera |
| 4 | Move your fingers and hands |
| 5 | Try a 🤏 pinch gesture |
| 6 | Bring **two hands** into frame |
| 7 | Explore the theme selector 🎨 |

---

## 🔐 Privacy

> 🛡️ **Neon Aura AR is 100% client-side.**

The webcam feed is processed **locally in the browser** for real-time hand tracking. There is no backend, no video upload, and no storage of camera footage. The landing page clearly informs users that all processing happens on-device.

---

## ⚙️ Configuration

```javascript
const HAND_CONFIG = {
  maxNumHands: 2,
  modelComplexity: 1,
  minDetectionConfidence: 0.7,
  minTrackingConfidence: 0.7
};
```

These settings balance real-time tracking accuracy with browser performance.

---

## 🔮 Future Improvements

- 🧠 Custom ML-based hand pose classification
- 🕹️ Gesture-controlled UI navigation
- 🧊 3D hand visualization
- 🎆 Additional particle systems
- 🎧 Richer interactive audio layers
- 📹 Recording & exporting generated visuals
- 📱 Mobile camera optimization
- 🖥️ WebGL-accelerated rendering

---

## 📌 Use Cases

<div align="center">

`Computer Vision` • `HCI Projects` • `AI/ML Portfolio` • `Interactive Digital Art`
`Gesture-Controlled Interfaces` • `AR-Inspired Web Experiences` • `Creative Coding`

</div>

---

## 📚 Core Concepts Demonstrated

| | | |
|:---|:---|:---|
| ✅ Computer Vision | ✅ Hand Landmark Detection | ✅ Gesture Recognition |
| ✅ Real-Time Video Processing | ✅ Canvas Rendering | ✅ Particle Physics |
| ✅ Interactive Visualization | ✅ Web Audio | ✅ Event-Driven JS |
| ✅ Responsive UI Design | ✅ Client-Side AI Processing | |

---

## 👨‍💻 Author

<div align="center">

### **Sai Kiran Boya**

*AI/ML • Generative AI • Computer Vision • Data Analytics*

Focused on building practical AI applications and interactive computer-vision experiences using Python, machine learning, deep learning, and modern web technologies.

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/your-username)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](#)

</div>

---

<div align="center">

## ⭐ Support This Project

If you find this project interesting, consider giving the repository a **star** ⭐

![Stars](https://img.shields.io/github/stars/your-username/neon-aura-ar?style=social)

### ✨ Neon Aura AR ✨
**See the hand. Track the movement. Turn motion into light.**

</div>
