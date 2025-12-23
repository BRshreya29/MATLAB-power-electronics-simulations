# Study & Analysis of Lead-Acid Battery Charging for Electric Vehicles  
This project focuses on analysing the charging characteristics of a lead-acid battery using an IGBT-based bidirectional DC-DC converter. The study includes MATLAB/Simulink simulations, hardware measurements, efficiency calculation, and evaluation under different duty cycles.

---

##  Objectives
1. To study and analyse the charging characteristics of a lead-acid battery using an IGBT-based bidirectional DC-DC converter in real time.  
2. To determine the charging efficiency of the converter.  
3. To repeat the experiment for different duty cycles and input voltage variations.  

---

##  Apparatus Required
- MATLAB / Simulink  
- Real-time microcontroller  
- IGBT-based bidirectional DC-DC converter  
- Lead-acid battery  
- DC power supply / AC supply  
- Digital Storage Oscilloscope (DSO)  
- Voltage and current probes  

---

##  Theory (Summary)
An electric vehicle battery charger typically operates by receiving either **single-phase or three-phase AC supply** and converting it into a constant DC voltage.

The system consists of:
1. **AC–DC Converter:**  
   A diode bridge rectifier that converts AC input into constant DC.

2. **Bidirectional DC–DC Converter:**  
   A buck/boost converter that can:  
   - **Charge the battery (buck mode)** – S1 ON, S2 OFF, diode acts as freewheeling path  
   - **Discharge or boost mode (boost)** – S1 OFF, S2 ON  

Bidirectional operation is essential in EVs for charging as well as regenerative braking.

The output filter and converter parameters are computed using standard inductor–capacitor design equations.

---

##  Circuit & Block Diagrams
All diagrams used in this experiment are available in:

```
/circuit_diagrams/
```

- **block_diagram.png** – Hardware setup configuration  
- **lead_acid_battery_charging_circuit_diagram.png** – EV battery charger circuit  

---

##  Observation Table — Converter Efficiency

| Duty Cycle | Vs (V) | Is (A)   | Vb (V) | Ib (A)  | η (%)   |
|-----------|--------|----------|--------|---------|---------|
| 40%       | 30V    | 106.44A  | 6V     | 24.6A   | 4.52%   |
| 50%       | 30V    | 108.86A  | 6.3V   | 38.84A  | 7.38%   |

---

##  Battery Charging Characteristics

### **Duty Cycle = 40%**

| Time       | Vb (V) | Ib (mA)  |
|------------|--------|-----------|
| 0 sec      | 3.4    | 34.66     |
| 3.5 sec    | 4.5    | 34.66     |
| 47.86 sec  | 4.7    | 28.35     |
| 1:36.64 min| 5.6    | 26.415    |
| 3:45.92 min| 6.0    | 24.6      |

### **Duty Cycle = 50%**

| Time       | Vb (V) | Ib (mA) |
|------------|--------|----------|
| 0 sec      | 2.8    | 58.810   |
| 37.03 sec  | 6.0    | 46.724   |
| 1:19.66 min| 6.2    | 54.010   |
| 1:48 min   | 6.2    | 46.724   |
| 2:38 min   | 6.3    | 38.845   |

---

##  Calculations

Given switching frequency:  
**fₛ = 2 kHz**

## Inductor (L) Calculation

### **For 40% Duty Cycle**
\[
L = \frac{D(V_s - V_b)}{\Delta I \cdot f_s}
\]
\[
L = \frac{40/100 \times (30 - 6)}{0.2 \times 2000} = 120 \times 10^{-3} \, H
\]

### **For 50% Duty Cycle**
\[
L = \frac{50/100 \times (30 - 6.3)}{0.2 \times 0.038 \times 2000}
= 779 \times 10^{-3} \, H
\]

---

## Capacitance (C) Calculation
\[
C = \frac{\Delta I}{8 f_s \Delta V_b}
\]

Example:
\[
C = 3.76 \, F
\]

---

## Efficiency (η) Calculation
\[
\eta = \frac{V_b I_b}{V_s I_s} \times 100
\]

- **For 40% duty cycle → 4.52%**  
- **For 50% duty cycle → 7.38%**

---

##  Results
- The charging characteristics of the lead-acid battery were successfully recorded.  
- Bidirectional DC-DC converter operated correctly in buck and boost modes.  
- The converter efficiency increased with duty cycle.  
- Battery voltage and charging current increased proportionally over time.

---

##  Folder Contents
```
03_Lead_Acid_Battery_Charging/
│
├── circuit_diagrams/
│   ├── block_diagram.png
│   └── lead_acid_battery_charging_circuit_diagram.png
│
├── MATLAB_Simulation_files
└── README.md
```

---

## 📎 Note  
This experiment provides both simulation and hardware insight into EV battery charging systems.
