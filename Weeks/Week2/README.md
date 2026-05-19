# Week 2 — Diodes + BJT/MOS (light touch)

The point of this week is *exposure*, not mastery. You need to recognize these devices in a schematic and know what they do — we'll lean on op-amps for the rest of the course.

## Concepts
- **Diodes:** PN junction, exponential I-V, constant-voltage-drop model, half/full-wave rectifier, Zener regulation, clipper, clamper.
- **BJT (overview):** NPN/PNP, three regions (cutoff / active / saturation), "transistor as a switch" and "transistor as an amplifier" — qualitative only.
- **MOSFET (overview):** NMOS/PMOS, threshold voltage, "voltage-controlled switch" intuition.

## Reading & slides
- **Sedra & Smith** Ch. 4 — diode models, rectifiers (skip deep small-signal r_d). [Drive folder](https://drive.google.com/drive/folders/1AWumX1rr4MDby0pJfxpg7-JE0xuE8mdn?usp=drive_link)
- **Sedra & Smith** Ch. 6 §6.1–6.2 — BJT operation, regions (skim only).
- **Prof. M. B. Patil's EE204 slides:** `mc_diodes_1`, `mc_diodes_2`, `mc_bjt_1`. [Drive mirror](https://drive.google.com/drive/folders/1jPG5-WahBaDfoCOUDKTlCq3mqKhl5vyN?usp=drive_link) · [Source](https://www.ee.iitb.ac.in/~sequel/course_material.html)

## LTspice lab
1. **Full-wave bridge rectifier** with smoothing cap → measure ripple vs C. Sweep with `.step param C 10u 1000u 10`.
2. **Zener shunt regulator** — V_out vs V_in (`.dc`); observe regulation knee.
3. **BJT as a switch** — NPN driving an LED, base resistor + 5 V input toggling on/off (`.tran` with PULSE source). Observe V_CE in saturation.

## Deliverable
Ripple-vs-C plot + a clipper of your own design that limits a ±5 V sine to ±2 V.
