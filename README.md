# The Ghost Feed — Algorithmic Influence Projection

> *"You don't scroll the feed. It scrolls you."*

An interactive 3D spatial simulation and forensic deconstruction of algorithmic social media capture, cognitive dwell-time decay, and predictive latency.

---

## 👁️ Core Mechanics & Architecture

1. **Initial Ingestion Gatekeeper (`/`)**:
   - Monospace user handle capture with dynamic, character-scaled profile confidence meter (`min(charCount * 4.8, 97)%`).
   - Anonymous entry bypass and assigned `USER-0xXXXX` session identification.
   - CRT chromatic glitch transition into the navigation hub.

2. **Navigation Hub (`/hub`)**:
   - Continuous uninterrupted session timer (`SESSION: HH:MM:SS`) persisting across all route transitions.
   - Three navigation vectors:
     - `[01] ENTER THE FEED` &rarr; 3D corridor visualizer.
     - `[02] THE MANIPULATION CODEX` &rarr; Standalone Algorithmic Dossier modal.
     - `[03] ABOUT THIS BUILD` &rarr; Architecture & prompt specification modal.
   - Rotating forensic telemetry status line cycling every ~4s.

3. **Interactive 3D Corridor (`/feed`)**:
   - **Locked First-Person Z-Drift**: Camera navigation driven by mouse look-ahead and debounced scroll inertia.
   - **3D Social Cards (`PostCard3D`)**: Procedurally rendered high-contrast cards tracking individual dwell times and cortisol escalation with glowing alarm-red threshold breaches (&ge; 70%).
   - **Predictive Ghost Silhouette (`GhostFigure`)**: Low-poly humanoid entity exhibiting a **~500ms time-buffered lag queue** and periodic **predictive glitch leaps** (every 18–25s) snapping ahead to upcoming high-outrage cards.
   - **"The Friction of Leaving"**: Viscous scroll resistance scaling dynamically when attempting to navigate away from high-influence cards.
   - **The Clinical Hum (`audioEngine`)**: Zero-dependency Web Audio API synthesizer generating sub-bass server drones (55Hz/110Hz), subconscious tension tones (2600Hz binaural dissonance), and synthetic glitch chirps.
   - **2D Parallax Fallback**: Automatic detection and graceful fallback canvas for devices without WebGL support.

---

## 🛠️ Technical Stack

- **Framework**: React 19 + Vite
- **3D Engine**: Three.js, React Three Fiber (`@react-three/fiber`), React Three Drei (`@react-three/drei`)
- **Routing**: React Router DOM (`BrowserRouter` with SPA rewrites)
- **Audio Engine**: Web Audio API (`AudioContext`, `BiquadFilterNode`, `OscillatorNode`)
- **Styling & Design System**: Stitch Forensic Design Tokens, JetBrains Mono & Fira Sans typography
- **Icons**: Lucide React & Google Material Symbols

---

## 🚀 Quick Start & Local Development

### 1. Install Dependencies
```bash
npm install
```

### 2. Run Local Development Server
```bash
npm run dev
```
Open `http://localhost:5173/` in your browser.

### 3. Production Build & Preview
```bash
npm run build
npm run preview
```

---

## 🌐 Deployment Instructions

### Option 1: Deploy to Vercel (Recommended)

#### Using Vercel CLI:
```bash
npm install -g vercel
vercel
```
*(When prompted, accept default settings. The included `vercel.json` ensures all SPA routes `/`, `/hub`, and `/feed` rewrite cleanly.)*

#### Using GitHub & Vercel Dashboard:
1. Push your repository to GitHub:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: The Ghost Feed"
   git branch -M main
   git remote add origin https://github.com/[YOUR-USERNAME]/the-ghost-feed.git
   git push -u origin main
   ```
2. Go to [vercel.com/new](https://vercel.com/new) and import the repository.
3. Framework preset: **Vite**.
4. Click **Deploy**.

---

### Option 2: Deploy to Netlify

#### Using Netlify CLI:
```bash
npm install -g netlify-cli
npm run build
netlify deploy --prod --dir=dist
```
*(The included `public/_redirects` file automatically handles SPA routing on Netlify.)*

---

## 📂 Project Structure

```
thrive-website-2/
├── index.html                   # HTML entry with JetBrains Mono & Fira Sans
├── vercel.json                  # SPA rewrite configuration for Vercel
├── vite.config.js               # Vite bundler config
├── public/
│   └── _redirects               # SPA routing rewrite for Netlify
└── src/
    ├── App.jsx                  # Route definitions (/, /hub, /feed)
    ├── main.jsx                 # React root mount
    ├── index.css                # Stitch design tokens & scanline styling
    ├── context/
    │   └── SessionContext.jsx   # Global store for subjectId, timer & glitch state
    ├── components/
    │   ├── 3d/
    │   │   ├── Scene.jsx        # Three.js canvas & camera rig
    │   │   ├── CardField.jsx    # 3D spatial distribution of social cards
    │   │   ├── PostCard3D.jsx   # Interactive 3D post with dwell & influence shaders
    │   │   ├── GhostFigure.jsx  # 500ms lagged humanoid entity with predictive leaps
    │   │   └── ReactiveLights.jsx # Scene lighting responding to alarm levels
    │   ├── screens/
    │   │   ├── EntryScreen.jsx  # / route: Handle ingestion & confidence meter
    │   │   ├── NavigationHub.jsx# /hub route: Command center & modal launcher
    │   │   └── FeedExperience.jsx# /feed route: Full 3D corridor experience
    │   ├── ui/
    │   │   ├── HeaderHUD.jsx    # Top telemetry bar & clinical hum toggle
    │   │   ├── SidePanel.jsx    # Algorithmic Dossier & Manipulation Codex
    │   │   ├── ScrollGuide.jsx  # Right edge depth rail & velocity gauge
    │   │   └── GlitchTransition.jsx # Reusable CRT chromatic glitch overlay
    │   └── fallback/
    │       └── Fallback2DFeed.jsx # Graceful 2D canvas parallax fallback
    ├── hooks/
    │   ├── useGhostLag.js       # 500ms time-buffered queue tracking
    │   ├── useInfluenceScore.js # Dwell-time diminishing returns engine
    │   └── useScrollVelocity.js # Viscous friction scroll physics
    ├── data/
    │   └── feedPosts.js         # 9 psychological content payloads
    └── utils/
        └── audioEngine.js       # Web Audio API synthesizer ("The Clinical Hum")
```

---

## 📄 License
MIT License. Built for forensic demonstration and research into algorithmic attention dynamics.
