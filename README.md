# Inverter_Schematic_To_GDS
****Inverter_Schematic_To_GDS (45nm)****

This project demonstrates the complete Schematic-to-GDSII flow for a CMOS inverter using Cadence Virtuoso with the GPDK045 (45nm technology) library. It covers schematic design, simulation, layout, verification (DRC, LVS), parasitic extraction, and GDS generation.

****Objective****

To design and implement a CMOS inverter in 45nm technology, verify its layout against design rules and schematic, and generate a GDSII file suitable for fabrication.

****Tools & Technology used****

| Tool/Platform     | Purpose                               |
| ----------------- | ------------------------------------- |
| Cadence Virtuoso  | Schematic, Layout, GDS Export         |
| Spectre (ADE)     | Functional and post-layout simulation |
| Assura            | DRC, LVS, RCX (Parasitic Extraction)  |
| GPDK045           | 45nm Technology Design Kit            |

****Design Flow****

_**1. Schematic Design**_
NMOS and PMOS connected in pull-down and pull-up configuration respectively.

**Create symbol view for top-level usage and simulation.**

_**2. Functional Simulation (Pre-layout)**_
Transient simulation using Spectre.

**Verify logic functionality, propagation delay, rise/fall times.**

_**3. Layout Design**_
Draw layout using GPDK045 rules.

**Use appropriate layer assignments and transistor PCell generation.**

_**4. DRC (Design Rule Check)**_
Run DRC via Assura .

**Ensure there are 0 violations**

_**5. LVS (Layout vs Schematic)**_
Confirm the layout matches the schematic.

**Pass LVS with net and device match.**

_**6. Parasitic Extraction (RCX)**_
Use Assura RCX to extract parasitics.

**Generate extracted view for post-layout simulation.**

_**7. Post-Layout Simulation**_
Run transient simulation using the extracted view.

**Measure impact of parasitics on delay and performance.**

_**8. GDSII Generation**_
Export layout to GDSII using Cadence Virtuoso.


**✅ Verification Summary**

| Step                  | Tool Used  | Status     |
| --------------------- | ---------- | ---------- |
| Functional Simulation | Spectre    | ✅ Passed   |
| DRC Check             | Assura     | ✅ Passed   |
| LVS Check             | Assura     | ✅ Matched  |
| RC Extraction         | Assura RCX | ✅ Complete |
| Post-Layout Sim       | Spectre    | ✅ Verified |
| GDSII Export          | Virtuoso   | ✅ Done     |




