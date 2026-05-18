# Week 2 — Diodes, rectifiers, wave-shaping

**Concepts:** PN junction, exponential I-V, constant-voltage-drop model, small-signal r_d, Zener regulation, half/full-wave rectifier, peak detector, clipper, clamper.

## Reading & slides
- S&S Ch. 4 — diode models, rectifiers, limiting/clamping
- Slides: `mc_diodes_1`, `mc_diodes_2`
- HW: `3_bode+rectifier.pdf` (rectifier portion)

## LTspice lab
1. Full-wave bridge rectifier with smoothing cap → ripple vs C. Sweep with `.step param C 10u 1000u 10`.
2. Zener shunt regulator: V_out vs V_in (`.dc`), and vs I_load.
3. Bonus: precision rectifier preview (op-amp + diode) — revisit Week 6.

## Deliverable
Ripple-vs-C plot + a custom clipper limiting a ±5 V sine to ±2 V.
