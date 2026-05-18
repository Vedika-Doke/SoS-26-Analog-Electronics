# Week 6 — Op-amps III: Non-linear (Schmitt, comparators, oscillators) + ADC/DAC primer

Flip the script: **positive feedback**, **open-loop comparators**, and **regenerative switching**. These building blocks power the 555 timer and a huge chunk of analog signal-conditioning.

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
Relaxation oscillator with measured frequency within 10 % of design. Show: schematic, V_cap (triangle-ish ramp) and V_out (square) on the same plot, hand calc of period.

---

## Bonus topic: ADC & DAC fundamentals

Now that you've seen comparators and summing amplifiers, you can build (or at least understand) every common ADC and DAC topology. This is a *short* survey — enough to recognize them and pick the right one.

### DAC (Digital → Analog)
- **Weighted-resistor DAC** — a summing op-amp with binary-weighted input resistors (R, 2R, 4R, 8R…). Direct application of the Week-3 summing amp. Simple but doesn't scale: resistor spread blows up past ~8 bits.
- **R-2R ladder DAC** — only two resistor values, regardless of bit count. The industry workhorse.

### ADC (Analog → Digital)
- **Flash ADC** — `2^N − 1` comparators in parallel. Fastest possible. Costly past 8 bits.
- **Counter-type / ramp ADC** — counter drives a DAC; output compared to input; counter stops when DAC ≥ input. Simple, slow.
- **Successive-approximation (SAR) ADC** — binary search using a DAC + comparator. The most common embedded-MCU ADC.
- **Sigma-delta (Σ-Δ)** — oversampling + noise shaping. High resolution at low speed (audio).

### Key spec
**Resolution** = full-scale range / 2^N. E.g. 10 V FS, 10 bits → ~10 mV per LSB.

### LTspice mini-lab (optional)
Build a 4-bit weighted-resistor DAC: summing op-amp with R, 2R, 4R, 8R inputs driven by four DC sources (1/0 representing logic high/low). Sweep through all 16 codes (`.step param`) and verify the staircase output.

### HW for this section
- `resources/hw/mbp_2018_hw12.pdf` — covers DAC resolution, weighted-resistor DAC with tolerance analysis, flash vs counter ADC, **and** 555 timer internals (monostable + astable). Recommend Q1–Q11 here; Q12–Q14 in Week 7.
