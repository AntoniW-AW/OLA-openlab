# High-Speed Benchtop Microcentrifuge

## Project Description

The OLA High-Speed Microcentrifuge is an open-hardware centrifugal separation platform engineered for basic biological sample processing, such as cell pelleting, reagent spin-down, and nucleic acid extraction. 

Commercial microcentrifuges represent a substantial capital expenditure for resource-constrained laboratories, with market prices ranging from $2,200 to $11,000 USD. This module provides a low-cost alternative using readily available industrial electronics and 3D-printed mechanical components.

Development focused on rotor integrity, tube containment, and structural containment:

* **Rotor Geometry and Safety:** Early open-slot rotor designs posed severe risks of tube displacement under high centrifugal acceleration. The finalized design features a closed 45-degree fixed-angle rotor geometry that fully supports the walls of standard 1.5 mL and 2.0 mL microcentrifuge tubes (Eppendorf style), constraining radial displacement and preventing mechanical shear.
* **Structural Frame:** The chassis houses the drive motor, bearing assemblies, and speed control module within a compact desktop form factor.

## System Components

The hardware setup utilizes off-the-shelf industrial components:

* **Drive Motor:** RS-550 High-Torque DC Motor (12V–21V operating range).
* **Speed Controller:** HW-201 DC Motor PWM Speed Regulator for manual speed control.
* **Radial Bearings:** Sealed ball bearings to support the motor driveshaft and maintain rotational alignment.
* **Power Supply:** External 12V DC power adapter or battery pack.
* **Chassis and Rotor:** FDM 3D-printed protective enclosure, lid, and fixed-angle rotor.

## Application and Operating Protocol

The unit is designed for rapid phase separation and sample consolidation in molecular workflows:

1. **Balanced Loading:** Samples must be loaded in opposing slots with equal mass (balanced to $\pm 0.01\text{ g}$) to minimize rotational kinetic imbalance.
2. **Speed Regulation:** Power is applied via the HW-201 PWM dial, gradually increasing rotational velocity to avoid sudden mechanical strain on the drive shaft.
3. **Spin-Down Cycle:** The rotor maintains high-speed rotation for the prescribed protocol duration, after which power is cut and the rotor coasts to a complete stop before opening the lid.

## Fabrication Guidelines

* **Structural Body:** Printable on standard FDM printers ($220 \times 220 \times 250\text{ mm}$ minimum build volume).
* **Material Selection:** PETG or ABS is required for the rotor and structural housing due to dynamic tensile strength requirements under high rotational loads. PLA is not recommended due to brittle failure risks.
* **Rotor Print Settings:** The rotor must be printed with 100% solid infill (concentric pattern) and at least 6 wall perimeters to eliminate internal air voids that cause dynamic weight imbalance.

## Directions for Future Development

* **Dampening and Vibration Isolation System:** The current dampening element requires significant further refinement. High vibrational noise and dynamic instability at maximum rotational speeds remain a primary mechanical challenge. Future work must focus on developing improved elastomeric mounts, spring-suspended motor cradles, or tuned vibration dampeners.
* **Rotational Speed Telemetry:** Integration of an optical or Hall-effect tachometer sensor connected to a microcontroller for real-time display of RPM and Relative Centrifugal Force ($RCF / g\text{-force}$).
* **Lid Interlock Mechanism:** Implementation of a physical solenoid or servo-driven safety lock to prevent the enclosure from being opened while the motor is spinning.
