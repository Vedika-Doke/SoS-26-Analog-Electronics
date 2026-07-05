# Week 7 — Final project (design + first build)

Pick **one** of the three projects below. The first two are well-scoped; the third is a stretch challenge for the ambitious.

---

## Option A — Analog differential-equation solver

Build a circuit that physically solves an ODE. Voltage at each node = a variable in the equation; integrators do the integration; summers and inverters wire up the equation itself.

**Suggested ODE:** simple harmonic oscillator (mass-spring-damper) → d²x/dt² + 2ζω·dx/dt + ω²·x = 0. Output a damped sine on the scope.

**Building blocks (all from weeks 3–4):**
- 2× integrators (one per order of the ODE)
- 1× summer (wires up the equation)
- 1× inverter (sign correction)
- Initial conditions set by pre-charging integrator caps

**Resources:**
- Franco, *Design with Op-Amps and Analog ICs* — analog computation chapter. [Drive folder](https://drive.google.com/drive/folders/17T1Mnk_SVdqIi2b4Fn-qmpbAn6tkMbvd?usp=drive_link)
- Classic Philbrick Researches op-amp application notes (public domain — Google "Philbrick analog computer").
- Analog Lab (EE230) Course Project: [Drive folder](https://drive.google.com/drive/folders/1aSZTyTb9XHa9UuP4lbLYzMAh9Tl3c__E?usp=drive_link)

---

## Option B — 555 timer from scratch (*not* the IC)

Recreate the internals of the legendary NE555 using discrete op-amps: two comparators, an SR latch, a discharge transistor, and the 5 kΩ resistor divider. Configure in **astable** mode (square-wave oscillator) or **monostable** mode (one-shot pulse).

**Building blocks (all from weeks 3–5):**
- 2× comparators with 2/3·V_CC and 1/3·V_CC thresholds
- SR latch — either op-amp Schmitt latch or two NAND gates
- Discharge path (BJT or MOSFET switch from week 2)
- External R and C set the timing

**Resources:**
- TI LM555 datasheet — functional block diagram page is the canonical schematic. https://www.ti.com/lit/ds/symlink/lm555.pdf
- Franco — Schmitt trigger + relaxation oscillator sections. [Drive folder](https://drive.google.com/drive/folders/17T1Mnk_SVdqIi2b4Fn-qmpbAn6tkMbvd?usp=drive_link)
- EE204 slides `mc_opamp_6.pdf` — Prof. M. B. Patil. [Drive mirror](https://drive.google.com/drive/folders/1jPG5-WahBaDfoCOUDKTlCq3mqKhl5vyN?usp=drive_link) · [Source](https://www.ee.iitb.ac.in/~sequel/course_material.html)
- EE204 HW12 (`Resources/Hw/mbp_2018_hw12.pdf`) Q12–Q14 — drawn-out 555 monostable + astable schematics with comparator/SR-latch internals. Highly recommended.

---

## Option C — Lotka-Volterra solver *(stretch challenge)*

The predator-prey equations:

```
dx/dt = αx − βxy
dy/dt = δxy − γy
```

Same idea as Option A — voltages represent populations, integrators do the integration — but the **xy** terms are **non-linear**, so you need an **analog multiplier** (AD633 is the classic part; the model is in [`Ltspice/Models/`](../../Ltspice/Models/) or downloadable from Analog Devices).

If you get it right, the output shows the populations oscillating out of phase — the famous predator-prey limit cycle. Plot V_x vs V_y on an X-Y scope plot to see the closed orbit.

**Building blocks:**
- 2× integrators (one for each population)
- 2× analog multipliers (one for each `xy` term)
- Summers + inverters to assemble each equation
- Initial-condition caps

**Resources:**
- **Lotka-Volterra task brief / reference material** — [Drive folder](https://drive.google.com/drive/folders/1Eb89DbthMYpdsaxMRP_hKD4yDCrUxa3Q?usp=drive_link)
  *(courtesy of EESA's "opAmped" — Learner's Space, IIT Bombay, Summer 2025)*
- Analog Devices AD633 datasheet — usage examples. https://www.analog.com/media/en/technical-documentation/data-sheets/AD633.pdf
- Franco — analog computation chapter (same as Option A). [Drive folder](https://drive.google.com/drive/folders/17T1Mnk_SVdqIi2b4Fn-qmpbAn6tkMbvd?usp=drive_link)
- "Analog Computing" by Bernd Ulmann — best modern reference if you want to go deep (book, optional).

---

## Week 7 deliverable

- Choice locked in by Day 1.
- Block-diagram schematic on paper (or in LTspice as a draft).
- First half built and simulating (even if buggy).
- Hand calc of expected values (frequency, damping ratio, threshold voltages, oscillation period — whichever applies).
