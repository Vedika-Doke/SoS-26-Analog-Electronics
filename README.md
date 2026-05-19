# SoS '26 — Analog Electronics

Structured 8-week curriculum I'm using to mentor a Summer of Science (SoS) student in analog electronics. Heavy focus on **op-amps** — ideal linear circuits, real-world limits, and non-linear applications (Schmitt triggers, comparators, oscillators) — culminating in a project where the mentee picks between an **analog differential-equation solver**, a **555 timer built from scratch**, or a **Lotka-Volterra solver** (stretch).

**Mentor:** Vedika Doke · **Institute:** IIT Bombay · **Duration:** 8 weeks

> 📋 **This repo is a guideline, not a rulebook.** You'll have to submit your own **Plan of Action (POA)** to the SoS coordinators — see [`POA.md`](POA.md) for the submission rules (midterm mid-June, endterm mid-July, references mandatory, mentor-reviewed before submission). You can follow this trajectory, mix and match, or chart your own — whatever helps *you* learn.

---

## Plan at a glance

| Week | Topic | Key deliverable |
|------|-------|-----------------|
| 0 | LTspice setup | Tool installed, simple sim run |
| 1 | Linear networks + LTspice fluency | RC step response, τ measured |
| 2 | Diodes + BJT/MOS (light touch) | Bridge rectifier + custom clipper |
| 3 | Op-amps I — ideal linear | Integrator producing triangle wave |
| 4 | Op-amps II — real-world limits *(midterm window)* | Gain-bandwidth tradeoff measured at 3 gain settings |
| 5 | Instrumentation amplifier + active filters | Inst. amp with CMRR ≥ 60 dB |
| 6 | Op-amps III — non-linear (Schmitt, comparators, oscillators) + ADC/DAC primer | Relaxation oscillator at target frequency |
| 7 | Final project — design + first build | Choice locked, half built |
| 8 | Final project — polish + report + presentation | Report + demo |

## Final project options (pick in Week 7)

1. **Analog differential-equation solver** — integrators + summers + inverters wired to solve an ODE (e.g. mass-spring-damper → damped sine).
2. **555 timer from scratch** — recreate the NE555 internals (two comparators + SR latch + discharge switch) in astable or monostable mode.
3. **Lotka-Volterra solver** *(stretch)* — predator-prey ODEs with `xy` non-linearities; needs an analog multiplier (AD633). Shows the famous closed-orbit limit cycle on an X-Y plot.

## Cadence
- **At least one short meet per week.** Please show up — as the mentor I have to submit an involvement / interactions log to the SoS coordinators, and consistent participation makes that smooth for both of us.
- Content released week by week (current week's folder is the active one).
- **Start: Sun 24 May 2026.**
- **Midterm submission: 21 June 2026** (+4 weeks).
- **Endterm submission: 19 July 2026** (+8 weeks).
- **Buffer week — week of June 12–19** — no new content. Catch up, redo any deliverable, finish the midterm submission, or explore an optional topic.

## Repo layout

```
.
├── POA.md               Plan-of-Action submission rules
├── Weeks/
│   ├── Week0/           LTspice onboarding
│   ├── Week1/ … Week8/  notes, labs, deliverables per week
├── Ltspice/             shared .asc files, SPICE models
└── Resources/           external links, references, EE204 homeworks
```

## Resource credits
- **Sedra & Smith**, *Microelectronic Circuits* — [Drive folder](https://drive.google.com/drive/folders/1AWumX1rr4MDby0pJfxpg7-JE0xuE8mdn?usp=drive_link)
- **Sergio Franco**, *Design with Op-Amps and Analog ICs* — [Drive folder](https://drive.google.com/drive/folders/17T1Mnk_SVdqIi2b4Fn-qmpbAn6tkMbvd?usp=drive_link)
- **Prof. M. B. Patil, EE204 slides (IIT Bombay)** — [course page](https://www.ee.iitb.ac.in/~sequel/course_material.html) · [Drive mirror](https://drive.google.com/drive/folders/1jPG5-WahBaDfoCOUDKTlCq3mqKhl5vyN?usp=drive_link)
- **Lotka-Volterra project brief** — courtesy of EESA's *opAmped*, Learner's Space, IIT Bombay (Summer 2025). [Drive folder](https://drive.google.com/drive/folders/1Eb89DbthMYpdsaxMRP_hKD4yDCrUxa3Q?usp=drive_link)
- LTspice install + tutorial videos — Drive links inside [`Weeks/Week0/`](Weeks/Week0/)
