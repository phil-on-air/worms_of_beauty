## Worms of Beauty v2.1 — UI Guide

`Worms of Beauty v2.1` is a generative art piece built with p5.js. The canvas fills the entire browser window, and a floating control panel on the right lets you explore different looks, record videos, and save still images.

### Layout

- **Main canvas**: The animated particle field (“worms”) occupies the full background.
- **Control panel (right side)**: Floating glassy panel with grouped controls.
- **Recording indicator (top‑left)**: Shows a red dot and timer while recording.
- **Panel toggle (top‑right)**: A small ☰ button appears when the panel is hidden so you can bring it back.

---

### Seed

The **Seed** section controls the random seed behind the composition. This is how you get reproducible or new variations.

- **Seed input**  
  - Text field showing the current numeric seed.  
  - Type a positive integer and press Enter (or unfocus) to regenerate the scene with that seed.

- **← Prev / Next → buttons**  
  - Step the seed down or up by 1.  
  - Each click regenerates the scene with the new seed.

- **Random Seed button**  
  - Picks a random seed and regenerates the scene.  
  - Use this to quickly discover new compositions.

---

### Parameters

These sliders control how the “worms” move, how dense they are, and how they feel over time.

- **Particle Count**  
  - Number of particles in the scene.  
  - Higher values look richer but may be heavier on performance.

- **Drift Speed**  
  - Overall movement speed of the particles.  
  - Lower values feel calmer; higher values feel more turbulent and active.

- **Noise Scale**  
  - How “tight” or “broad” the underlying flow field is.  
  - Smaller values → large, smooth flows. Larger values → more intricate, local motion.

- **Time Flow**  
  - How quickly the noise field itself evolves over time.  
  - Very small values drift slowly; larger values cause more rapid changes in the flow.

- **Particle Size**  
  - Visual size of each particle.  
  - Use smaller values for fine fog; larger values for chunkier, more visible dots.

- **Base Opacity**  
  - Overall brightness/opacity of the particles.  
  - Increasing this makes trails more solid; decreasing makes them more ethereal.

- **Trail Dissolve**  
  - Controls how quickly old trails fade out.  
  - `0`: almost no active fade, rich accumulation.  
  - Higher values: faster fade, lighter trails and less build‑up.

Each slider displays its current numeric value to the right for reference.

---

### Atmosphere (Colors)

The **Atmosphere** section defines the color palette and background.

- **Warm Tone**  
  - Color picker for the warm end of the gradient.  
  - Particles blend between warm and cool based on their position and motion.

- **Cool Tone**  
  - Color picker for the cool end of the gradient.  
  - Adjust together with Warm Tone for different moods (e.g., teal–orange, purple–blue).

- **Background**  
  - Color picker for the canvas background.  
  - Changing this also reinitializes the system to keep the look coherent.

Each color shows its current hex value next to the picker.

---

### Recording

You can export animated sequences as WebM videos (best in Chrome / Edge).

- **⏺ Start Recording / ⏹ Stop Recording button**  
  - Click **⏺ Start Recording** to begin capturing the canvas.  
  - While recording:  
    - Button label changes to **⏹ Stop Recording** and turns red.  
    - A recording pill appears at the top‑left with a blinking red dot and an `mm:ss` timer.  
  - Click **⏹ Stop Recording** to finish and trigger a WebM download.

- **Frame Rate (30 / 60 fps)**  
  - Choose the target frame rate for the recording.  
  - 60 fps is smoother but produces larger files.

- **Quality (Medium / High / Ultra)**  
  - Sets video bitrate (file size vs. quality).  
  - Use **Medium** for quick tests, **High/Ultra** for final captures.

- **Format note**  
  - Output is **WebM**. Playback works best in Chrome/Edge; some apps may need conversion.

---

### Actions

Final utility controls for resetting, clearing, and saving stills.

- **Reset**  
  - Restores all parameters and colors to their original defaults.  
  - Seed is reset to the default, and the scene is fully regenerated.

- **Clear**  
  - Clears the canvas with the current background color.  
  - Particles continue moving from that clean state.

- **Download PNG**  
  - Saves a high‑resolution still image of the current canvas as a PNG file.  
  - Filenames start with `worms-of-beauty-<seed>.png`, so different seeds are easy to track.

---

### Basic usage tips

- Start by using **Random Seed** and minor tweaks to **Drift Speed**, **Trail Dissolve**, and **Base Opacity** to feel how the piece responds.
- When you find a look you love, note the **Seed** value and use **Download PNG** or make a **Recording** so you can revisit and share that exact configuration.

