# 🎵 Music Player with 3-Band EQ + Dynamic Color Visualizer

This is a simple web-based music player that features a **3-band equalizer (Low, Mid, High)** and a real-time **color visualizer** that changes the screen color based on the music's frequency energy.

## 🌈 Features

- Upload and play local audio files
- Adjustable EQ bands:
  - **Low** (Red channel)
  - **Mid** (Green channel)
  - **High** (Blue channel)
- Color changes dynamically based on real-time frequency analysis
- Adaptive scaling based on the last 4 seconds of playback
- Unified color normalization for consistent visual effects

## 🚀 How to Use

1. Go to:  
   👉 **[https://carlosforster.github.io/ColorLightsMusicPlayer](https://carlosforster.github.io/ColorLightsMusicPlayer)**  
   
2. Upload an audio file from your device.

3. Use the sliders to adjust the EQ bands and watch the background color change based on audio dynamics.

## 🛠 How It Works

- Uses the Web Audio API to create a 3-band EQ with `BiquadFilterNode`s.
- An `AnalyserNode` reads frequency data in real time.
- The RGB background color corresponds to the energy in each band:
  - **Red**: Low (20–320 Hz)
  - **Green**: Mid (320–2000 Hz)
  - **Blue**: High (2000–8000 Hz)
- Color intensities are normalized using a rolling buffer of the last 4 seconds for smooth transitions.

## 📱 Mobile Use

The app works in mobile browsers like Chrome or Safari. For best performance:
- Use `.mp3`, `.wav`, or `.ogg` files.
- Add the site to your home screen to use it like an app (PWA support can be added later).

## 📂 Repository Structure

📁 ColorLightsMusicPlayer/
├─ index.html
└─ README.md
