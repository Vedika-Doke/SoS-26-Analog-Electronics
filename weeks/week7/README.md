# Week 7 — Real op-amps + active filters

**Concepts:** Finite open-loop gain, GBW, slew rate, input offset, input bias current, output saturation — and *when each bites*. Sallen-Key LP/HP/BP; Q and damping.

## Reading & slides
- Franco Ch. 5–6 (real op-amp limitations) + filter chapter
- Slides: `mc_opamp_4` → `mc_opamp_6`
- HW (bonus): `Output_stage.pdf`, `Current_mirror.pdf`

## LTspice lab
1. Take Week-6 non-inverting amp; sweep GBW of `UniversalOpAmp2`, watch bandwidth shrink. Plot GBW = constant.
2. Slew-rate experiment: large fast step → triangular output → extract SR.
3. Sallen-Key 2nd-order LPF at 1 kHz, Q = 0.707; verify −40 dB/dec slope.

## Deliverable
Sallen-Key filter design — pick specs (e.g. audio anti-alias at 15 kHz), simulate, justify components.
