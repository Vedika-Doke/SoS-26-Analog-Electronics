# Week 0 — LTspice Setup

Onboarding before the program starts. Get LTspice installed and run one simulation.

## Steps

### Step 1: Install LTspice
Install LTspice XVII or latest from Analog Devices (Windows / Mac).
**Installation guide (video):** https://drive.google.com/file/d/1zGUMgb3VqzTxMfs1BEleY2YaYObVNJ2c/view

### Step 2: Learn the basics
Walk through the official Analog Devices tutorial — interface, placing components, running simulations, viewing waveforms.
**Getting Started Tutorial:** https://www.analog.com/en/resources/media-center/videos/series/ltspice-getting-started-tutorial.html

### Step 3: Add external components / models
Some parts (specific op-amps, transistors, diodes) aren't in the default library. Learn how to import them — essential for the circuits we'll build.
**Adding components (video):** https://drive.google.com/file/d/1D-YBuiAPc-czAoGhfAhSZUVWT8j0mYcg/view

## Pre-loaded SPICE models

Common parts (LM324, uA741, BC547, 1N914, Zener, LEDs, MOSFETs) are already packaged in [`ltspice/models/`](../../ltspice/models/) with usage instructions.

## Checkpoints

- [ ] LTspice installed and opens correctly
- [ ] Completed the Getting Started tutorial
- [ ] Built one simple circuit (resistor + voltage source) and ran a simulation
- [ ] Know how to add a new component/model

Reach out if you hit any installation or setup issue. Happy simulating ⚡

---

## What's coming — the 8-week journey

The course is **op-amp heavy**. We touch diodes, BJTs and MOSFETs lightly in Week 2 just so you recognize them in a schematic — the real work starts at Week 3 and stays in op-amp land.

| Week | Topic | You'll build |
|------|-------|--------------|
| 1 | Linear networks + LTspice fluency | RC step response, τ from waveform |
| 2 | Diodes + BJT/MOS (light touch) | Bridge rectifier + your own clipper |
| 3 | Op-amps I — ideal linear | Integrator turning square waves into triangles |
| 4 | Op-amps II — real limits *(midterm window)* | Slew-rate measurement |
| 5 | Op-amps III — non-linear: Schmitt, comparators, oscillators (+ ADC/DAC primer) | Relaxation oscillator at target frequency |
| 6 | Active filters + instrumentation amp | Inst. amp with CMRR ≥ 60 dB |
| 7 | Final project — design + first build | Choice locked, half built |
| 8 | Final project — polish + report + demo | Working circuit + presentation |

**Final project — pick one in Week 7:**
1. **Analog differential-equation solver** — integrators + summers wired up to physically solve an ODE (e.g. a damped mass-spring oscillator). Voltage at each node *is* a variable.
2. **555 timer from scratch** — recreate the legendary NE555 internals using discrete op-amps, comparators and a latch. Configure as astable oscillator or monostable one-shot.
3. **Lotka-Volterra solver 🌶️** *(stretch challenge)* — predator-prey ODEs. Same idea as Option 1 but the `xy` terms are non-linear, so you'll learn to use an **analog multiplier** (AD633). The reward: an X-Y plot showing the famous predator-prey limit cycle.

**Midterm submission** likely happens around the Week 4 / Week 5 boundary — keep your weekly deliverables organized so you can compile a summary easily.

Each week: ~6–8 hours of effort, one short meet, one deliverable (hand calc + LTspice schematic + sim plots).

> **Meet attendance:** we'll have **at least one short meet per week** — could be 20 min, could be longer if you have lots to show. Please try to make every one: I submit an involvement / interactions log to the SoS coordinators, and consistent participation keeps that simple for both of us.

> **Buffer week — week of June 12–19** — no new content. Catch-up, midterm submission, or an optional topic if you're ahead.
