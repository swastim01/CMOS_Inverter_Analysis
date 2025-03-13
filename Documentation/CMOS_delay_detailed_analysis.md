# CMOS Inverter Delay - Detailed Analysis

## Introduction
The **delay of a CMOS inverter** is a critical performance parameter in digital circuits. It determines the **speed of signal propagation** and impacts overall system performance. Delay is primarily influenced by **parasitic capacitances, transistor sizing, and load conditions**.

## Key Delay Parameters

1. **Propagation Delay (tp)**
   - The time taken for the output to transition after the input changes.
   - Defined as:
     \[
     t_p = \frac{t_{PLH} + t_{PHL}}{2}
     \]
   - Where:
     - \( t_{PLH} \) = LOW-to-HIGH propagation delay.
     - \( t_{PHL} \) = HIGH-to-LOW propagation delay.

2. **Rise Time (tr)**
   - Time taken for output voltage to rise from **10% to 90%** of VDD.

3. **Fall Time (tf)**
   - Time taken for output voltage to fall from **90% to 10%** of VDD.

## Factors Affecting CMOS Delay

1. **Parasitic Capacitances**
   - Gate, drain, and interconnect capacitances impact the charging/discharging time.
   - The **RC time constant** (\( \tau = RC \)) determines the switching speed.

2. **Transistor Sizing (W/L Ratio)**
   - Affects drive strength and charge/discharge speed.
   - Increasing **Wn and Wp** can reduce delay but increases power consumption.

3. **Load Capacitance (CL)**
   - Larger capacitance increases delay:
     \[
     t_p \approx 0.69 R_{eq} C_L
     \]
   - Where:
     - \( R_{eq} \) is the equivalent resistance of the transistors.
     - \( C_L \) is the load capacitance.

4. **Supply Voltage (VDD)**
   - Higher VDD reduces delay but increases power dissipation.

5. **Process Variations**
   - Fabrication variations affect mobility, threshold voltage, and capacitances.

## Delay Measurement in Simulation

- The CMOS inverter delay can be analyzed using **transient analysis** in LTSpice.
- Key steps:
  1. Apply a **pulse input** (square wave).
  2. Observe the **output transition times**.
  3. Measure **tPLH, tPHL, tr, tf** using waveform analysis.
  4. Extract the **average propagation delay**.

## Simulation Results

- The simulation shows that **CMOS delay increases with load capacitance**.
- The **delay is asymmetric** due to different PMOS/NMOS mobility.
- Optimizing **transistor sizing** can minimize propagation delay.

## Conclusion

- **Lower CL → Faster switching speed.**
- **Wider transistors → Reduce resistance but increase power.**
- **Higher VDD → Reduces delay but affects power efficiency.**
- **Trade-offs between power, speed, and area** are crucial in circuit design.

---
