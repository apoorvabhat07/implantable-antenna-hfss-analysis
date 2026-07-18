# implantable-antenna-hfss-analysis

## >> Detuning-Immune Implantable Patch Antenna for Subcutaneous Telemetry
This project presents the design, optimization, and tissue-interaction analysis of a compact microstrip patch antenna engineered to operate within the MedRadio band (~600 MHz). Using Ansys HFSS, the design was characterized inside a simulated, high-loss multilayer human tissue phantom (skin, fat, and muscle) to evaluate performance stability against individual anatomical variations.

## >> The Engineering Challenge
Designing antennas intended for implantation presents two major challenges:
1. Severe Tissue Attenuation: Electromagnetic energy is rapidly absorbed by high-permissivity biological layers (like muscle and skin), leading to low radiative efficiency.
2. Anatomical Detuning: Variations in a patient's subcutaneous fat thickness change the surrounding dielectric environment. This shifting boundary layer routinely shifts the resonant frequency of an implant away from its target operating band, causing total communication failure.

## >> The Objective:
To design a compact 14 mm x 14 mm radiator that maintains tight resonance stability (~600 MHz) and reliable impedance matching even when the surrounding fat boundary fluctuates dynamically from 5 mm to 15 mm.

## >> Design Architecture & Methodology
The antenna was modeled using the Finite Element Method (FEM) inside Ansys HFSS:
**Radiator:** Square microstrip patch (14 mm x 14 mm) fed via a discrete 50 Ohm lumped terminal.
**Superstrate Layer:** A 2 mm Teflon (PTFE) bioceramic layer sits directly over the radiating element to insulate the metal components and serve as a low-loss dielectric buffer against surrounding tissues.
**Tissue Environment:** A 60 mm x 60 mm stacked block consisting of Muscle (15 mm base), a parametrically swept Fat layer (5 mm to 15 mm in 2.5 mm increments), and a capping Skin layer (1.5 mm).

## >> Key Performance Findings

**Robust Resonant Stability**
Across all five simulated tissue thickness iterations, the antenna effectively resisted detuning. The resonant frequency held tight between 590.53 MHz and 601.00 MHz, exhibiting a maximum variation of only 10.47 MHz. This proves the Teflon superstrate successfully isolates the radiator's near-field from shifting biological boundaries.

**Excellent Impedance Matching**
*Return Loss (S11):* Maintained comfortably below -16.9 dB across all configurations, reaching a peak match of -19.12 dB at 15 mm thickness.
*VSWR:* Ranged tightly from 1.25 to 1.33, verifying exceptionally efficient power transfer into the feed network without risky internal reflections.
*Input Impedance:* The antenna achieved a purely resistive profile at resonance (Reactance = 0 Ohm) with the input resistance varying minimally between 60.96 Ohm and 64.49 Ohm.

**Radiation Profile & Path Loss Buffering**
As the fat thickness increases from 5 mm to 15 mm, the peak far-field realized gain steadily improves from -34.15 dB to -31.73 dB.

Because biological fat has lower electrical conductivity than wet muscle tissue, a thicker fat layer acts as a low-loss physical spacer. This spatial buffer moves the radiator further away from the deeply dissipative muscle core, lowering overall path attenuation while maintaining a perfectly symmetrical broadside radiation pattern loop centered directly at Theta ~ 92 degrees.

## >> Key Engineering Takeaway

The simulation dataset successfully demonstrates that incorporating a low-loss dielectric superstrate provides robust detuning immunity for implantable systems. The antenna delivers highly predictable electrical behavior under highly variable anatomical conditions, rendering it a viable architecture for next-generation wireless health monitoring devices.
