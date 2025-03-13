# DC Sweep Analysis of CMOS Inverter with Varying PMOS Width (Wp)

## Introduction
This analysis explores the impact of **PMOS width (Wp)** variation on the **Voltage Transfer Characteristics (VTC)** of a CMOS inverter. By sweeping **Wp**, we analyze how it affects:
- **Switching threshold voltage (Vth)**
- **Noise margins**
- **Power dissipation**

This study helps in optimizing transistor sizing for better performance.

---

## Effect of PMOS Width (Wp) on CMOS Inverter

### 1️⃣ Switching Threshold (Vth)
- **Vth** is the input voltage where **Vout = Vin**.
- Increasing **Wp** shifts **Vth lower** (PMOS gets stronger).
- Decreasing **Wp** shifts **Vth higher** (NMOS dominates).

### 2️⃣ Noise Margins
- **Noise margins change** based on the VTC curve.
- **Higher Wp** improves **NM_H (high-level noise margin)**.
- **Lower Wp** improves **NM_L (low-level noise margin)**.

### 3️⃣ Power Dissipation
- **DC power dissipation remains low** (due to minimal static current).
- **Short-circuit current may increase** for very high Wp.

---

## Simulation Setup in LTSpice

### **SPICE Directives Used**
```spice
.dc V2 0 1.8 0.02
.step param Wp 800n 1600n 400n
.include tsmc018.lib
```

### **Explanation**
- `.dc V2 0 1.8 0.02` → Sweeps **Vin** from **0V to 1.8V** in **0.02V steps**.
- `.step param Wp 800n 1600n 400n` → Varies **Wp** from **800nm to 1600nm** in **400nm increments**.
- `.include tsmc018.lib` → Loads **TSMC 180nm MOSFET models**.

---

## Observations from Simulation

### **1️⃣ VTC Curve Behavior**
- **For smaller Wp (800nm)**:
  - **NMOS dominates**, shifting **Vth right**.
  - **Better NM_L, worse NM_H**.

- **For larger Wp (1600nm)**:
  - **PMOS dominates**, shifting **Vth left**.
  - **Better NM_H, worse NM_L**.

### **2️⃣ Noise Margin Analysis**
- **Balancing Wp/Wn ratio is critical**.
- Optimal sizing ensures **equal noise margins**, improving circuit robustness.

### **3️⃣ Power Dissipation Trends**
- **Static power remains minimal**.
- **Short-circuit current may increase** for **very large Wp**.

---

## Conclusion
- **Wp directly influences switching behavior, noise margins, and power consumption**.
- **Optimizing Wp/Wn ratio is crucial for performance**.
- **A balanced design ensures robustness and efficiency**.

---
