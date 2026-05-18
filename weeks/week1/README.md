# Week 1 — Linear networks + LTspice fluency

**Concepts:** KVL/KCL, Thevenin/Norton, superposition, RC transient response (charging / discharging, time constant), capacitor and inductor I-V relationships.

Everything later — op-amp integrator behaviour, Schmitt switching, 555 timing — reduces to these. Don't skip.

## Reading & slides
- **Sedra & Smith**, *Microelectronic Circuits*, Ch. 1 (signals + amplifier model — gain, Z_in, Z_out). [Drive folder](https://drive.google.com/drive/folders/1AWumX1rr4MDby0pJfxpg7-JE0xuE8mdn?usp=drive_link)
- **Prof. M. B. Patil's EE204 slides:** `mc_thev_1`, `mc_superposition_1`, `mc_rc_1`. [Drive mirror](https://drive.google.com/drive/folders/1jPG5-WahBaDfoCOUDKTlCq3mqKhl5vyN?usp=drive_link) · [Original course page](https://www.ee.iitb.ac.in/~sequel/course_material.html)
- HW (from EE204): `1_basic.pdf` (+ `1_sol.pdf`)

## LTspice lab
1. **RC charging** — DC source + switch + R + C. `.tran` simulation; measure time constant τ = RC by reading the 63% point off the waveform.
2. **RC discharging** — pre-charged cap discharging through R; verify same τ.
3. **Thevenin equivalent** — build a 3-resistor + source network; find V_th and R_th by simulation (open-circuit voltage, short-circuit current).

## Deliverable
Step-response plot of RC charging with τ marked at 63%, hand calc matching the sim within 5%. One paragraph: "what surprised me / what broke."
