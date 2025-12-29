# Post-Simulation Results – CMOS Ring Oscillator

## 📌 Overview
This file presents the post-layout simulation results of the CMOS ring oscillator or inverter chain design. The simulation validates the circuit performance after layout parasitics and interconnect effects, ensuring that the design meets functional, timing, and power requirements.

## 📌 Simulation Summary

The circuit achieves an oscillation frequency of approximately 99 MHz, close to the target frequency of 100 MHz.

The power consumption is measured at ~13 µW, demonstrating the design’s low-power operation.

Output waveforms show stable oscillation with full voltage swing, confirming functional correctness.<br>

<br><img width="1755" height="835" alt="Screenshot from 2025-10-27 09-13-36" src="https://github.com/user-attachments/assets/49032870-ccea-4c30-8eb3-916cea162093" />

## 📌 Key Observations

The 1 MHz deviation from the target is within acceptable tolerance, primarily due to parasitic capacitances and layout effects.

Frequency stability confirms robustness under nominal operating conditions.

The signal exhibits low jitter and clean transitions, suitable for timing-critical VLSI applications.<br>

<br><img width="208" height="37" alt="Screenshot from 2025-12-29 19-13-57" src="https://github.com/user-attachments/assets/7a2f2c58-facb-476c-87fc-90f0eca5cc0d" />


## 📌 Applications & Implications

On-chip clock generation for digital systems

Timing analysis and PVT monitoring

Ring oscillator use in adaptive voltage and frequency scaling (DVFS) and delay monitoring

Energy-efficient VLSI designs due to low power consumption

## 📌 Conclusion
The post-simulation demonstrates that the CMOS design achieves ~99 MHz output at 13 µW, closely matching the 100 MHz target. This confirms that the design and layout are ready for integration into higher-level VLSI systems and further testing.


