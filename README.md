# OLA-openlab: Accessible Infrastructure for Molecular Biology

## Project Context and Background

This repository documents the practical output of a Master's Thesis project in Industrial Design at the Academy of Fine Arts in Warsaw (Faculty of Design), supervised by dr hab. Agata Szydłowska.

The project, titled "Democratization of Science – Accessible Laboratory Equipment," addresses the systemic barriers in accessing fundamental scientific infrastructure. In low-resource academic settings, field research, and educational environments, high-end scientific tools remain largely inaccessible due to prohibitive commercial pricing, closed proprietary hardware models, and supply chain constraints.

To tackle this disparity, the OLA-openlab ecosystem provides an open-hardware alternative for molecular biology workflows. Grounded in the principles of Open Design, RepRap digital fabrication, and off-the-shelf component integration, this suite aims to bridge the gap between raw DIY functional hacks and professional laboratory tools that inspire user trust and offer sound ergonomic operation.

## System Overview

The ecosystem comprises three open-source instruments designed for basic biological sample processing and molecular diagnostics:

* **Precision Mechanical Micropipette:** A fully 3D-printed liquid handling system featuring an integrated compliant spring printed in PETG. It uses low-cost, universally available glass or plastic Pasteur pipettes as fluid conduits to achieve repeatable, pre-calibrated liquid dosing without requiring metallic coil springs.
* **High-Speed Microcentrifuge:** A benchtop centrifugal separation unit built around a high-torque RS-550 DC motor and HW-201 PWM controller. It utilizes a closed 45-degree angle rotor geometry designed to support standard 1.5 mL / 2.0 mL microcentrifuge tubes under high radial acceleration.
* **ESP32 PCR Thermal Cycler:** An automated nucleic acid amplification system powered by an ESP32 microcontroller, a TEC1-12715 Peltier module, and a BTS7960B H-bridge driver. The firmware incorporates an asynchronous web server for protocol management and a thermal mass compensation algorithm for target temperature dwell cycles.

## Subdirectory Structure

* `/micropipette/` – CAD source files (.step, .f3z), fabrication guidelines, and operating protocols for the mechanical pipette.
* `/centrifuge/` – Rotor designs, dynamic balancing parameters, and electrical schematics for the benchtop centrifuge.
* `/pcr_cycler/` – Thermal block designs, ESP32 control firmware, and circuit wiring diagrams for the thermal cycler.
* `/docs/` – Theoretical thesis documentation, empirical measurement records, and presentation materials.

## Directions for Future Development

The repository is structured as a baseline framework intended for continuous, community-driven iteration:

* **Empirical Validation and Standards:** Conducting systematic gravimetric testing (ISO 8655 compliance) for the micropipette and thermal mapping across the PCR aluminum block to publish standard deviation figures.
* **Material Resilience in Lab Environments:** Testing alternative chemical-resistant filaments (PETG, ASA, resin-coated surfaces) against prolonged exposure to harsh laboratory reagents, such as ethanol and sodium hypochlorite.
* **Hardware Expansion:** Development of integrated optical modules for real-time quantitative PCR (qPCR) detection and active safety lid locks for high-speed centrifugation.

## Licensing

* **Firmware:** Distributed under the [GNU General Public License v3.0 (GPLv3)](LICENSE).
* **Hardware Designs & 3D Models:** Licensed under [CERN Open Hardware Licence Strongly Reciprocal (CERN-OHL-S v2)](https://ohwr.org/cernohl).
* **Documentation & Written Materials:** Licensed under [Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/).
