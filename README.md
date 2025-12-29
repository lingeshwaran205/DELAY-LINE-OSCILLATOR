# DELAY-LINE-OSCILLATOR

Application-oriented **CMOS ring oscillator** designed for on-chip clock generation and precise delay characterization.  
The oscillator is used as a fundamental timing element to study inverter delay, oscillation behavior, and sensitivity to environmental and process variations in VLSI systems.  
Validated through circuit-level simulations for accurate frequency and delay analysis.<br>

</br>

## 100 MHz CMOS Ring Oscillator for Delay Characterization

<img width="689" height="643" alt="Screenshot from 2025-10-25 15-14-24" src="https://github.com/user-attachments/assets/de873b73-7cac-4330-88a9-0d74948b4d24" />  <br>

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

## 🧠 Architecture Overview

### Block Diagram
<img width="661" height="611" alt="image" src="https://github.com/user-attachments/assets/5fbfd758-1114-49b0-8770-acfd89eb89c0" />

#### Inside the R2 block, multiple cascaded CMOS inverters form the delay line whose cumulative delay produces oscillation at approximately 100 MHz.

<img width="1625" height="516" alt="1000038193" src="https://github.com/user-attachments/assets/8c28f956-c41f-475f-a264-e82b538c84ab" />

**Key Elements:**
- Cascaded CMOS inverter stages  
- Feedback connection to enforce oscillation  
- Output buffering for observation and measurement  

---

## 🔄 Operating Principle
1. An odd number of inverters creates a phase inversion around the loop.
2. Propagation delay through the inverter chain introduces a finite loop delay.
3. Continuous inversion and delay result in sustained oscillation.
4. The output frequency stabilizes near **100 MHz** based on total delay.

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

## 🧪 Simulation & Verification
### Output Waveform

<img width="1755" height="835" alt="Screenshot from 2025-10-27 09-13-36" src="https://github.com/user-attachments/assets/56fe3caf-953c-486f-bf4f-acfad9a46b75" />

### Power Analysis
<img width="212" height="41" alt="Screenshot from 2025-12-29 19-06-05" src="https://github.com/user-attachments/assets/b6abd4ce-1a59-47be-93e5-cb56c846527d" />



Verification includes:
- Transient simulation for oscillation startup
- Frequency measurement under nominal conditions
- PVT corner simulations
- Delay-to-frequency characterization

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
- **Technology:** CMOS (PDK-based)

---

## 👤 Author
**Naveen J**


---

## 📄 License
This project is intended for academic and educational use.
