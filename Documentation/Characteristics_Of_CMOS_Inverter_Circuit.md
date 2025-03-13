# Characteristics of CMOS Inverter Circuit

## Introduction
A CMOS (Complementary Metal-Oxide-Semiconductor) inverter is a fundamental building block in digital logic design. It consists of a PMOS transistor and an NMOS transistor connected in series, operating as a NOT gate. The circuit's behavior is determined by the voltage transfer characteristics (VTC), which define the relationship between input and output voltages.

## Circuit Description
The CMOS inverter consists of:
- **PMOS Transistor (M2)**: Positioned at the top, connected to VDD. It turns ON when the input is LOW (0V).
- **NMOS Transistor (M1)**: Positioned at the bottom, connected to GND. It turns ON when the input is HIGH (VDD).
- **Input Voltage (Vin)**: Controls the switching between HIGH and LOW states.
- **Output Voltage (Vout)**: The logical inverse of the input voltage.

## Operating Regions
The CMOS inverter operates in three main regions:

1. **Region 1 (Vin = 0V)**
   - PMOS is ON (strong conduction).
   - NMOS is OFF.
   - Output is HIGH (VDD).

2. **Region 2 (Vin ≈ VDD/2)**
   - Both PMOS and NMOS are partially conducting.
   - Creates a transition region in VTC.

3. **Region 3 (Vin = VDD)**
   - PMOS is OFF.
   - NMOS is ON (strong conduction).
   - Output is LOW (0V).

## Voltage Transfer Characteristics (VTC)
The **VTC Curve** of a CMOS inverter is a sigmoidal graph showing the relationship between **Vin** and **Vout**:
- **Noise Margins**: Defined as **NMH** (High Noise Margin) and **NML** (Low Noise Margin).
- **Switching Threshold (Vth)**: The input voltage at which Vout = VDD/2.

## Applications
- **Logic Gates**: Forms the basis of NAND, NOR, and XOR gates.
- **Microprocessors & Digital Circuits**: Essential in VLSI design.
- **Low-Power Applications**: Used due to low static power dissipation.

## Simulation Results
- The circuit simulation shows the transition curve from HIGH to LOW.
- The output follows the expected **inverted response**.
- Voltage transfer characteristics confirm the proper working of the inverter.

---


