# Electrical System Overview

This section provides a high-level overview of the electrical and electronic systems commonly used in Formula Student vehicles. It is intended to help teams understand the overall system architecture and how different electrical subsystems interact with each other.

> **Note:** This guide is intended for educational purposes. Always refer to the latest official competition rules applicable to your event.

## 1. Electrical System Categories

The vehicle electrical system can broadly be divided into:

- Low Voltage (LV) System
- Tractive System (TS) — applicable to Electric Vehicles
- Safety and Shutdown Systems
- Communication Systems
- Data Acquisition and Telemetry Systems

The exact architecture will vary depending on the vehicle type, team design choices, and applicable competition rules.

---

## 2. Low Voltage (LV) System

The Low Voltage (LV) system supplies power to the vehicle's control, communication, safety, and data acquisition electronics.

Typical components connected to the LV system may include:

- Electronic Control Units (ECUs)
- Vehicle Control Unit (VCU)
- Sensors
- Dashboard and driver controls
- Data acquisition systems
- Communication interfaces
- Safety-related control circuits

The LV system typically consists of an LV battery or another permitted power source, power distribution, protection devices, wiring harnesses, connectors, and electronic control modules.

Good LV system design should consider:

- Appropriate voltage levels
- Current requirements
- Wire sizing
- Fuse and circuit protection
- Connector selection
- Grounding strategy
- Electromagnetic compatibility (EMC)
- Reliability and serviceability

---

## 3. Tractive System (TS)

In an Electric Vehicle (EV), the Tractive System is responsible for delivering electrical energy from the accumulator to the motor or motors used for propulsion.

A typical tractive system may include:

- Accumulator
- Accumulator Management System (AMS)
- Accumulator Isolation Relays (AIRs)
- Precharge circuit
- Discharge circuit
- Inverter or motor controller
- Electric motor
- High-voltage cables and connectors
- Tractive System Active Light (TSAL)
- Isolation monitoring devices

Because the Tractive System may operate at hazardous voltage and energy levels, its design requires careful consideration of electrical isolation, insulation, protection, interlocking, and safe shutdown.

The exact implementation must comply with the latest applicable competition rules.

---

## 4. Safety and Shutdown Systems

Safety systems are designed to place the vehicle into a safe state when certain faults or unsafe operating conditions are detected.

Depending on the vehicle category and applicable rules, these systems may include:

- Shutdown Circuit
- Brake System Plausibility Device (BSPD)
- Accumulator Management System (AMS)
- Insulation Monitoring Device (IMD)
- Emergency shutdown buttons
- Brake over-travel protection
- Interlocks

Safety-related systems should be designed so that critical faults can be detected and the appropriate shutdown action can occur reliably.

Teams should consider both normal operation and possible failure conditions during the design and validation process.

---

## 5. Communication Systems

Modern Formula Student vehicles typically contain multiple electronic modules that need to exchange information.

Common communication interfaces may include:

- CAN
- UART
- SPI
- I2C
- Ethernet

CAN is commonly used for communication between distributed vehicle controllers because of its robustness and suitability for automotive applications.

Communication system design should consider:

- Network topology
- Termination
- Bit rate
- Message prioritization
- Error handling
- Connector and wiring selection
- Electromagnetic interference

---

## 6. Data Acquisition and Telemetry

Data acquisition systems allow teams to monitor vehicle performance and analyze system behavior.

Typical parameters may include:

- Battery voltage
- Cell voltages
- Temperatures
- Motor speed
- Wheel speed
- Brake pressure
- Accelerator position
- Steering angle
- Current consumption
- Vehicle acceleration

Depending on the team's architecture, data may be stored locally or transmitted using a telemetry system.

A well-designed data acquisition system can help with:

- Vehicle development
- Troubleshooting
- Driver analysis
- Performance optimization
- Reliability monitoring

---

## 7. Example High-Level Architecture

A simplified EV electrical architecture can be represented as:

```text
Accumulator
    │
    ▼
AIRs / Precharge System
    │
    ▼
Inverter
    │
    ▼
Motor
```

The LV electrical system may simultaneously support:

```text
LV Power Source
    │
    ▼
Power Distribution
    │
    ├── VCU
    ├── ECUs
    ├── Sensors
    └── Dashboard
```

Communication networks such as CAN can connect the major electronic control units.

Safety systems monitor critical vehicle conditions and interact with the shutdown system when required.

> **Note:** This is a simplified conceptual architecture. Actual implementations will vary between teams and must comply with applicable competition rules.

---

## 8. Design Philosophy

When developing a Formula Student electrical system, teams should consider:

- Safety
- Rule compliance
- Reliability
- Simplicity
- Testability
- Maintainability
- Documentation
- Fault detection
- Ease of troubleshooting

A system that performs well under ideal conditions but is difficult to test or troubleshoot can create significant challenges during vehicle development and technical inspection.

Teams should design their electrical systems with testing and validation in mind from the beginning.

---

## 9. Further Topics

More detailed sections of this repository will cover individual systems and topics such as:

- Low Voltage System Design
- Tractive System Architecture
- Shutdown Circuit
- BSPD
- Accumulator and AMS
- Precharge and Discharge Circuits
- CAN Communication
- Wiring and Harness Design
- PCB Design
- Sensors and Data Acquisition
- Testing and Validation
- Common Electrical Design Mistakes

---

## Disclaimer

This repository is an independent, community-driven educational resource. It is not officially affiliated with or endorsed by Formula Bharat or any Formula Student organization.

The information provided here should not be considered a replacement for official competition rules.

Always refer to the latest official rules and technical documentation applicable to the competition you are participating in. In case of any discrepancy, the official rules take precedence.