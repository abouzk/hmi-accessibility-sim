# Accessibility Experience Simulator

## Overview
This Pygame project simulates the physical and sensory barriers often experienced by nonspeaking individuals and those with motor dysfunctions. By artificially introducing motor control limitations and environmental stressors (sensory/cognitive load), this simulator demonstrates how physical barriers can lead to unfair or lowered performance metrics in digital environments.

The project is built modularly, allowing users to experience just the motor dysfunction, or layer on additional visual and auditory distortions.

## Tech Stack
* **Language:** Python 3.x
* **Library:** Pygame
* *(To add any other libraries we end up using, like NumPy for audio manipulation)*

## Development Phases

### Phase 1: Core Motor Dysfunction (The Base Layer)
This phase focuses on the physical barriers of interacting with standard interfaces. The goal is to make the mouse feel uncooperative and heavy.
* **Mouse Lag:** Introduce a delay between the user's physical mouse movement and the cursor's movement on-screen. 
* **Mouse Jitter:** Add randomized `(x, y)` offsets to the cursor's coordinates to simulate tremors or lack of fine motor control.
* **Hitbox Alteration:** Require the user to hover over a target for a sustained period, or make clicks randomly fail to register, simulating difficulties with precise timing.

### Phase 2: Video/Visual Distortion (Sensory Layer 1)
This phase introduces visual stressors to simulate environmental/cognitive overload. These effects can be toggled on or off over the base motor layer.
* **Screen Shake:** Randomly shift the display surface coordinates during specific "stress" triggers.
* **Vision Tunneling/Blurring:** Use Pygame's surface alpha and drawing features to darken the edges of the screen or overlay a semi-transparent layer that reduces clarity.
* **Flashing/Distracting Assets:** Introduce sudden, brief visual artifacts on the screen to break focus.

### Phase 3: Audio Distortion (Sensory Layer 2)
This phase adds an auditory component to the cognitive load simulation, which can be stacked with the motor and visual layers.
* **Overwhelming Background Noise:** A constant, looping track of overlapping sounds (e.g., crowds, static, machinery) that fluctuates in volume.
* **Delayed Audio Feedback:** If the game features audio cues for clicking or hovering, delay these sounds to disorient the user.
* **Audio Distortion:** Play audio files with added echo, pitching, or bit-crushing effects.

## Getting Started

1. **Clone the repository:**
2. **Set up a virtual environment (recommended {idk why it says recommeded here, must research this}):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```

3. **Install dependencies {what}:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the simulation:**
   ```bash
   python main.py
   ```

## Project Structure
* `main.py`: The entry point and main Pygame event loop.
* `settings.py`: Configuration variables (screen size, FPS, toggle states for distortions).
* `motor_sim.py`: Logic for mouse lag, jitter, and click registration.
* `visual_fx.py`: Logic for screen shaking, overlays, and visual stressors.
* `audio_fx.py`: Logic for background noise and distorted sound cues.
* `assets/`: Directory for images, fonts, and sound files.
