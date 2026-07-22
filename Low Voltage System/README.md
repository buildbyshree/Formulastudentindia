# Low Voltage (LV) System

The Low Voltage (LV) system provides electrical power to the control, safety, communication, sensing, and data acquisition systems of a Formula Student vehicle.

A well-designed LV system should provide reliable power distribution while protecting the vehicle electronics against electrical faults and environmental conditions.

> **Note:** This section provides general engineering guidance. Always refer to the latest applicable Formula Bharat and Formula Student rules for specific requirements.

---

## 1. Purpose of the LV System

The LV system is responsible for supplying power to various electronic systems in the vehicle.

Depending on the vehicle architecture, these may include:

- Vehicle Control Unit (VCU)
- Electronic Control Units (ECUs)
- Accumulator Management System (AMS)
- Sensors
- Dashboard
- Data acquisition system
- Telemetry system
- Communication modules
- Safety-related control circuits
- Cooling system controls
- Pumps and fans
- Relays and contactors

The exact components and architecture depend on the type of vehicle and the team's design.

---

## 2. Typical LV System Architecture

A simplified LV architecture may look like:

```text
LV Battery / LV Power Source
            │
            ▼
       Main Protection
         (Fuse)
            │
            ▼
      LV Master Switch
            │
            ▼
     Power Distribution
            │
    ┌───────┼────────┬──────────┐
    │       │        │          │
    ▼       ▼        ▼          ▼
   VCU     ECUs    Sensors    Dashboard
    │
    ├── Communication
    │
    └── Control Outputs
```

This is only a conceptual example. The actual architecture will depend on the vehicle design and applicable rules.

---

## 3. LV Power Source

The LV power source provides energy for the low-voltage electrical system.

When selecting or designing an LV power source, teams should consider:

- Nominal voltage
- Maximum and minimum operating voltage
- Required capacity
- Maximum continuous current
- Peak current requirements
- Battery chemistry
- Protection requirements
- Weight
- Packaging
- Accessibility
- Charging requirements

The power source should be capable of supplying all connected loads under expected operating conditions.

---

## 4. Power Budget

Before designing the LV power distribution system, teams should estimate the total electrical load.

A simple power budget can be created by listing each load:

| Device | Voltage | Typical Current | Peak Current |
|---|---:|---:|---:|
| VCU | TBD | TBD | TBD |
| Dashboard | TBD | TBD | TBD |
| Sensors | TBD | TBD | TBD |
| Cooling Fan | TBD | TBD | TBD |
| Pump | TBD | TBD | TBD |
| Telemetry | TBD | TBD | TBD |

The values should be obtained from component datasheets or verified through testing.

The LV power source and wiring should be designed considering both continuous and peak current requirements.

---

## 5. Power Distribution

Power distribution is responsible for safely delivering electrical power from the LV source to different loads.

A typical distribution system may include:

- Main fuse
- Branch fuses
- Relays
- Power distribution modules
- Connectors
- Wiring harnesses
- Ground distribution

Where practical, individual loads or groups of loads should have appropriate protection.

This can help prevent a fault in one subsystem from damaging other parts of the vehicle electrical system.

---

## 6. Fuse Selection

Fuses are used to protect wiring and electrical systems against excessive current.

Fuse selection should consider:

- Normal operating current
- Maximum expected current
- Inrush current
- Wire current-carrying capability
- Fault current
- Fuse response characteristics

A fuse should primarily protect the wiring and downstream circuit from excessive current.

Simply selecting a fuse based only on the nominal current of the connected device may not provide adequate protection.

---

## 7. Wire Selection

Wire sizing should consider:

- Continuous current
- Peak current
- Wire length
- Voltage drop
- Ambient temperature
- Bundling
- Mechanical strength
- Insulation rating

Long wire runs can introduce significant voltage drop, especially for high-current loads such as pumps and fans.

Teams should verify that the voltage available at the load remains within the device's acceptable operating range.

---

## 8. Grounding Strategy

A good grounding strategy is important for reliable vehicle electronics.

Poor grounding can result in:

- Sensor measurement errors
- Communication problems
- Ground loops
- Unexpected ECU resets
- Electrical noise
- Intermittent faults

Teams should carefully plan:

- Power grounds
- Signal grounds
- High-current return paths
- Sensor reference grounds
- Shield connections

High-current return paths should be designed so that they do not introduce unwanted voltage differences into sensitive sensor or communication circuits.

---

## 9. Voltage Regulation

Different electronic systems may require different voltage levels.

