# Final Year Project — GaN Power Electronics Hardware

KiCad PCB and schematic designs, an LTspice circuit, and an IGI60L1111B1M Simscape digital-twin model collected from the local FYP project.

## Files

Download and extract **FYP-project-files.zip**. The archive preserves the original directory structure:

- `hardware/FYP/`: KiCad project, schematic, PCB, and local footprint library.
- `hardware/fyp1/`: alternate KiCad project, schematic, and PCB.
- `hardware/fyp_pcb/`: additional project settings.
- `hardware/MyComponents.kicad_sym`: custom symbol library.
- `hardware/fyp_ltspice.asc`: LTspice circuit.
- `hardware/*.zip`: original hardware design archives.
- `digital-twin/IGI60L1111B1M_DigitalTwin/`: Simscape component, parameter script, and test model.

Open the KiCad project files in KiCad. Preserve the local `Library.pretty` directory and configure any missing symbol/footprint libraries. For the digital twin, inspect the `.ssc` component and parameter script before building with MATLAB/Simscape; exact compatible versions and a verified execution procedure are not yet documented.

These files are published as existing project artifacts. Electrical rule checks, PCB design rule checks, simulation execution, and hardware operation have not been validated for this upload. Multiple design variants are retained; none is designated a fabrication-ready release. Generated editor state, history snapshots, and duplicate backup files were excluded. No open-source license has been adopted.


## How the project works

The hardware files describe GaN power-switching circuit designs in schematic and PCB form. The associated Simscape component represents a high-side and low-side half bridge controlled by INH and INL logic inputs. Its electrical nodes connect the DC rail, switching midpoint, low-side reference, driver supply, and bootstrap supply.

The component equations include driver propagation delay, gate rise and fall dynamics, supply undervoltage checks, switch on/off resistance, output capacitance currents, reverse conduction, and bootstrap charging. These mechanisms let a simulation examine switching behavior before comparing it with a physical circuit. The parameter script records nominal device, timing, capacitance, and thermal values; the presence of thermal parameters does not mean the current component implements a validated thermal model.

A practical review sequence is to inspect the schematic and custom libraries, check PCB connectivity and layout constraints, configure the component and test model in MATLAB/Simscape, and compare simulated waveforms with appropriately measured hardware results. No such comparison or efficiency benchmark was performed as part of publishing this repository.
