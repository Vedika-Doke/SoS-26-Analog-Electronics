# Week 5 — Op-amps III: Non-linear circuits (Schmitt, comparators, oscillators)

So far we've used op-amps with negative feedback. This week flips the script: **positive feedback**, **open-loop comparators**, and **regenerative switching**. These building blocks power the 555 timer and a huge chunk of analog signal-conditioning.

## Concepts
- **Comparator** — open-loop op-amp as a 1-bit decision maker. Why you should use a dedicated comparator IC (LM311) instead of a slow op-amp in practice.
- **Schmitt trigger** — comparator + positive feedback → hysteresis (two distinct thresholds, V_TH and V_TL). Kills chatter on noisy edges.
  - Inverting and non-inverting variants.
  - How to calculate the thresholds from the resistor divider.
- **Relaxation oscillator** — Schmitt trigger + RC charging loop → square wave with frequency set by RC and the hysteresis window. This is *exactly* how the 555 timer works internally.
- **Precision rectifier** preview (op-amp + diode) — overcoming the 0.7 V diode drop.

## Reading & slides
- **Sergio Franco** — chapter on comparators / non-linear circuits. [Drive folder](https://drive.google.com/drive/folders/17T1Mnk_SVdqIi2b4Fn-qmpbAn6tkMbvd?usp=drive_link)
- **Prof. M. B. Patil's EE204 slides:** `mc_opamp_6`. [Drive mirror](https://drive.google.com/drive/folders/1jPG5-WahBaDfoCOUDKTlCq3mqKhl5vyN?usp=drive_link) · [Source](https://www.ee.iitb.ac.in/~sequel/course_material.html)
- Reference: TI LM555 datasheet (the 555 has a Schmitt + comparator structure we'll meet in the project). https://www.ti.com/lit/ds/symlink/lm555.pdf

## LTspice lab
1. **Open-loop comparator** — `UniversalOpAmp2` with no feedback; threshold = 0 V. Drive with a sine, observe square output.
2. **Inverting Schmitt trigger** — design for V_TH = +2 V, V_TL = −2 V with V_sat = ±10 V. Verify with a slow noisy sine; show output doesn't chatter on the zero-crossing.
3. **Relaxation oscillator** — Schmitt trigger + RC feedback. Design for f ≈ 1 kHz. Measure period, compare with hand calc.
4. **Bonus: precision half-wave rectifier** — works on signals smaller than 0.7 V.

## Deliverable
Relaxation oscillator with measured frequency within 10% of design. Show: schematic, V_cap (triangle-ish ramp) and V_out (square) on the same plot, hand calc of period.
