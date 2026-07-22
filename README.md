# 🏎️ Formula Student India & Formula Bharat - Electronics Systems

Welcome to the definitive repository for **Formula Student India** and **Formula Bharat** electronics systems. 

This project serves as a comprehensive guide and resource hub for developing compliant, high-performance EV electronics. It bridges the gap between rulebook theory and practical hardware engineering, offering detailed rule-based explanations alongside production-ready hardware designs.

## 📜 Rulebook Compliance

All schematics and architectures in this repository are designed in compliance with the **2025/2026 Formula Bharat EV Rulebook** and the latest **FS India** regulations. Always cross-reference with the official rules before manufacturing.

## 📌 Repository Overview

Designing electronics for Formula Student requires a strict balance of safety, performance, and rule compliance. This repository provides:
*   **Rule-Based Explanations:** Deep dives into EV regulations to explain *why* systems are designed the way they are.
*   **Schematic Designs:** Robust, industry-standard circuit designs for critical EV accumulator and tractive system components.
*   **Manufacturing-Ready Files:** Complete Gerber files ready for PCB fabrication.

*(Optional: Insert a high-level System Architecture Block Diagram or 3D PCB render below)*
`![System Architecture Placeholder](docs/images/system_architecture.png)`

## 🛠️ Prerequisites & Technologies

The designs and architectures within this repository are built utilizing industry-standard hardware engineering tools. To view, modify, or compile these files, you will need:
*   **PCB Design & EDA:** Altium Designer (v20+ recommended), Cadence Allegro, or OrCAD
*   **Embedded Systems:** STM32 Microcontrollers
*   **Firmware:** STM32CubeIDE

## 📂 Suggested Directory Structure

```text
📦 Formulastudentindia
 ┣ 📂 Documentation      # Rule breakdowns, system architecture guides, and block diagrams
 ┣ 📂 Schematics         # Source files (OrCAD, Altium) and PDF exports
 ┣ 📂 Gerbers            # Manufacturing-ready PCB files for fabrication
 ┣ 📂 Firmware           # STM32 embedded C code examples
 ┗ 📜 README.md
```

## 🚀 Getting Started

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/buildbyshree/Formulastudentindia.git](https://github.com/buildbyshree/Formulastudentindia.git)
   ```
2. **Review the Documentation:** Start with the `Documentation` folder to understand the specific EV rule constraints (e.g., Accumulator Management System, Tractive System Active Light, Shutdown Circuit) before diving into the schematics.
3. **Open the Designs:** Use your preferred EDA tool to view and modify the source schematics. 

## 📄 License

*   **Hardware/Schematics:** Released under the [CERN Open Hardware Licence Version 2 - Strongly Reciprocal (CERN-OHL-S)](https://ohwr.org/cernohl). 
*   **Firmware/Software:** Released under the [MIT License](https://opensource.org/licenses/MIT).

## 👨‍💻 About the Author

**Shriyog Jambekar**  
*Hardware Design Engineer | Electric Technical Inspector @ Formula Bharat*

Driven by a passion for embedded systems, this repository was created to help teams navigate the complex electrical design challenges of Formula Student. By sharing these schematics and rule interpretations, the goal is to elevate the overall engineering standard across the paddock.

---
*If you find this repository helpful, consider leaving a ⭐!*
