CMOS NOT Gate (Inverter) – Schematic Description
📌 Overview

This file contains the schematic design of a basic CMOS NOT gate (inverter) implemented using one PMOS and one NMOS transistor. The inverter is a fundamental digital building block used extensively in VLSI systems for logic inversion, buffering, and timing control.

📌 Design Description

The CMOS inverter consists of a PMOS transistor connected to the supply voltage (VDD) and an NMOS transistor connected to ground (GND). Both transistor gates are driven by a common input signal, while their drains are connected together to form the output node. This complementary configuration ensures full logic-level swing and low static power consumption.

📌 Pin Configuration

📌 VDD – Positive supply voltage for the PMOS transistor
📌 GND – Ground reference for the NMOS transistor
📌 IN – Input logic signal applied to both PMOS and NMOS gates
📌 OUT – Inverted output logic signal

📌 Functional Operation

When the input is logic low, the PMOS transistor turns ON and the NMOS turns OFF, pulling the output to logic high. When the input is logic high, the NMOS turns ON and the PMOS turns OFF, pulling the output to logic low. This complementary switching behavior provides fast transition times and near-zero static power dissipation.

📌 Applications

The CMOS NOT gate is used in logic inversion, signal buffering, delay elements, and as the basic stage in ring oscillators and digital timing circuits.

📌 Conclusion

This schematic demonstrates a standard CMOS inverter with correct functional behavior and power-efficient operation. It serves as a foundational block for more complex digital and mixed-signal VLSI designs.
<img width="1920" height="1080" alt="Screenshot from 2025-12-29 15-10-05" src="https://github.com/user-attachments/assets/a4c6a058-f3d9-4469-80f5-4f90479e6c19" />
