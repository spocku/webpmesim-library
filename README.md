# WEBPMESIM-library

> **Retro Sci-Fi Operations Archive & Interactive Mechanical Engineering Simulation Catalog**

WEBPMESIM-library(Website Physics Math Engineering Simulator Library) A browser-native repository dashboard built in the **webpmesim** retro-futuristic CAD/CRT aesthetic (inspired by retro crt tactical command consoles, vintage vector monitors, and engineering blueprints). It indexes, categorizes, stores, inspects, and launches standalone HTML physics & engineering simulations locally without external backend dependencies.

Live deployment: **[https://spocku.github.io/webpmesim-library/](https://spocku.github.io/webpmesim-library/)**

---

## Features

### Three Retro-Futuristic Themes
Switch between themes instantly via the top telemetry HUD:
- **CRT Mode**: Deep phosphor amber/orange glow, CRT scanlines, sweep bar, noise grain, corner reticles, and monospaced typography.
- **Blueprint Mode**: Cyan / dark slate vector wireframes with architectural graph grid overlays.
- **White / Technical Print Mode**: Clean daytime engineering document aesthetic with high contrast.

###  Local-First Storage & Offline Operation
- **IndexedDB**: Stores complete standalone HTML simulation bundles for persistent offline execution.
- **LocalStorage**: Retains catalog metadata, dossiers, search state, and UI theme preferences.
- **Zero Server Overhead**: The entire platform runs statically inside client browsers—compatible with GitHub Pages, local file links, or static hosting.

###  Engineering Dossiers & Mathematical Typesetting
- **KaTeX Integration**: Renders mathematical equations and physical governing relations ($$x(\theta)$$, $$\sigma = \frac{F}{A}$$, slider-crank position formulas, Wankel epitrochoids, etc.) with real-time math previews.
- **Interactive Dossier Modal**: Inspect component breakdowns, material specs, kinematic degrees of freedom, and mechanical schematics.
- **In-App Runner & Pop-Out Mode**: Run simulations directly inside an embedded CRT modal runner or open full-screen in a detached window.

###  Catalog Management
- **Batch HTML Import**: Drag and drop or upload multiple `.html` / `.htm` standalone webpmesim simulations at once. The engine automatically parses titles, subtitles, formulas, and metadata tags from the files.
- **Real-Time Search & Filtering**: Instant search across titles, scope descriptions, and KaTeX mathematical formulas (press `/` to focus search).
- **JSON Catalog Export & Import**: Backup or sync catalog databases across machines with a single click.
- **Sort Controls**: Sort items by recently added, alphabetical order, or mechanical parts count.


### 🚀 Pre-Installed Core Simulation Units
The repository includes three high-fidelity physics & engineering simulation models ready to run out of the box:

1. **Slider-Crank Mechanism** (`slider-crank` // Mechanisms):
   - Exact kinematics and inertial dynamics of an in-line crank, connecting rod and reciprocating piston.
   - Governing relation: $$x(\theta) = r\cos\theta + \sqrt{l^2 - r^2\sin^2\theta}$$
   - Features: pin double-shear analysis, connecting rod obliquity angle $\varphi$, exact kinematic derivatives, and 8/8 independent numerical validation checks.

2. **Ninety-Degree V4 Reciprocating Engine** (`v4-engine` // Engines):
   - Kinematic geometry, multi-cylinder inertial dynamics, and primary/secondary balancing.
   - Governing relation: $$\sum_{i=1}^4 \mathbf{F}_{1,i} \equiv \mathbf{0},\quad F_{x,2}(\theta) = -2\sqrt{2}\,m_r r \omega^2 \lambda \sin 2\theta$$
   - Features: 15 mechanical parts, $180^\circ$ flat-plane crankshaft with two shared crankpins, full primary reciprocating shaking force cancellation, second-order horizontal shaking analysis, and 8/8 validation checks.

3. **Wankel Rotary Engine** (`wankel-engine` // Rotary):
   - Epitrochoid kinematics, thermodynamic chamber volume cycles, apex seal dynamics, indicated gas torque, and dynamic balancing.
   - Governing relation: $$V(\theta) = e R B\left(2\sqrt{3} - \frac{3\sqrt{3}}{2}\sin\left(\frac{2\theta}{3}\right)\right)$$
   - Features: 2-lobed epitrochoid stator housing, triangular rotor with $1:3$ gear kinematics, four-stroke cycle over $1080^\circ$ shaft rotation, apex seal centrifugal liftoff and Hertzian contact stresses, and 8/8 validation checks.
---

## Live Demo & Quick Start

### 1. View Online
Visit the live GitHub Pages instance:
[https://spocku.github.io/webpmesim-library/](https://spocku.github.io/webpmesim-library/)

### 2. Run Locally
Clone the repository and open `index.html` (or `webpmesim-library.html`) directly in any modern browser:

```bash
git clone https://github.com/spocku/webpmesim-library.git
cd webpmesim-library
# Open in your preferred browser:
# Windows
start index.html
# macOS
open index.html
# Linux
xdg-open index.html
```

---

## Keyboard Shortcuts

| Shortcut | Action |
| :--- | :--- |
| <kbd>/</kbd> | Focus real-time search field |
| <kbd>Esc</kbd> | Dismiss active modal (Runner / Dossier / Register form) |

---

## Technical Stack

- **Markup & Layout**: Pure HTML5 & CSS3 with CSS custom properties (fluid typography via `clamp()`, CSS grid and flexbox).
- **Typography**: `@fontsource` web fonts (`Orbitron`, `Share Tech Mono`, `Roboto Mono`, `Chakra Petch`, `Saira Extra Condensed`).
- **Math Engine**: KaTeX (`katex.min.js` + `auto-render.min.js`).
- **Storage**: Browser IndexedDB (`IDBDatabase`) + `localStorage`.
- **Frameworks / Libraries**: 100% vanilla JavaScript; zero Node/npm runtime dependencies required.

---

## License

MIT License. Free to use, adapt, and build upon for engineering educational tools and interactive simulation suites.
