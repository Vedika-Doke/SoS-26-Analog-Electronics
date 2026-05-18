# Week 0 — LTspice Setup

Onboarding before the program starts. Get LTspice installed and run one simulation.

**Original handout:** [`Week0.pdf`](Week0.pdf) (GitHub's PDF viewer doesn't preserve clickable links — use the links below instead)

## Steps

### Step 1: Install LTspice
Install LTspice XVII or latest from Analog Devices (Windows / Mac).
**Installation guide (video):** https://drive.google.com/file/d/1D-YBuiAPc-czAoGhfAhSZUVWT8j0mYcg/view

### Step 2: Learn the basics
Walk through the official Analog Devices tutorial — interface, placing components, running simulations, viewing waveforms.
**Getting Started Tutorial:** https://www.analog.com/en/resources/media-center/videos/series/ltspice-getting-started-tutorial.html

### Step 3: Add external components / models
Some parts (specific op-amps, transistors, diodes) aren't in the default library. Learn how to import them — essential for the circuits we'll build.
**Adding components (video):** https://drive.google.com/file/d/1zGUMgb3VqzTxMfs1BEleY2YaYObVNJ2c/view

## Pre-loaded SPICE models

Common parts (LM324, uA741, BC547, 1N914, Zener, LEDs, MOSFETs) are already packaged in [`ltspice/models/`](../../ltspice/models/) with usage instructions.

## Checkpoints

- [ ] LTspice installed and opens correctly
- [ ] Completed the Getting Started tutorial
- [ ] Built one simple circuit (resistor + voltage source) and ran a simulation
- [ ] Know how to add a new component/model

Reach out if you hit any installation or setup issue. Happy simulating ⚡
