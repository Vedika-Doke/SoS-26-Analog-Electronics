# Week 5 — Instrumentation amplifier + active filters

Before we flip op-amps into non-linear territory, finish the *linear* applications. Two big workhorses: the instrumentation amplifier (sensor front-ends) and active filters (signal conditioning).

## Concepts
- **Difference amplifier** recap — gain = R_f/R_in *only if* resistors are matched. Tolerance kills CMRR.
- **3-op-amp instrumentation amplifier** — two buffers + a difference amp; gain set by a single resistor. CMRR is huge because matching only matters in the back stage.
- **CMRR** intuition — differential signals survive, common-mode noise gets rejected. Compute CMRR = 20·log(A_diff / A_cm).
- **Active filters** — why active beats passive (gain, no inductors, easy cascading).
- **Sallen-Key topology** — 2nd-order low-pass / high-pass / band-pass. Pick R and C to set f_c and Q.

## Reading & slides
- **Sergio Franco** — instrumentation amplifier chapter + filter chapter. [Drive folder](https://drive.google.com/drive/folders/17T1Mnk_SVdqIi2b4Fn-qmpbAn6tkMbvd?usp=drive_link)
- HW (from EE204): `2_instrumentation.pdf` (+ `2_sol.pdf`) — the harder problems this time.

## LTspice lab
1. **3-op-amp instrumentation amplifier** — gain ×10 set by single resistor. Verify by hand calc.
2. **CMRR measurement** — drive both inputs with the same 1 kHz signal (common-mode); then with opposite-polarity signals (differential). Compute CMRR.
3. **Sallen-Key LPF** at f_c ≈ 1 kHz, Q = 0.707 (Butterworth). Test by driving with sines at f_c/10, f_c, 10·f_c — measure output amplitude at each. Verify the ratio drops by ~100× per decade above f_c (i.e. 2nd-order roll-off) using numbers, not log plots.

## Deliverable
Instrumentation amplifier with measured CMRR ≥ 60 dB at 1 kHz. Table of common-mode and differential gains.
