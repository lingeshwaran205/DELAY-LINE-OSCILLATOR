# DELAY-LINE-OSCILLATOR

Application-oriented **CMOS ring oscillator** designed for on-chip clock generation and precise delay characterization.  
The oscillator is used as a fundamental timing element to study inverter delay, oscillation behavior, and sensitivity to environmental and process variations in VLSI systems.  
Validated through circuit-level simulations for accurate frequency and delay analysis.<br>

</br>

## 100 MHz CMOS Ring Oscillator for Delay Characterization

<img width="860" height="709" alt="Screenshot from 2025-10-25 15-14-24" src="https://github.com/user-attachments/assets/de873b73-7cac-4330-88a9-0d74948b4d24" />  <br>

</br> 

<img width="860" height="709" alt="Screenshot from 2025-10-25 15-15-52" src="https://github.com/user-attachments/assets/c6b64d28-d33a-471b-95c0-b07ca51e795c" />



---

## 📌 Overview
This project focuses on the **design, analysis, and validation of a 100 MHz CMOS ring oscillator** implemented using cascaded inverter stages.

The oscillator serves as a **self-contained timing element** whose frequency directly reflects:
- Inverter propagation delay
- Supply voltage variations
- Temperature changes
- Manufacturing process spread

Due to its fully digital nature, the ring oscillator is well suited for **on-chip timing analysis, monitoring, and characterization** in modern CMOS technologies.

---

## 🧩 Problem Statement (Broader Context)
As semiconductor technologies scale, **timing uncertainty** has become a fundamental challenge across a wide range of digital systems.

Key contributors include:
- Variability in manufacturing processes
- Fluctuations in supply voltage
- Temperature gradients across the chip
- Device aging and long-term degradation

These effects alter **gate propagation delay**, making it difficult to accurately predict timing behavior under real operating conditions.  
Conventional timing analysis relies heavily on **static worst-case assumptions**, which do not capture real-time or local delay variations.

### ❗ Core Challenge
Develop a **simple, fully digital timing element** that can accurately reflect **delay variations** caused by physical and environmental factors, without relying on complex analog circuitry or external components.

---

## 🛠️ Oscillator Design Approach
A **100 MHz CMOS ring oscillator** is implemented using an odd number of cascaded inverter stages connected in a feedback loop.

The oscillation frequency is determined by the **total propagation delay** of the inverter chain, making the oscillator a direct representation of intrinsic CMOS delay characteristics.

### Fundamental Relation
<img width="886" height="379" alt="image" src="https://github.com/user-attachments/assets/aa63990b-ff3b-4c24-9cf6-6fce995cf425" />

Where:
- `n` = number of inverter stages  
- `T` = propagation delay of a single inverter  

Any increase in inverter delay results in a proportional reduction in oscillation frequency.

---

## 🎯 Why a 100 MHz Ring Oscillator?
| Aspect | Reason |
|-----|------|
| Moderate high frequency | Suitable for delay-sensitive analysis |
| Digital-only design | No analog biasing or tuning |
| Compact layout | Minimal area overhead |
| Technology-sensitive | Accurately reflects PVT variations |
| Easy integration | Compatible with standard CMOS flows |

---

## ⚠️ Design Considerations
Key challenges addressed in the oscillator design include:
- Frequency variation due to process corners
- Sensitivity to supply noise
- Output jitter caused by delay mismatch
- Load-dependent frequency shifts

Mitigation strategies involve:
- Careful inverter sizing
- Output buffering
- Consistent layout practices
- Controlled loading conditions

---

## 🧩 Cadence-Based EDA Design Flow

The design and validation of the **100 MHz CMOS ring oscillator** were carried out using a structured **end-to-end CMOS EDA workflow** in **Cadence Virtuoso**, following standard VLSI design practices from schematic entry to post-layout verification.

This flow ensures functional correctness, physical validity, and manufacturability of the oscillator design.

---

### 1️⃣ Pre-Design Specification
- Target oscillation frequency: **100 MHz**
- Selection of inverter-based ring oscillator topology
- An odd number of inverters creates a phase inversion around the loop.
- Propagation delay through the inverter chain introduces a finite loop delay.
- Continuous inversion and delay result in sustained oscillation.
- The output frequency stabilizes near **100 MHz** based on total delay.

---

### 2️⃣ Schematic Design

<img width="1920" height="1080" alt="Screenshot from 2025-12-29 15-10-05" src="https://github.com/user-attachments/assets/747bad09-d399-4bfa-ad42-a8f32061b61a" />

<img width="1920" height="1080" alt="Screenshot from 2025-12-29 15-10-29 (1)" src="https://github.com/user-attachments/assets/0440949f-a3f6-4484-ab4b-bd892ac8bdc1" />

