# Week 6 — Op-amps: ideal + classic topologies

**Concepts:** Golden rules, virtual short; inverting / non-inverting / summing / difference / integrator / differentiator; instrumentation amplifier.

## Reading & slides
- Franco Ch. 1–2 (op-amp basics + resistive networks); S&S Ch. 2 for cross-reference
- Slides: `mc_opamp_1` → `mc_opamp_3`
- HW: `2_instrumentation.pdf` (+ `2_sol.pdf`)

## LTspice lab
Use `UniversalOpAmp2` (parameterizable, so we can later study finite GBW).
1. Inverting amp, gain −10.
2. Non-inverting summer.
3. Integrator: square in → triangle out. Add large feedback R to prevent DC drift; explain why.
4. 3-op-amp instrumentation amplifier — verify CMRR by driving both inputs with same signal.

## Deliverable
Instrumentation amp with measured CMRR ≥ 60 dB at 1 kHz.
