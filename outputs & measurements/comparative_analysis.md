# CMOS Ring Oscillator Project
## 📌 Overview

This repository contains the design, simulation, and layout of a CMOS ring oscillator and inverter chain. The project demonstrates low-power, high-frequency design using PMOS and NMOS transistors, including:

Single CMOS inverters (NOT gates)

Integrated 243-stage inverter chain

Ring oscillator operation for timing and frequency analysis

Pre- and post-layout simulation studies

The design is targeted for VLSI timing characterization, on-chip clock generation, and energy-efficient digital applications.

## 📌 Schematic & Symbol

CMOS NOT gate: Basic inverter using 1 PMOS and 1 NMOS transistor

Integrated 243-stage inverter chain: Cascaded inverters forming a delay line / ring oscillator

Symbol view: Abstracted representation exposing essential pins for hierarchical integration

## Pin Configuration:
1. VDD – Positive supply voltage
2. GND – Ground reference
3. IN – Logic input
4. OUT – Logic output

## 📌 Layout (Cadence Virtuoso)

Layout follows standard CMOS design rules (DRC/LVS compliant)

Includes metal routing, vias, and well taps for reliable operation

Optimized for minimal area and low parasitic capacitance

Supports both open-chain delay measurement and ring oscillator operation

## 📌 Pre-Simulation Results

Frequency: 83 MHz<br>

<br><img width="1920" height="1080" alt="Screenshot from 2025-12-29 15-03-08" src="https://github.com/user-attachments/assets/670a179b-fe0b-449d-b925-bed9efce0699" />


Power Consumption: 15 µW

<img width="208" height="37" alt="Screenshot from 2025-12-29 19-13-57" src="https://github.com/user-attachments/assets/45ff2b8a-c479-4826-a6f0-c0223e7c19bc" />


Functional correctness confirmed with full logic swing

Serves as a baseline for layout and timing expectations

## 📌 Post-Simulation Results

Frequency: ~99 MHz (Target: 100 MHz)<br>

<br><img width="1755" height="835" alt="Screenshot from 2025-10-27 09-13-36" src="https://github.com/user-attachments/assets/1c8498a5-c842-4fbe-864f-19e8ebebab6f" />


Power Consumption: ~13 µW<br>

<br><img width="212" height="41" alt="Screenshot from 2025-12-29 19-06-05" src="https://github.com/user-attachments/assets/0edfcac8-2399-40e7-b4b7-f205860d34a1" />


Layout parasitics considered; waveform stability and low jitter verified

Confirms readiness for integration and further testing

## 📌 Conclusion

This project demonstrates a complete CMOS ring oscillator design workflow:

Schematic-level design (single inverters & 243-stage chain)

Symbol abstraction for hierarchical integration

Cadence Virtuoso layout with DRC/LVS compliance

Pre- and post-layout simulations showing frequency and power optimization

Comparative analysis confirming design readiness for high-speed, low-power VLSI applications
