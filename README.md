# Viveka Vara 🌌

![Project Status](https://img.shields.io/badge/Status-Prototype-blue)
![Tech](https://img.shields.io/badge/Engine-React%20%2B%20Vite-61DAFB)
![AI](https://img.shields.io/badge/AI-Google%20Gemini%203.0-8E75B2)

**Viveka Vara** (Sanskrit for *"Choice of Wisdom"*) is a generative reality engine that bridges the gap between human emotion and digital environments. 

Unlike traditional applications that are static, Viveka Vara acts as a living system. It utilizes Multimodal AI to sense the user's emotional state—via text, voice, or facial expression—and dynamically reconstructs the 2D parallax environment, lighting, weather physics, and procedural audio soundscapes in real-time.

---

## ✨ Key Features

### 🧠 Multimodal Neural Sensor
The application ingests human input through three distinct streams using the **Google GenAI SDK**:
*   **Vision Sync:** Real-time facial emotion recognition via webcam (Gemini Vision).
*   **Semantic Analysis:** Text-based sentiment analysis.
*   **Tonal Analysis:** Voice recording analysis for emotional inflection.

### 🍃 Procedural Environment
A custom 2D rendering engine built on top of React:
*   **Parallax Scrolling:** Multi-layered SVG depth system (Foreground, Hero, Mid-ground, Background, Sky).
*   **Dynamic Physics:** Particle systems for rain, ash, fog, fireflies, and birds that respect wind speed and gravity based on emotion.
*   **Post-Processing:** CSS-based dynamic color grading, bloom, vignetting, and chromatic aberration.

### 🔊 Generative Audio Engine
*   **Zero Sample Files:** All ambient audio is synthesized 100% procedurally using the **Web Audio API**.
*   **Real-time Synthesis:** Pink noise for wind/rain, oscillators for birds/chimes, and low-frequency drones for tension are mixed live based on the current state.


## 🛠️ Tech Stack

*   **Core:** React 18, TypeScript, Vite
*   **AI:** Google GenAI SDK (`@google/genai`)
    *   *Models:* `gemini-3-flash`, `gemini-3-pro`, `gemini-2.5-flash-native-audio`
*   **Styling:** Tailwind CSS, Framer Motion, Lucide React
*   **Audio:** Native Web Audio API (Oscillators, GainNodes, BiquadFilters)
*   **Graphics:** HTML5 Canvas (Particles), SVG (Environment Layers)

---

## 🚀 Getting Started

### Prerequisites
*   Node.js (v18+)
*   A Google Cloud Project with the **Gemini API** enabled.
*   An API Key (Get one at [aistudio.google.com](https://aistudio.google.com/)).

### Installation

1.  **Clone the repository**
    ```bash
    git clone https://github.com/yourusername/viveka-vara.git
    cd viveka-vara
    ```

2.  **Install dependencies**
    ```bash
    npm install
    ```

3.  **Configure Environment**
    Create a `.env` file in the root directory (or set it in your system environment variables):
    ```env
    API_KEY=your_google_gemini_api_key_here
    ```

4.  **Run the Application**
    ```bash
    # Standard launch
    npm run dev
    
    # Or use the provided batch script (Windows)
    ./run_app.bat
    ```

---

## 🎮 Controls

### The Dashboard
Upon logging in (mock auth), you access the Command Console.
*   **Launch Sim:** Enters the main immersive view.
*   **Settings:** Toggle hardware acceleration, spatial audio, etc.

### The Simulation
*   **Sidebar Controls:** Manually force specific emotional states to test the renderer.
*   **Camera Icon:** Activates the webcam for continuous emotion scanning.
*   **Headphones Icon:** Summons "Viveka" (Gemini Live) for a voice conversation.
*   **Brain Icon:** Opens the text/voice analysis modal.

---

## 📂 Project Structure

```text
src/
├── components/
│   ├── CameraEmotionSync.tsx   # Webcam analysis logic
│   ├── EnvironmentAssets.tsx   # SVG definitions for world layers
│   ├── ParticleSystem.tsx      # Canvas-based weather effects
│   ├── SimulationView.tsx      # Main game loop & layer composition
│   ├── VoiceGuide.tsx          # Gemini Live API implementation
│   ├── AmbientAudio.tsx        # Web Audio API synthesizer
│   └── ...
├── services/
│   └── geminiService.ts        # API wrappers for GenAI SDK
├── constants.tsx               # Emotion presets (Physics/Colors/Audio config)
└── types.ts                    # TypeScript definitions
```

---

## 🔮 Future Roadmap

*   [ ] **3D Migration:** Porting the rendering layer from DOM/SVG to Three.js/R3F for true depth.
*   [ ] **User Profiles:** Long-term memory for the Spirit Guide to remember past conversations.
*   [ ] **Biometric Integration:** Support for smart watch heart-rate data API.

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

---
