# Study of IGBT Characteristics

This folder contains MATLAB simulations and hardware lab results for the study of Insulated Gate Bipolar Transistor (IGBT) characteristics. The experiment focuses on understanding the switching behaviour, transient response, and operating principles of an IGBT.

---

## Objective
To determine the characteristics of a given IGBT and measure key switching parameters such as rise time and fall time.

---

## Apparatus Used
- IGBT  
- Resistors  
- Transformer  
- Diodes & Zener Diodes  
- Capacitors  
- TLP250 Gate Driver  
- DSO (Digital Storage Oscilloscope)  
- Function Generator  

---

## Theory
The IGBT combines the advantages of MOSFET and BJT:
- High input impedance like a MOSFET  
- Low on-state conduction losses like a BJT  
- Voltage-controlled device  
- No second-breakdown problem (unlike BJT)  
- Lower switching and conduction losses compared to power MOSFETs  
- Faster switching than BJTs  

IGBTs are widely used in medium-power motor drives, power supplies, relays, and AC/DC converters.  
In forward operation, the IGBT behaves similar to a logic-level BJT but is controlled using **gate-to-emitter voltage** instead of base current.

---

## Circuit Diagrams Included
- Simplified equivalent circuit of IGBT  
- IGBT transient characteristics test circuit  
- TLP250 isolation and gate-driving circuit  
- Full experimental test setup block diagram  

---

## 📊 Observations (Sample Table)

| Freq (kHz) | V<sub>G</sub> (V) | T<sub>r</sub> (µs) | T<sub>f</sub> (µs) | V<sub>CE</sub> (V) | I<sub>C</sub> (A) | V<sub>F</sub> (V) | I<sub>F</sub> (mA) |
|-----------|-------------------|---------------------|---------------------|---------------------|-------------------|-------------------|---------------------|
| 15        | 110               | 14.35               | 10                  | 1V                  | 1.082             | 111               | 100                 |

---

## 🧮 Calculations
- **Rise Time (Tr)**  
  \( T_r = T_2 - T_1 = 81.23 - 66.88 = 14.35 \ \mu s \)

- **Fall Time (Tf)**  
  \( T_f = T_2 - T_1 = 7 - (-3) = 10 \ \mu s \)

---

## ✅ Results
1. Characteristics of the given IGBT were obtained successfully.  
2. **Rise Time:** 14.35 µs  
3. **Fall Time:** 10 µs  

---

## ⚠️ Precautions
- Show the circuit diagram to the instructor before acquiring components.  
- Verify all wiring connections before powering the circuit.  
- Wear appropriate safety footwear in the laboratory.

---

## 📂 Files in This Folder
- `/Hardware_Images/` – Photos of hand-written observations & circuit diagrams  
- `/MATLAB_Simulation/` – Simulink files (if applicable)  
- `/Plots/` – Switching waveforms and extracted rise/fall points  

---

## 📎 Notes
This experiment supports the power electronics repository by providing practical insight into real-world switching behaviour of IGBTs, complementing MATLAB-based analysis.

