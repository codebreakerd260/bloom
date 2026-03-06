# Bloom 3D 🌱

Voice your gratitude. Watch your 3D garden grow.

Bloom is an interactive web application that transforms your spoken gratitude journal entries into a vibrant, procedurally generated 3D garden. Through a combination of on-device AI for speech recognition and Gemini API for sentiment analysis, it builds a peaceful, personal space entirely within your browser.

## ✨ Features

- **3D Interactive Garden:** Built with React Three Fiber (`@react-three/fiber` & `three.js`), the garden exists in real 3D space. You can click and drag to pan and zoom around your growing plants.
- **Local Speech-to-Text (STT):** Powered by `transformers.js` running an on-device Whisper Tiny model. Hold the record button to speak your entry directly into the browser without any audio ever leaving your machine!
- **AI Sentiment Analysis:** Integrates the official `@google/generative-ai` SDK (Gemini 2.5 Flash) to analyze the meaning and emotion behind your gratitude entry. Based on the sentiment (e.g., family, peace, joy, nature), it procedurally selects and plants the corresponding 3D flora (Sunflower, Fern, Tulip, Tree, or Grass).
- **TTS Integration:** Supports an external Piper TTS audio engine (running on `http://localhost:5050/api/tts`) to speak encouraging responses, with an automatic, graceful native Web Speech API fallback if the local Piper server is offline.
- **Procedural 3D Assets:** All plants (Sunflowers, Tulips, Ferns, Trees, Grass) are procedurally generated in R3F with custom stylized glass/matte materials, randomized scale/rotation, and optimized with React `useMemo` to prevent rendering jitter holding random 3D identities across keystrokes.
- **Interactive Memories:** The generated plants are fully interactive. Hover over any plant to reveal a stunning frosted-glass tooltip containing the original journal entry that spawned it, and click on the plant to replay the AI's encouraging audio response.
- **Glassmorphic UI:** Features a modern, premium frosted-glass design layered seamlessly atop the active 3D `Canvas`.
- **Single File Wonders:** The entire React architecture, Tailwind styling, and 3D rendering loop are elegantly bundled into a single `index.html` file using Babel standalone. No node modules or build steps required.
## 🚀 How to Run

Because Bloom relies entirely on CDN-delivered ESM imports, you don't even need to install Node.js!

1. Simply double-click `index.html` to open it in your web browser, or host it on GitHub Pages.
2. Enter your Gemini API Key.
3. Hold the "Hold to Talk" button (allow Microphone permissions when prompted) and speak your gratitude.
4. Watch your garden grow!

## 🛠️ Stack

- **React 18** (via ESM)
- **Tailwind CSS** (via CDN)
- **Three.js & React Three Fiber/Drei**
- **@xenova/transformers** (Browser-native Whisper STT)
- **@google/generative-ai** (Gemini Sandbox)
