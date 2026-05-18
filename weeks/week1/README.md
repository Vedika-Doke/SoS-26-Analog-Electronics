# Week 1 — Linear networks + LTspice fluency

**Concepts:** KVL/KCL, Thevenin/Norton, superposition, RC transient & frequency response, phasors.

## Reading & slides
- S&S Ch. 1 (signals + amplifier model — gain, Z_in, Z_out)
- Slides: `mc_thev_1`, `mc_superposition_1`, `mc_rc_1`, `mc_phasors`
- HW: `1_basic.pdf` (+ `1_sol.pdf`)

## LTspice lab
1. RC low-pass: `.tran` step response + `.ac dec 100 1 1MEG`; verify f_c = 1/(2πRC).
2. Thevenin equivalent: 3-resistor + source network, find V_th, R_th by simulation.

## Deliverable
Bode plot of RC with cursor markers at f_c, hand calc matching within 5%.

## Files
- `labs/` — LTspice schematics
- `deliverable.md` — mentee writeup
