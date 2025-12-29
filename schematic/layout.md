# CMOS Layout – Cadence Virtuoso

## 📌 Overview
This folder contains the layout design of CMOS circuits implemented in Cadence Virtuoso. The layout corresponds to the transistor-level schematic, including individual CMOS inverters and the integrated 243-stage inverter chain. The layout ensures proper connectivity, spacing, and adherence to design rules for fabrication while maintaining functional correctness.

## 📌 Design Features

The layout is created using PMOS and NMOS transistors as per the schematic design.

Proper metal routing, via connections, and well taps are included to ensure reliable operation.

Layer usage follows standard CMOS rules, ensuring DRC/LVS compliance.

The layout is optimized for minimal area while maintaining signal integrity and timing performance.

## 📌 Functional Behavior
The layout preserves the functionality of the underlying schematic. CMOS inverters operate with full logic swing, low static power, and fast switching. In the case of the 243-stage inverter chain, the layout supports both open-chain delay analysis and ring oscillator operation when feedback is applied.

## 📌 Applications

Hierarchical digital design and verification

Ring oscillator and delay chain implementation

Timing characterization under PVT variations

Educational and experimental VLSI layout studies

## 📌 Conclusion
This Cadence Virtuoso layout demonstrates a practical, fabrication-ready CMOS design. It enables designers to verify schematic-to-layout correspondence, analyze timing behavior, and use the integrated layout in higher-level designs or simulations.<br>

<br><img width="860" height="709" alt="Screenshot from 2025-10-25 15-15-52" src="https://github.com/user-attachments/assets/20767a69-a864-42de-aac9-cf6af6d6c525" /><br>


<br><img width="860" height="709" alt="Screenshot from 2025-10-25 15-14-24" src="https://github.com/user-attachments/assets/b56d104e-88ab-4b5a-9a25-4dacf199e113" />
