# ✋ Neon Aura AR – Hand Detection AI

An interactive AI-powered hand tracking system that turns your hand gestures into stunning neon visuals and sound effects in real-time.  
Built using MediaPipe Hands, this project blends computer vision, creativity, and AR-like experiences in the browser.

---

## 🌟 Demo

Open the project → Allow camera → Move your hands → Watch the magic ✨

---

## 🚀 Features

### 🤖 AI Hand Tracking
- Detects up to 2 hands simultaneously  
- Tracks 21 landmarks per hand  
- High accuracy with real-time performance  

### ✋ Gesture Recognition
- 🤏 Pinch detection (Thumb + Index)  
- ✊ Fist / ✋ Open hand detection  
- 📏 Finger spread calculation  

### 🎨 Visual Effects
- Neon glowing fingertips  
- Particle trails  
- Shockwave effects on pinch  
- Lightning between hands  
- Matrix-style animated background  

### 🎧 Audio Effects
- Dynamic sound on gestures  
- Distance-based audio modulation  

### 🎭 Themes
Switch between multiple visual styles:
- 🌈 Rainbow  
- ⚡ Cyberpunk  
- 🔥 Lava  
- 🌊 Ocean  
- 🌌 Galaxy  

---

## 🧠 How It Works

- 📷 Captures webcam input  
- 🧩 Uses MediaPipe to detect hand landmarks  
- 📐 Calculates distances between points  
- 🎯 Identifies gestures  
- 🎨 Renders visuals + audio based on interaction  

### Example
- Pinch → Shockwave + zap sound  
- Fast movement → More particles  
- Two hands close → Electric arcs  

---

## ⚙️ Tech Stack

- 🧩 MediaPipe Hands  
- 🎥 Web Camera API  
- 🖼️ HTML5 Canvas  
- 🔊 Web Audio API  
- 🌐 JavaScript (Vanilla)  

---

## 📊 Hand Landmark Model

Each hand contains **21 key points**, including:
- Fingertips (4, 8, 12, 16, 20)  
- Finger joints  
- Palm center  

Used to detect:
- Distance  
- Motion  
- Gesture patterns  

---

## 📁 Project Structure
