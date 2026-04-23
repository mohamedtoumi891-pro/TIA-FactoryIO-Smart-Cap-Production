# TIA-FactoryIO-Smart-Cap-Production

This project implements a fully functioning production line simulation using **Factory I/O** and **Siemens TIA Portal V17**. The system automates the manufacturing of "Smart Bottle Caps," covering the entire lifecycle from raw material feeding to machining, assembly, and color-coded sorting. The system is controlled by a **SIMATIC S7-1500 PLC** and includes a custom **HMI interface** for monitoring and supervisory control.

---

## 1. Project Directory Structure

The project is organized into specific directories for the simulation environment and the PLC/HMI automation logic.

```text
TIA-FACTORY-IO/
├── PLC-HMI-Code/             # Siemens TIA Portal Project Folder
│   ├── ff.ap17               # Main TIA Portal Project File (V17)
│   ├── System/               # PLC System Configuration
│   └── [Internal Folders]    # IM, Logs, XRef, AdditionalFiles
├── Production-Line-Scene     # Factory I/O Scene File
├── HMI interface.png         # HMI Screenshot for Documentation
└── tia portail img.png       # Factory I/O Screenshot for Documentation
