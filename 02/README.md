# CS460 - Assignment 2: Pedestrian 3D Cube City & Randomized Streets (XTK)

An interactive, procedural 3D WebGL city simulation built with **The X Toolkit (XTK)** framework, created directly from the specifications and layout sketched in [`assignment 2.pdf`](file:///C:/Users/denni/OneDrive%20-%20University%20of%20Massachusetts%20Boston/UMass%20Boston/Computer%20Science/cs460student/02/assignment%202.pdf).

---

## 🏙️ What's New in this Build

### 1. Zero-Leak Cube Pooling (Orphaned Beacons Fixed)
- All buildings, setbacks, rooftop antennas, glowing spire beacons, street elements, and traffic cars are managed through a unified **pre-allocated cube pool** (~480+ cubes).
- When the city is re-randomized, all pool members are either reconfigured to their new coordinates or hidden with `visible = false`. **No beacons or antennas ever linger in the sky.**

### 2. Randomized Street Network
- The street grid dynamically reconfigures on every randomization:
  - **Randomized Intersections**: 2 to 4 cross-streets at varying depths with T-junctions (branching left, branching right like in the PDF sketch, or 4-way crossways).
  - **Painted Crosswalks**: Realistic white zebra-stripe pedestrian crossings flanking every intersection.
  - **Modular Sidewalk Curbs**: Flanking the avenue with openings that allow you to walk into any cross-street.
  - **Dashed Lane Markings & Streetlights**: Center stripes down the avenue and side streets with glowing warm streetlight poles along sidewalks.

### 3. Colossal Urban Scale & Abundance (340+ Buildings)
- Spanning nearly **1,000 units wide** ($X: -450$ to $+450$) and over **1,100 units deep** ($Z: +400$ to $-740$).
- **Signature Foreground Buildings**: Always preserves the 6 authentic buildings from `assignment 2.pdf`:
  - *Left Foreground*: Purple compact cube
  - *Left Midground*: Leaf Green rectangular block
  - *Left Horizon*: Canary Yellow soaring skyscraper
  - *Right Foreground*: Ruby Red cube
  - *Right Midground*: Sky Blue skyscraper
  - *Right Crossway*: Elongated Amber Orange horizontal building past the intersection
- **Metropolitan Skyline**:
  - Megatall skyscrapers soaring up to 340+ units high with architectural setbacks and glowing spires.
  - Commercial and residential mid-rises (65–160 units).
  - Low-rise shops, lofts, and urban pavilions (22–60 units).
  - Vibrant multi-colored building palette (Yellow, Blue, Green, Purple, Orange, Red, Cyan, Coral, Mint, Cobalt, Gold).

### 4. True Human-Scale Pedestrian Camera
- **Street-Level Eye Height**: Set to `7.8 units` above the street. Skyscrapers tower over 30× your height, giving a true pedestrian street perspective.
- **Pedestrian Physics & Kinematics**:
  - Smooth ground acceleration and friction deceleration (realistic human momentum rather than rigid teleportation).
  - **Bipedal Gait Head-Bobbing**: Subtle vertical head-bob ($0.32$ units) and lateral shoulder sway ($0.14$ units) synchronized to your step speed.
  - **Pedestrian Jump**: Press <kbd>Space</kbd> or click "Jump" to leap with gravity.
  - **Building Collision Detection**: Prevents walking through skyscraper walls, keeping you naturally along streets, sidewalks, and crossways.
  - **Look Controls**: Click and drag on the screen to look around freely (yaw & pitch), allowing you to tilt your head all the way up to gaze at skyscraper rooftops against the sky.

---

## ⌨️ Controls Summary

| Input | Action |
|:---:|:---|
| <kbd>W</kbd> | Walk forward down the road |
| <kbd>S</kbd> | Walk backward |
| <kbd>A</kbd> | Strafe left |
| <kbd>D</kbd> | Strafe right |
| <kbd>Shift</kbd> | Sprint (Jogging pace) |
| <kbd>Space</kbd> | Jump |
| <kbd>Mouse Drag</kbd> | Look around (tilt up at towers, look left/right) |
| <kbd>Q</kbd> / <kbd>E</kbd> or <kbd>&larr;</kbd> <kbd>&rarr;</kbd> | Turn camera left / right |
| <kbd>&uarr;</kbd> <kbd>&darr;</kbd> | Look up / down |
| <kbd>G</kbd> | **Randomize City &amp; Street Grid** |
| <kbd>R</kbd> | **Reset Position to Street Level** |
| <kbd>V</kbd> | Toggle Pedestrian Walk / Aerial Drone camera |
| <kbd>N</kbd> | Cycle Atmosphere (Day / Sunset / Cyberpunk Night) |
| <kbd>T</kbd> | Toggle traffic animation |
| <kbd>?</kbd> | Open Controls cheat sheet |

---

## 🚀 Files

- **[`index.html`](file:///C:/Users/denni/OneDrive%20-%20University%20of%20Massachusetts%20Boston/UMass%20Boston/Computer%20Science/cs460student/02/index.html)**: Main XTK WebGL assignment submission.
- **[`assignment 2.pdf`](file:///C:/Users/denni/OneDrive%20-%20University%20of%20Massachusetts%20Boston/UMass%20Boston/Computer%20Science/cs460student/02/assignment%202.pdf)**: Assignment specification and visual sketch.
- **[`agent.html`](file:///C:/Users/denni/OneDrive%20-%20University%20of%20Massachusetts%20Boston/UMass%20Boston/Computer%20Science/cs460student/02/agent.html)**: Mathematical cube art visualization (bonus archive).
