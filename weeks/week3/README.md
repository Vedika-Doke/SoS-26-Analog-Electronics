# Week 3 — BJT: DC bias, load lines

**Concepts:** NPN/PNP operation, regions (cutoff / active / saturation), β, Ebers-Moll → simplified active-region model, voltage-divider bias, load line, Q-point sensitivity.

## Reading & slides
- S&S Ch. 6 — operation + DC analysis
- Slides: `mc_bjt_1`, `missedclass/ee204_bjt_1`
- HW: `BJT.pdf` (+ `BJT_ans.pdf`)

## LTspice lab
1. Plot I_C vs V_CE for stepped I_B (`.dc V1 0 10 0.05` with `.step` on I_B) — family of curves.
2. Voltage-divider biased CE stage: `.op` Q-point; sweep β by 2×, observe shift.

## Deliverable
Annotated output-characteristics plot + table showing Q-point stability across β.
