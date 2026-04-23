# TIA-FactoryIO-Smart-Cap-Production

This project implements a fully functioning production line simulation using **Factory I/O** and **Siemens TIA Portal V17**. The system automates the manufacturing of "Smart Bottle Caps," covering the entire lifecycle from raw material feeding to machining, assembly, and color-coded sorting.

---

## 1. Production Line Design & Simulation

The layout consists of a synchronized flow managed by a **SIMATIC S7-1500 PLC**. It integrates robotic pick-and-place units with CNC machining centers.

![Factory I/O Production Line](tia%20portail%20img.jpg)
*Figure 1: Overview of the Smart Cap Production Floor in Factory I/O*

### Process Flow:
* **Feeding**: Random raw materials (Green/Blue) are placed onto the line.
* **Machining**: CNC stations fabricate **Bases** (3s) and **Lids** (6s).
* **Assembly**: Components are pressed together to form the final product.
* **Sorting**: Finished caps are sorted by color into designated storage ramps.

---

## 2. Human-Machine Interface (HMI)

The HMI was developed in TIA Portal to provide real-time supervisory control and data acquisition (SCADA) for the operator.

| HMI Control Panel View | Functional Description & Control |
| :--- | :--- |
| ![HMI Interface](HMI%20interface.jpg) | **Control Commands:** <br> - **Start/Reset**: Master control for the PLC sequence. <br> - **Stop Feeding**: Halts new material while clearing the line. <br> - **Setpoint (V)**: Analog adjustment for conveyor speed. <br><br> **Live Statistics:** <br> - **Counter**: Total throughput of the plant. <br> - **Color Sort**: Specific tracking for Green vs. Blue products. <br> - **Safety**: Integrated Emergency Stop monitoring. |

---

## 3. Fault Detection & Alarms

To ensure industrial-grade reliability, the system includes:
* **Sequence Monitoring**: Detects if a part is stuck between stations.
* **Hardware Interlocks**: The HMI displays field-related alarms for any component failure.
* **Emergency Protocols**: Immediate halting of all actuators upon E-Stop activation.

## 4. Setup Instructions

1. **Factory I/O**: Open the provided `.factoryio` scene file.
2. **TIA Portal**: Open the `.ap17` project and download the hardware configuration to **PLCSIM**.
3. **Operation**: Switch the PLC to 'RUN' mode and use the HMI Start button to begin.
