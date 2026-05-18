# Week 5 — MOSFETs + frequency response

**Concepts:** MOSFET square-law model, biasing, CS amplifier (quick compare vs CE), Bode plots in detail, dominant pole, GBW, Miller effect (intuition).

## Reading & slides
- S&S Ch. 5 — MOSFET + CS amplifier; revisit Bode intuition from Ch. 1
- Slides: `mc_bode_1`, `missedclass/mc_bode_1.pdf`
- HW: `MOS.pdf`, `3_bode+rectifier.pdf` (Bode portion)

## LTspice lab
1. CS amplifier mirror of Week-4 CE design; compare gain, Z_in, distortion.
2. CE amplifier frequency response: `.ac dec 50 1 1G`. Identify LF pole (coupling cap), HF roll-off.

## Deliverable
Annotated Bode plot of Week-4 CE amp with poles labeled + cause of each explained.
