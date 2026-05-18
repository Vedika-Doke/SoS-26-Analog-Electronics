# Week 6 — Active filters + instrumentation amp

Last "fundamentals" week before the project. Two more workhorse op-amp circuits you'll likely need.

## Concepts
- **Active filters** — why active beats passive (gain, no inductors, easy cascading).
- **Sallen-Key topology** — 2nd-order low-pass, high-pass, band-pass. Pick component values to set cutoff f_c and Q.
- **Instrumentation amplifier** — 3-op-amp topology with high CMRR. The standard front-end for sensor signals (Wheatstone bridges, thermocouples, biopotentials).
- **CMRR** intuition — why differential signals survive but common-mode noise gets rejected.

## Reading & slides
- **Sergio Franco** — filter chapter + instrumentation amplifier chapter. [Drive folder](https://drive.google.com/drive/folders/17T1Mnk_SVdqIi2b4Fn-qmpbAn6tkMbvd?usp=drive_link)
- HW (from EE204, bonus): `Output_stage.pdf`, `Current_mirror.pdf` for the curious

## LTspice lab
1. **Sallen-Key 2nd-order LPF** at f_c ≈ 1 kHz, Q = 0.707 (Butterworth). Test by driving with sines at f_c/10, f_c, 10·f_c — measure output amplitude at each. Verify −40 dB/decade roll-off by amplitude ratio (no log plots needed — just numbers).
2. **3-op-amp instrumentation amplifier** — gain ×10. Drive both inputs with the same 1 kHz signal (common-mode), then with opposite-polarity signals (differential). Compute CMRR = 20·log(A_diff / A_cm).

## Deliverable
Instrumentation amplifier with measured CMRR ≥ 60 dB at 1 kHz. Table of common-mode and differential gains.
