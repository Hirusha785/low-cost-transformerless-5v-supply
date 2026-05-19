# Low-Cost Transformerless 5V Supply

A compact **non-isolated transformerless AC-to-5V DC power supply PCB** designed using KiCad.

This project uses a capacitive dropper circuit, bridge rectifier, smoothing capacitors, zener protection, and an LM7805 voltage regulator to generate a low-current 5V DC output.

> ⚠️ **High Voltage Warning:**  
> This is a **non-isolated mains-powered circuit**. The 5V output is **not safely isolated** from AC mains.  
> Do not touch the circuit while powered. Do not connect it to USB, computers, Arduino boards, ESP32 boards, oscilloscopes, or any user-accessible circuit unless proper isolation is added.

---

## Repository Description

A compact non-isolated transformerless AC-to-5V DC power supply PCB using a capacitive dropper, bridge rectifier, zener protection, 7805 regulator, and LED power indicator.

---

## Project Overview

This PCB demonstrates a low-cost transformerless power supply design suitable for learning, testing, and sealed low-power applications.

The circuit converts AC mains input into regulated 5V DC through the following stages:

1. Capacitive voltage/current dropping stage
2. Bridge rectifier stage
3. DC smoothing and filtering stage
4. Zener overvoltage protection stage
5. 7805 linear voltage regulation stage
6. LED power indication stage

---

## Features

- Low-cost transformerless AC-to-DC design
- Compact PCB layout
- 5V regulated DC output
- Bridge rectifier using 1N4007 diodes
- Zener diode voltage protection
- LM7805 / 7805 TO-220 voltage regulator
- LED power indicator
- Screw terminal AC input
- Screw terminal 5V DC output
- Through-hole component design
- Designed in KiCad

---

## Circuit Operation 

AC mains input is connected through J1.
C4 works as the capacitive dropper and limits the input current.
R3 discharges C4 after power is removed.
D1–D4 form the bridge rectifier and convert AC to DC.
C1 filters high-frequency noise.
C2 smooths the rectified DC voltage and reduces ripple.
D5 and D6 provide Zener voltage protection/clamping.
R1 and R2 help limit current in the protection stage.
U1 is the 7805 voltage regulator and provides regulated 5V DC output.
C5 smooths the final 5V output.
D7 and R4 work as the power indicator circuit.
Since this is a transformerless design, the output is not isolated from AC mains and must be handled carefully.

---

## Main Components

| Reference | Component | Description |
|---|---|---|
| J1 | Screw Terminal | AC input connector |
| C4 | 225k / 2.2uF Capacitor | Capacitive dropper capacitor |
| R3 | 1MΩ | Dropper capacitor discharge resistor |
| D1 | 1N4007 | Bridge rectifier diode |
| D2 | 1N4007 | Bridge rectifier diode |
| D3 | 1N4007 | Bridge rectifier diode |
| D4 | 1N4007 | Bridge rectifier diode |
| C1 | 0.1uF | Noise filtering capacitor |
| C2 | 1000uF | DC smoothing capacitor |
| D5 | Zener Diode | Voltage protection/clamping |
| D6 | Zener Diode | Voltage protection/clamping |
| R1 | 20kΩ | Protection/bias resistor |
| R2 | 20kΩ | Protection/bias resistor |
| U1 | LM7805 / 7805 TO-220 | 5V voltage regulator |
| C5 | 470uF | Output smoothing capacitor |
| D7 | LED | Power indicator |
| R4 | 2.2kΩ | LED current-limiting resistor |
| J2 | Screw Terminal | 5V DC output connector |

---

## PCB Design

The PCB was designed using KiCad and includes:

- Through-hole components
- AC input screw terminal
- 5V DC output screw terminal
- Compact board layout
- Top and bottom routing
- 3D model preview
- Power indicator LED
- Mounting holes

---

## Project Images

### Circuit Schematic

<img width="1262" height="400" alt="image" src="https://github.com/user-attachments/assets/92ace52f-0f47-4f9e-a7d7-dd1c73052d8c" />

![Circuit Schematic](schematic/circuit_schematic.png)

---

### PCB Layout
<img width="851" height="659" alt="image" src="https://github.com/user-attachments/assets/e253e18b-10bd-440a-81dc-cf78d3940d15" />

![PCB Layout](pcb/pcb_layout.png)

---

### 3D View
<img width="1044" height="812" alt="image" src="https://github.com/user-attachments/assets/c8b6038b-a696-433d-87dd-5ee0f1e2cc72" />
<img width="1041" height="695" alt="image" src="https://github.com/user-attachments/assets/764469ae-08a8-4d1c-99b3-bc95fe86ff80" />
<img width="717" height="765" alt="image" src="https://github.com/user-attachments/assets/7c917602-c226-4a30-94c4-bea376a2ef3e" />
<img width="938" height="757" alt="image" src="https://github.com/user-attachments/assets/8d014ccc-e03c-44eb-9e0f-973e16904973" />

![3D View](3d-view/top_3d_view.png)


---

## Suitable Applications

This circuit may only be used in **sealed low-power applications**, such as:

- 💡 **Small indicator circuits**  
  For basic power indication or low-current status indication circuits inside closed equipment.

- 🔧 **Low-current control circuits**  
  For small internal control circuits where only a limited amount of current is required.

- 📦 **Enclosed appliance control boards**  
  Suitable only when the full PCB is mounted inside a properly insulated and sealed enclosure.

- 🎓 **Educational PCB design demonstrations**  
  Useful for learning about capacitive dropper supplies, rectification, filtering, zener protection, and basic voltage regulation.
