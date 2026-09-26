# CS460 - Assignment 2: Dynamic Cube Art Visualization

An interactive 3D WebGL Cube Art Visualization built with **The X Toolkit (XTK)** framework, featuring mathematical generative formations, dynamic color harmonics, individual cube kinematics, camera auto-orbiting, real-time shockwave ripples, and an ambient Web Audio synthesizer.

---

## 🚀 Files

- **`index.html`** *(Primary Assignment)*: The complete XTK WebGL Cube Art Studio.
- **`bonus.html`** *(Bonus / Comparison)*: Companion implementation using **Three.js** with hardware-accelerated instanced meshes and dynamic PBR lighting.

---

## ✨ Features

### 1. Mathematical Formations & Morphing
Smooth fluid kinematic transitions interpolate the 256 cubes across 7 distinct 3D formations:
1. **Hypercube Wave Matrix**: 3D sinusoidal ripple harmonics with radial distance and angular phase modulation.
2. **Cosmic Vortex**: 3-armed logarithmic Fibonacci galaxy spiral with vertical gravitational drift.
3. **DNA Double Helix**: Intertwined double-stranded helical staircase with periodic connecting base rungs.
4. **Tesseract Shells**: Concentric 4D hypercube frames expanding and breathing along diagonal axes.
5. **Toroidal Ring**: Cubes woven along the major and minor radii of a 3D torus ribbon.
6. **Supernova Sphere**: Fibonacci golden ratio distribution on a spherical shell pulsing rhythmically.
7. **Audio Spectrum Arena**: Radial stepped equalizer ring reacting dynamically to synthesized frequencies.

### 2. Chromatic Harmonics & Color Themes
- **Neon Cyberpunk**: Electric Cyan (`#00f3ff`) & Hot Magenta (`#ff007f`) with solar yellow highlights.
- **Vaporwave Sunset**: Sunset Peach, Hot Pink, and deep twilight Violet.
- **Quantum Aurora**: Dynamic HSL spectrum phase-shifted across 3D distance, height, and time.
- **Molten Magma**: Volcanic obsidian core grading to crimson, flaming orange, and molten gold.
- **Bioluminescent Abyss**: Phosphorescent aqua, electric azure, and deep oceanic navy.
- **Matrix Emerald**: Digital terminal jade, cyber emerald, and fluorescent lime.
- **Prismatic Rainbow**: Continuous 360° chromatic spatial rainbow.

### 3. Kinematics & Transformations
- Each cube maintains its own 3D rotation angles along $(X, Y, Z)$ and spins independently in local space.
- The 4x4 transformation matrix (`cube.transform.matrix`) is calculated with rotation, scale, and world-space translation.
- Interactive **Click-to-Shockwave**: Clicking anywhere on the canvas radiates an expanding radial wave through the grid.

### 4. Generative Ambient Synthesizer (Web Audio API)
- Built-in atmospheric sci-fi ambient chord generator (harmonic F minor 9th / C minor voicing) with gentle detune chorus and lowpass filter sweeps.
- Real-time `AnalyserNode` extracts audio frequency energy to modulate cube heights, wave amplitudes, and color luminescence.
- Click the audio icon in the top-right toolbar or press `A` to toggle sound.

### 5. Controls & User Interface
- **dat.GUI Controller** (`xtk_xdat.gui.js`): Control animation speed, wave frequency, amplitude, spin rates, camera orbit speed, and color themes.
- **Glassmorphism HUD**: Live FPS counter, active cube count, current formation, and palette indicator.
- **Mouse Navigation**:
  - *Left Click + Drag*: Orbit / rotate the camera.
  - *Scroll Wheel / Right Click + Drag*: Zoom in / out.
  - *Middle Click + Drag*: Pan the scene.
  - *Canvas Click*: Spawn a 3D shockwave ripple.

---

## ⌨️ Keyboard Shortcuts

| Key | Action |
|:---:|:---|
| <kbd>Space</kbd> | Pause / Resume animation |
| <kbd>M</kbd> | Cycle next formation |
| <kbd>C</kbd> | Cycle next color palette |
| <kbd>A</kbd> | Toggle ambient audio synth |
| <kbd>O</kbd> | Toggle camera auto-orbit |
| <kbd>R</kbd> | Randomize parameters |
| <kbd>F</kbd> | Toggle fullscreen |
| <kbd>1</kbd> - <kbd>7</kbd> | Jump directly to formations 1 through 7 |
| <kbd>?</kbd> / <kbd>Esc</kbd> | Open / Close keyboard shortcuts cheat sheet |

---

## 🛠️ Frameworks & CDNs Used

- **XTK (The X Toolkit)**: `https://get.goXTK.com/xtk_edge.js`
- **XTK Dat.GUI**: `https://get.goXTK.com/xtk_xdat.gui.js`
- **Three.js** (for `bonus.html`): `https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js`
