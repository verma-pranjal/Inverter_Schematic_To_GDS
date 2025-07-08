# Inverter_Schematic_To_GDS
**Inverter_Schematic_To_GDS (45nm)**
This project demonstrates the complete Schematic-to-GDSII flow for a CMOS inverter using Cadence Virtuoso with the GPDK045 (45nm technology) library. It covers schematic design, simulation, layout, verification (DRC, LVS), parasitic extraction, and GDS generation.

**🎯 Objective**
To design and implement a CMOS inverter in 45nm technology, verify its layout against design rules and schematic, and generate a GDSII file suitable for fabrication.

**Tools & Technology used - **

| Tool/Platform     | Purpose                               |
| ----------------- | ------------------------------------- |
| Cadence Virtuoso  | Schematic, Layout, GDS Export         |
| Spectre (ADE)     | Functional and post-layout simulation |
| Assura            | DRC, LVS, RCX (Parasitic Extraction)  |
| GPDK045           | 45nm Technology Design Kit            |

**Project Structure
**
Inverter_Schematic_To_GDS/
├── schematic/               # Schematic and symbol views
├── layout/                  # Layout view of the inverter
├── simulation/              # Functional and post-layout simulations
├── verification/            # DRC and LVS reports
├── extracted/               # Extracted view with parasitics
├── gds/                     # Final GDSII file
└── README.md                # Documentation


🔧 Design Flow
1. Schematic Design
NMOS and PMOS connected in pull-down and pull-up configuration respectively.

Create symbol view for top-level usage and simulation.

2. Functional Simulation (Pre-layout)
Transient simulation using Spectre.

Verify logic functionality, propagation delay, rise/fall times.

3. Layout Design
Draw layout using GPDK045 rules.

Use appropriate layer assignments and transistor PCell generation.

4. DRC (Design Rule Check)
Run DRC via Assura .

Ensure there are 0 violations.

5. LVS (Layout vs Schematic)
Confirm the layout matches the schematic.

Pass LVS with net and device match.

6. Parasitic Extraction (RCX)
Use Assura RCX to extract parasitics.

Generate extracted view for post-layout simulation.

7. Post-Layout Simulation
Run transient simulation using the extracted view.

Measure impact of parasitics on delay and performance.

8. GDSII Generation
Export layout to GDSII using Cadence Virtuoso.

Ensure correct layer mapping file is used (e.g., gpdk045.tf, gpdk045.map).

**✅ Verification Summary**

| Step                  | Tool Used  | Status     |
| --------------------- | ---------- | ---------- |
| Functional Simulation | Spectre    | ✅ Passed   |
| DRC Check             | Assura     | ✅ Passed   |
| LVS Check             | Assura     | ✅ Matched  |
| RC Extraction         | Assura RCX | ✅ Complete |
| Post-Layout Sim       | Spectre    | ✅ Verified |
| GDSII Export          | Virtuoso   | ✅ Done     |




