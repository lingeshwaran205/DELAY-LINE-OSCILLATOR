# Pre-Simulation Results – CMOS Inverter Design

## 📌 Overview
This file presents the pre-simulation analysis of the CMOS inverter (or inverter chain) design. The pre-simulation validates the circuit performance before full layout verification, providing insights into operating frequency, power consumption, and functional correctness.

## 📌 Simulation Summary

The CMOS circuit produces an oscillation frequency of 83 MHz, close to the target design range.

Power consumption is measured at approximately 15 µW, demonstrating the design’s low-power operation.

Pre-simulation confirms correct logical behavior, with full voltage swing at the output node.<br>

<br><img width="1920" height="1080" alt="Screenshot from 2025-12-29 15-03-08" src="https://github.com/user-attachments/assets/7508af6c-b9b8-4b0a-9605-54946bba47ae" />

## 📌 Key Observations

The 83 MHz frequency indicates that the propagation delay of individual inverter stages is well within expected limits.

Low power consumption ensures suitability for energy-efficient SoC and on-chip applications.

The design exhibits stable output transitions, confirming noise immunity and functional reliability at the pre-layout stage.<br>

<br><img width="208" height="37" alt="Screenshot from 2025-12-29 19-13-57" src="https://github.com/user-attachments/assets/d1e7f643-fe79-4f96-a528-6fc515d668b8" />


## 📌 Applications & Next Steps

The pre-simulated circuit can be used for timing analysis, ring oscillator studies, and delay chain characterization.

Provides a baseline for layout-aware simulations, including parasitic effects and PVT variations.

Supports further optimization for higher frequency or lower power if needed.

## 📌 Conclusion
The pre-simulation results validate the CMOS inverter design at 83 MHz and 15 µW, ensuring that the circuit meets functional and power requirements prior to full layout implementation. This step is crucial for robust, low-power, timing-aware VLSI design workflows.


