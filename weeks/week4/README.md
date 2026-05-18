# Week 4 — Op-amps II: Real-world limits

Ideal op-amps don't exist. This week is about understanding *when each non-ideality bites you*, so your designs in weeks 5–8 don't fall apart in simulation (or later, on the bench).

## Concepts
- Finite open-loop gain → gain error in closed-loop circuits.
- **Gain-Bandwidth Product (GBW)** → closed-loop bandwidth shrinks as you crank gain.
- **Input offset voltage** and **input bias current** → DC errors, integrator drift.
- **Output saturation** → can't swing rail-to-rail on most op-amps.

## Reading & slides
- **Sergio Franco** Ch. 5–6 (real op-amp limitations). [Drive folder](https://drive.google.com/drive/folders/17T1Mnk_SVdqIi2b4Fn-qmpbAn6tkMbvd?usp=drive_link)
- **Prof. M. B. Patil's EE204 slides:** `mc_opamp_4` → `mc_opamp_5`. [Drive mirror](https://drive.google.com/drive/folders/1jPG5-WahBaDfoCOUDKTlCq3mqKhl5vyN?usp=drive_link) · [Source](https://www.ee.iitb.ac.in/~sequel/course_material.html)

## LTspice lab
Use `UniversalOpAmp2` and edit its parameters (`Avol`, `GBW`, `Vos`) directly — no rewiring needed.
1. **GBW vs gain** — take a non-inverting amp; sweep gain (×1, ×10, ×100). At each gain, drive with a sine and find the frequency where output amplitude drops noticeably (~70% of low-freq value). Verify GBW ≈ gain × bandwidth is constant.
2. **Offset drift in an integrator** — take last week's integrator, set `Vos = 5mV`, run `.tran` for 1 second. Watch the output drift to the rail. Discuss fixes (chopper, auto-zero, AC coupling).
3. **Output saturation** — push the inverting amp's input until output clips at the supply rails. Confirm the amp can't swing fully rail-to-rail on a generic part.

## Deliverable
GBW table: at gains ×1, ×10, ×100, list the measured −3 dB frequency and verify the product is constant. Short explanation of why high gain ⇒ low bandwidth.

---

## 📌 Midterm submission (around end of Week 4 / start of Week 5)

There will likely be an SoS midterm submission window around here. Plan to consolidate Weeks 1–4 into a short report:

- 1 page summary per week (what was learned + the key plot)
- All LTspice schematics + simulation results
- Reflection: which topic clicked, which didn't, what's still fuzzy

Don't leave this for the last day — pull the weekly deliverables together as you go.