For example, a vehicle may contain:

```text
LV Battery
    │
    ├── Battery Voltage
    │
    ├── 12 V Rail
    │
    ├── 5 V Rail
    │
    └── 3.3 V Rail
```

Voltage conversion may be achieved using:

- Buck converters
- Boost converters
- Buck-boost converters
- Linear regulators

Regulator selection should consider efficiency, thermal performance, output current, input voltage range, transient response, and electromagnetic interference.

---

## 10. Protection

Vehicle electronics may experience electrical disturbances during operation.

Depending on the application, protection may be considered against:

- Reverse polarity
- Overcurrent
- Overvoltage
- Voltage transients
- Electrostatic discharge (ESD)
- Short circuits
- Inductive load switching

Possible protection components include:

- Fuses
- TVS diodes
- Reverse polarity protection circuits
- Flyback diodes
- Filtering components
- Current limiting devices

Protection should be selected based on the expected electrical environment and the requirements of the connected equipment.

---

## 11. Inductive Loads

Relays, contactors, solenoids, pumps, and motors can generate voltage transients when switched.

Appropriate suppression techniques may be required.

Examples include:

- Flyback diodes
- TVS diodes
- RC snubbers

The appropriate solution depends on the type of load and required switching behavior.

---

## 12. Connectors

Connector selection is an important part of LV system reliability.

Consider:

- Current rating
- Voltage rating
- Number of mating cycles
- Vibration resistance
- Locking mechanism
- Environmental sealing
- Contact resistance
- Wire size compatibility
- Ease of assembly

Connectors should be mechanically secured and protected against accidental disconnection where required.

---

## 13. Communication Wiring

Communication networks such as CAN should be designed separately from high-current power wiring where practical.

Consider:

- Twisted pair wiring
- Correct termination
- Network topology
- Shielding where necessary
- Routing away from noisy power circuits

Poor communication wiring can result in intermittent faults that may be difficult to diagnose.

---

## 14. Testing and Validation

The LV system should be tested before integration into the complete vehicle.

Useful tests may include:

- Continuity testing
- Short-circuit checks
- Insulation checks where applicable
- Power consumption measurement
- Voltage-drop measurement
- Fuse verification
- Load testing
- Connector inspection
- Ground integrity testing
- Communication testing

Testing should also be performed under realistic operating conditions.

For example, teams should verify the LV voltage while high-current loads such as pumps and fans are operating.

---

## 15. Documentation

Teams should maintain clear documentation of the LV electrical system.

Useful documents include:

- System block diagram
- Electrical schematic
- Wiring diagram
- Harness drawing
- Connector pinout
- Fuse list
- Power budget
- Bill of Materials (BOM)

Good documentation makes manufacturing, troubleshooting, maintenance, and technical inspection significantly easier.

---

## 16. Common Design Mistakes

Common LV system design issues may include:

- Incorrect fuse sizing
- Undersized wires
- Excessive voltage drop
- Poor grounding
- Missing protection circuits
- Inadequate connector locking
- Poor harness routing
- Insufficient strain relief
- Inadequate documentation
- No consideration of peak current
- Mixing noisy power circuits with sensitive signal wiring

Teams should review the complete LV architecture before manufacturing the wiring harness.

---

## 17. Recommended Design Process

A structured LV design process can be:

```text
Identify Electrical Loads
        │
        ▼
Create Power Budget
        │
        ▼
Select LV Power Source
        │
        ▼
Design Power Distribution
        │
        ▼
Select Fuses and Wiring
        │
        ▼
Select Connectors
        │
        ▼
Design Protection
        │
        ▼
Create Schematics
        │
        ▼
Create Wiring / Harness Documentation
        │
        ▼
Build and Test
        │
        ▼
Vehicle Integration
        │
        ▼
Validation
```

---

## 18. Rule References

Teams should verify the latest applicable rules related to:

- Low-voltage systems
- Grounded Low Voltage (GLV) systems
- Electrical system isolation
- Wiring
- Fusing
- Master switches
- Connectors
- Tractive System and LV separation for EVs

Rule numbers and requirements may change between competition seasons.

Always refer to the latest official Formula Bharat and applicable Formula Student rules.

---

## Disclaimer

This repository is an independent, community-driven educational resource. It is not officially affiliated with or endorsed by Formula Bharat or any Formula Student organization.

The information provided here is intended for educational purposes and should not be considered a replacement for official competition rules.

Always refer to the latest official rules applicable to your competition. In case of any discrepancy, the official rules take precedence.