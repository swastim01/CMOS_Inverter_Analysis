# DC Analysis of CMOS Inverter

## Introduction
DC analysis of a CMOS inverter helps in understanding its **static characteristics**, such as:
- **Voltage Transfer Characteristics (VTC)**
- **Noise Margins**
- **Threshold Voltage (Vth)**
- **Power Consumption in Steady State**

This analysis is crucial for designing **robust digital circuits** with proper noise immunity and stable operation.

---

## **Voltage Transfer Characteristics (VTC)**
The **VTC curve** describes the relationship between the **input voltage (Vin)** and the **output voltage (Vout)**.

### Key Points:
1. **Logic Levels**: 
   - At **Vin = 0V**, the output is at **VDD** (logic HIGH).
   - At **Vin = VDD**, the output is at **0V** (logic LOW).
  
2. **Transition Region**:
   - The inverter **switches states** when **Vin ≈ Vth**.
   - The **gain (dVout/dVin) is maximum** at this point.

3. **Noise Margins**:
   - Defined as:
     \[
     NM_H = V_{OH} - V_{IH}, \quad NM_L = V_{IL} - V_{OL}
     \]
   - Ensure proper **signal integrity** by preventing unintended switching.

---

## **Factors Affecting VTC**
### 1️⃣ Transistor Sizing (W/L Ratio)
   - Affects the **switching threshold (Vth)**.
   - Increasing **W/L ratio of PMOS** shifts VTC **left**.
   - Increasing **W/L ratio of NMOS** shifts VTC **right**.

### 2️⃣ Supply Voltage (VDD)
   - Higher **VDD improves noise margins**.
   - Lower **VDD reduces power consumption but increases delay**.

### 3️⃣ Process Variations
   - Fabrication differences cause **threshold voltage variations**.
   - Impacts **switching characteristics**.

---

## **Power Dissipation in DC Analysis**
A CMOS inverter has three **power components**:

1. **Static Power Consumption**
   - Ideally **zero**, since one transistor is always OFF.
   - In reality, **leakage currents** cause minor static power dissipation.

2. **Short-Circuit Power**
   - Occurs when both **NMOS & PMOS** are **partially ON** during switching.
   - Reduced by **proper transistor sizing**.

3. **Dynamic Power (in AC analysis)**
   - Not a concern in pure DC analysis.
   - Dominates in transient operation.

---

## **Simulation Setup in LTSpice**
- **DC Sweep Analysis**: 
  - Sweep **Vin** from **0V to VDD**.
  - Plot **Vout vs. Vin** (VTC curve).
  
- **Noise Margin Extraction**:
  - Identify **VIL, VIH, VOL, VOH** from VTC.
  - Compute **NMH, NML**.

- **Power Measurement**:
  - Measure **I(VDD) × VDD** at different input voltages.

---

## **Simulation Results**
- The **VTC curve** confirms proper inverter operation.
- **Noise margins** indicate good **signal stability**.
- **Power dissipation** is minimal in steady states.

---

## **Conclusion**
- **CMOS inverters provide excellent noise immunity**.
- **Transistor sizing** affects switching characteristics.
- **DC power dissipation is low**, making CMOS ideal for low-power applications.

---
