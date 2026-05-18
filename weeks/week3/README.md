# Week 3 — Op-amps I: Ideal linear circuits

The big one. Master the **golden rules** (V+ = V−, no current into inputs) and almost every linear op-amp circuit becomes one-line algebra.

## Concepts
- Golden rules, virtual short, negative feedback intuition.
- Inverting amplifier, non-inverting amplifier, voltage follower (buffer).
- Summing amplifier, difference amplifier.
- **Integrator** and **differentiator** — these are the workhorses of the analog DE solver project.

## Reading & slides
- **Sergio Franco**, *Design with Op-Amps and Analog ICs*, Ch. 1–2 (op-amp basics + resistive networks). [Drive folder](https://drive.google.com/drive/folders/17T1Mnk_SVdqIi2b4Fn-qmpbAn6tkMbvd?usp=drive_link)
- **Sedra & Smith** Ch. 2 for cross-reference. [Drive folder](https://drive.google.com/drive/folders/1AWumX1rr4MDby0pJfxpg7-JE0xuE8mdn?usp=drive_link)
- **Prof. M. B. Patil's EE204 slides:** `mc_opamp_1` → `mc_opamp_3`. [Drive mirror](https://drive.google.com/drive/folders/1jPG5-WahBaDfoCOUDKTlCq3mqKhl5vyN?usp=drive_link) · [Source](https://www.ee.iitb.ac.in/~sequel/course_material.html)
- HW (from EE204): `2_instrumentation.pdf` (+ `2_sol.pdf`) — try the easier problems

## LTspice lab
Use the built-in `UniversalOpAmp2` symbol so we can later tweak its non-idealities without rewiring.
1. **Inverting amp**, gain −10. Drive with a 1 kHz sine, verify gain and 180° phase shift.
2. **Non-inverting amp**, gain +5. Compare input impedance to the inverter (infinite vs R_in).
3. **Voltage follower** driving a small load — measure output stays at input.
4. **Summing amp** — add two DC voltages, verify V_out = −(V1 + V2).
5. **Integrator** — drive with a 1 kHz square wave, observe triangle output. Add a large feedback resistor (e.g. 1 MΩ) across the cap to stop DC drift; explain why.

## Deliverable
Integrator producing a clean triangle wave from a square input. Show: schematic, V_in vs V_out plot, hand-calc'd peak amplitude vs simulated.
