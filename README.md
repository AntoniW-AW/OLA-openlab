# Precision Mechanical Micropipette

## Project Description

The OLA Mechanical Micropipette is a fully 3D-printed liquid handling system designed as an accessible alternative to commercial single-channel pipettes. Commercial units maintain high price barriers due to specialized manufacturing and grant-funded procurement models. Open-source alternatives frequently lack the ergonomic stability or structural coherence required for professional environments. This project bridges that gap by integrating a standard plastic Pasteur pipette into a 3D-printed mechanical housing.

Development focused on functional reliability, material selection, and universal human factors:

* **Universal Ergonomics:** Initial iterations utilized hand-molded biometric grips. Testing showed that custom hand impressions restricted usability across different hand sizes. The final form adopts a neutral geometry with an ergonomic index finger hook, ensuring universal comfort and control across diverse user groups.
* **Compliant Mechanism and Material Selection:** To eliminate reliance on external metallic springs, the internal mechanism uses a 3D-printed compliant spring. PETG was selected over PLA due to its yield strength, elastic memory, and resistance to structural fatigue under repeated flexural stress. PETG also offers necessary chemical resistance to common laboratory reagents.

## Application and Operating Protocol

The instrument is engineered for repeatable, pre-calibrated liquid dosing. Operating sequence:

1. **Volume Adjustment:** Rotate the top adjustment screw to set the mechanical plunger travel limit, establishing the precise target volume for repetitive dispensing.
2. **Aspiration:** Depress the top button to displace air from the Pasteur pipette. Submerge the tip into the liquid and release the button, allowing the return force of the internal PETG spring to draw the preset volume.
3. **Dispensing:** Transfer the assembly to the receiving container and fully depress the button to expel the measured volume.

## Fabrication Guidelines

* **Fluid Conduit:** Standard disposable plastic Pasteur pipette.
* **Structural Body:** Printable on standard FDM printers ($220 \times 220 \times 250\text{ mm}$ minimum build volume).
* **Material Requirements:** PETG is required for structural parts and flexural spring elements. Additional wall perimeters should be applied to flexural regions to prevent delamination under continuous cycle strain.

## Directions for Future Development

* **Refinement of Side-Clamping Element:** The lateral clamping structure designed to secure the Pasteur pipette body is currently optional. Further geometric optimization is required to achieve optimal retention force without deforming the thin plastic pipette wall.
* **Adjustment Screw Locking Mechanism:** Implementation of a physical locking or detent mechanism to fix the position of the volume adjustment screw during extended, high-volume repetitive dispensing sessions.
