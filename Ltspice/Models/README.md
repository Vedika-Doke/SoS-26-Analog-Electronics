# SPICE model files

Drop-in `.txt`/`.lib` models for parts not in the default LTspice library.

## Available
- **Op-amps:** `lm324.txt`, `ua741.txt`
- **BJT:** `bc547.txt`, `ca3046_ca3086.txt`
- **MOSFET:** `ALD110X.txt`, `cd4007.txt`, `tsmc_spice_180nm.txt`
- **Diodes:** `Diodes/Diode_1N914.txt`, `Diodes/Zener_1N4688.txt`
- **LEDs:** `LEDs/{red,green,blue,yellow,white}_5mm.txt`
- **Other:** `Solar_Cell.txt`

## How to use

1. Place a generic symbol (e.g. `npn`, `opamp2`) on the schematic.
2. Right-click → set `Value` to the model name (e.g. `BC547B`).
3. Add a SPICE directive (`.op` icon → SPICE directive):
   ```
   .include /path/to/Ltspice/Models/bc547.txt
   ```
4. Run sim. If model not found, check the model name inside the `.txt` matches what you typed.

Tip: drop the whole folder into LTspice's `lib/sub/` (Mac) or `lib\sub\` (Windows) to skip `.include` directives.
