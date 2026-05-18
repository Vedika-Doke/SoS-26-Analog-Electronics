# LTspice — shared resources

Place here:
- Reusable schematics (`.asc`)
- SPICE models (`.lib`, `.mod`) added from manufacturer sites
- Symbols (`.asy`) for parts not in the default library
- Cheat-sheet PDFs / notes

## Directives to know

| Directive | Use |
|-----------|-----|
| `.tran 0 10m 0 1u` | transient with max-step (avoids aliasing HF content) |
| `.ac dec <pts> <fstart> <fstop>` | log-sweep AC analysis |
| `.dc V1 0 10 0.05` | DC sweep; nest with `.step` for family of curves |
| `.op` | quick Q-point check |
| `.step param C 10u 1000u 10` | parameter sweep |
| `.meas AC gain MAX V(out)` | automated measurement |
| `.include` / `.lib` | pull in external SPICE models |

## `UniversalOpAmp2` parameters

`Avol`, `GBW`, `SR`, `Vos` — sweep these to study real op-amp non-idealities without changing the schematic.

## Tips

- Alt-click a wire to probe **current**; Alt-click a component to plot **power** (V·I).
- Save plot window settings as `.plt` to restore view on reopen.
- Default `.tran` max-step is too coarse for HF — always specify one.
