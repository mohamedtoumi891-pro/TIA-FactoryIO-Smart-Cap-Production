<img width="787" height="880" alt="HMI interface" src="https://github.com/user-attachments/assets/e5d14875-ccf1-4541-ac9d-59f1b5882977" />
<img width="1917" height="907" alt="tia portail img" src="https://github.com/user-attachments/assets/5da94904-bad6-48c5-af9e-330812b1cdb1" />
# TIA Portal & Factory I/O: Integrated Assembly & Machining Line

This project features a sophisticated industrial automation system developed using **Siemens TIA Portal V17** and **Factory I/O**. It simulates a high-precision manufacturing environment where raw materials are machined into components, assembled, and sorted based on real-time production requirements.

## 1. System Architecture & Layout

The production floor is divided into four main zones: Feeding, Machining, Assembly, and Sorting. The logic is driven by a **SIMATIC S7-1500 PLC**, ensuring high-speed synchronization between the conveyors and the robotic cells.

![Factory I/O Production Line](https://raw.githubusercontent.com/placeholder-link-to-your-factoryio-img.jpg)
*Figure 1: Full Factory I/O 3D Simulation Environment*

### Process Workflow:
* **Feeding Unit**: A Pick & Place robot identifies raw material colors (Green/Blue) and feeds the primary conveyor.
* **Machining Center**: Two CNC stations transform raw blocks into "Lids" (6s process) and "Bases" (3s process).
* **Assembly Station**: A dedicated robotic arm performs the final "press-fit" assembly of the lid onto the base.
* **Sorting & Logistics**: Finished products are identified by color and diverted to their respective storage ramps.

---

## 2. Human-Machine Interface (HMI)

The HMI serves as the central "brain" for the operator. It allows for manual overrides, production target setting, and real-time data visualization.

| HMI Control Panel | Functional Explanation |
| :--- | :--- |
| ![HMI Interface](https://raw.githubusercontent.com/placeholder-link-to-your-hmi-img.jpg) | **Production Control:** <br> - **Start/Reset:** Initiates or clears the PLC sequence. <br> - **Stop Feeding:** Ceases raw material input while allowing current work-in-progress to finish. <br> - **Setpoint (V):** A potentiometer to adjust conveyor speeds or production rates. <br><br> **Data Monitoring:** <br> - **Counter:** Displays total units processed. <br> - **Product Tracking:** Individual counters for **Green** and **Blue** finished goods. <br> - **Safety:** Prominent Emergency Stop for immediate hardware interlocking. |

---

## 3. Automation Logic & Safety

### Fault Detection (Alarms)
The system is programmed with **Field-Related Alarms**. If a sensor fails to detect a part within a specific timeframe (Sequence Fault) or if a conveyor motor draws excessive current (Hardware Fault), the HMI triggers a diagnostic message and halts the affected zone.

### Technical Deliverables
1.  **PLC Logic**: Developed in LAD/SCL within TIA Portal.
2.  **HMI Design**: Multi-screen interface for monitoring and diagnostics.
3.  **Digital Twin**: Factory I/O scene configured for SIL (Software-in-the-Loop) testing.
4.  **Performance Report**: Analysis of cycle times (3s base vs 6s lid) and throughput optimization.

## 4. How to Run
1.  Open the `.factoryio` scene.
2.  Launch **TIA Portal V17** and open the `.ap17` project.
3.  Establish a connection via **PLCSIM**.
4.  Switch to the HMI view and press **Start** to begin the automated cycle.
