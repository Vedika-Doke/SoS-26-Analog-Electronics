# SoS '26 — Analog Electronics

Structured 8-week curriculum I'm using to mentor a Summer of Science (SoS) student in analog electronics. Builds fundamentals — linear networks, diodes, BJTs, MOSFETs, op-amps, filters — through weekly readings (Sedra/Smith, Sergio Franco), problem sets, and LTspice simulation labs, culminating in a discrete + op-amp design project.

**Mentor:** Vedika Doke · **Institute:** IIT Bombay · **Duration:** 8 weeks

---

## Plan at a glance

| Week | Topic | Key deliverable |
|------|-------|-----------------|
| 0 | LTspice setup | Tool installed, simple sim run |
| 1 | Linear networks + LTspice fluency | RC Bode plot vs hand calc |
| 2 | Diodes, rectifiers, wave-shaping | Ripple-vs-C plot + custom clipper |
| 3 | BJT — DC bias, load lines | Q-point stability across β |
| 4 | BJT amplifiers (small-signal) | CE amp: A_v, BW, Z_in, Z_out measured |
| 5 | MOSFETs + frequency response | Annotated Bode plot of CE amp |
| 6 | Op-amps — ideal topologies | Instrumentation amp, CMRR ≥ 60 dB |
| 7 | Real op-amps + active filters | Sallen-Key filter design |
| 8 | Final project + presentation | Report + demo |

Full plan: [`SoS_Plan.html`](SoS_Plan.html) (open in browser).

## Repo layout

```
.
├── SoS_Plan.html        full 8-week plan (styled)
├── weeks/
│   ├── week0/           LTspice onboarding
│   ├── week1/ … week8/  notes, labs, deliverables per week
├── ltspice/             shared .asc files, models, cheat-sheet
└── resources/           external links and references
```

## Final project options

Picked in Week 4, built through weeks 5–8:

1. Audio preamp + Baxandall tone control
2. Function generator (sine / square / triangle)
3. Two-stage discrete amplifier with measured specs
4. Thermistor / strain-gauge front-end

## Notes

- Textbook PDFs (Sedra/Smith, Sergio Franco) and EE204 course material are kept locally but gitignored — copyrighted, not for redistribution.
- All LTspice simulations target LTspice XVII or later.
