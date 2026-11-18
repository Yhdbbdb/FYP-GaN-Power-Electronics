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