<img width="1625" height="516" alt="1000038193" src="https://github.com/user-attachments/assets/8c28f956-c41f-475f-a264-e82b538c84ab" />



- Transistor-level CMOS inverter schematic creation in **Cadence Virtuoso**
- Cascading of inverter stages with feedback to enable oscillation
- Output buffering for signal integrity and measurement isolation
- Hierarchical organization for clarity and scalability

---

### 3️⃣ Pre-Layout Simulation and it's analysis <br>

<br><img width="1920" height="1080" alt="Screenshot from 2025-12-29 15-03-08" src="https://github.com/user-attachments/assets/d0882d72-a658-487f-9f44-5846f8e22483" /><br>

<br><img width="212" height="42" alt="Screenshot from 2025-12-30 15-39-27" src="https://github.com/user-attachments/assets/996fb99f-363a-485d-82fd-51c0f181fde9" /><br>

<br><img width="209" height="40" alt="Screenshot from 2025-12-30 13-39-12" src="https://github.com/user-attachments/assets/759d42f1-be57-4dc9-add6-ca971a3b37bc" /><br>


- Transient simulations to verify oscillation startup
- Frequency extraction under nominal conditions
- Functional validation of delay-to-frequency relationship
- Early identification of instability or non-oscillation issues

---

### 4️⃣ Layout Design<br>

<table>
  <tr>
    <td>
      <img width="320" height="320"
      src="https://github.com/user-attachments/assets/3565b4be-9066-43c4-9137-ab6c7936596c">
    </td>
    <td style="width:40px"></td>
    <td>
      <img width="320" height="400"
      src="https://github.com/user-attachments/assets/160ecbaa-a93a-471d-9ca7-459c46c26f0d">
    </td>
  </tr>
</table>


- Custom layout of inverter stages using CMOS design rules
- Consistent device orientation to reduce systematic mismatch
- Symmetric routing to maintain uniform delay
- Compact placement to minimize parasitic imbalance

---

### 5️⃣ Design Rule Check (DRC)
- Verification of layout compliance with foundry design rules
- Resolution of spacing, width, and enclosure violations
- Ensuring layout manufacturability

---

### 6️⃣ Layout Versus Schematic (LVS)
- Electrical equivalence check between schematic and layout
- Verification of transistor connectivity, sizing, and hierarchy
- Confirmation of correct oscillator topology implementation

---

### 7️⃣ Parasitic Extraction (PEX)
- Extraction of layout-induced parasitic resistances and capacitances
- Generation of post-layout netlist
- Analysis of parasitic impact on inverter delay

---

### 8️⃣ Post-Layout Simulation and it's analysis <br>

<br><img width="1755" height="835" alt="Screenshot from 2025-10-27 09-13-36" src="https://github.com/user-attachments/assets/02cff8f8-bc0a-4709-880e-bdb5de5f7496" /><br>

<br><img width="212" height="39" alt="Screenshot from 2025-12-30 14-07-43" src="https://github.com/user-attachments/assets/912f2b25-b7d5-44ee-a297-8644da0cf793" /><br>

<br><img width="214" height="39" alt="Screenshot from 2025-12-30 14-06-54" src="https://github.com/user-attachments/assets/3a7c9d60-1239-4351-be3f-d202b7d89e65" /><br>



- Verification of oscillation with extracted parasitics
- Comparison of pre-layout and post-layout oscillation frequency
- Validation of stable operation near **100 MHz**
- Delay sensitivity analysis under voltage and temperature variations

---

### 9️⃣ Design Closure
- Clean DRC and LVS reports
- Verified post-layout functionality
- Documented simulation and waveform results
- Design ready for integration or academic sign-off


---

## 🏁 Conclusion
This work demonstrates a **100 MHz CMOS ring oscillator** as a robust and compact timing element for **delay analysis and characterization**.  
By directly mapping inverter delay to oscillation frequency, the design provides valuable insight into timing behavior under real operating conditions using a purely digital approach.

---

## 📚 Keywords
CMOS Ring Oscillator, Delay Line Oscillator, Timing Characterization, Inverter Delay, PVT Variations, Digital VLSI

---

### 🔧 Design Environment
- **EDA Tool:** Cadence Virtuoso
- **Design Level:** Transistor-level (CMOS)
- **Circuit Type:** Delay-line based ring oscillator
- **Technology:** CMOS (GPDK180-based)

---

## 👤 Authors
[Naveen J](https://www.linkedin.com/in/naveenjeyakumar)

[Lingeshwaran S](https://www.linkedin.com/in/lingeshwaran205)

## Under the guidance:

[Dr.Elango S](https://www.linkedin.com/in/elango-sekar-8973b958)




---

## 📄 License

This project, including the **100 MHz CMOS ring oscillator design, simulations, and documentation**, is licensed under the **GNU General Public License v3.0 (GPL-3.0)**.

