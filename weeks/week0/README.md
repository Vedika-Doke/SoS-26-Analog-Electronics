# Week 0 — LTspice Setup

Onboarding before the program starts. Get LTspice installed and run one simulation.

**Handout:** [`Week0.pdf`](Week0.pdf)

## Steps

1. **Install LTspice** — LTspice XVII or latest from Analog Devices (Windows / Mac).
2. **Getting Started Tutorial** — official Analog Devices walkthrough: interface, placing components, running simulations, viewing waveforms.
3. **Adding external components/models** — essential for parts not in the default library (specific op-amps, transistors, diodes).

## Walkthrough videos

Two short videos (installation + first-sim tutorial) live on Google Drive at `LTSpice_Guide/LTSpice_Installation_Material/`. Too large for git — ask the mentor for the Drive link.

## Pre-loaded SPICE models

Common parts (LM324, uA741, BC547, 1N914, Zener, LEDs, MOSFETs) are already packaged in [`ltspice/models/`](../../ltspice/models/) with usage instructions.

## Checkpoints

- [ ] LTspice installed and opens correctly
- [ ] Completed the Getting Started tutorial
- [ ] Built one simple circuit (resistor + voltage source) and ran a simulation
- [ ] Know how to add a new component/model
