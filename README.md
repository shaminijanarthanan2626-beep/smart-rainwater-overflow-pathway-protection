# Smart Flood / Waterlogging Access Control System

## 📌 Project Overview

The **Smart Flood / Waterlogging Access Control System** is a low-cost,
sensor-based safety system designed to help prevent people from entering
potentially dangerous waterlogged or flooded areas.

During heavy rainfall and floods, water may accumulate on roads,
pathways, and low-lying areas. In such situations, people may not always
have a clear indication that an area is unsafe. Our system combines
**hazard detection, person detection, warning, and automatic gate
control** to provide an active safety mechanism.

The prototype uses an **IR sensor to detect an approaching person** and
a microcontroller to control a **servo-based gate mechanism**. The
system can be extended with a water-level sensor to automatically
identify hazardous water conditions.

------------------------------------------------------------------------

## 🎯 Problem Statement

Flooding and waterlogging can make roads and other accessible areas
dangerous. Since warning signs or barriers may not always be available,
people can unknowingly approach or enter these areas.

There is a need for a simple and affordable system that can:

-   Detect hazardous water accumulation.
-   Detect people approaching the affected area.
-   Provide an immediate warning.
-   Control access to the dangerous zone automatically.

------------------------------------------------------------------------

## 💡 Proposed Solution

Our system provides an **automatic access-control mechanism** for
flood-prone or waterlogged areas.

The system works by combining:

1.  **Water-level / water-detection sensing** to identify a hazardous
    condition.
2.  **IR-based person detection** to detect someone approaching the
    restricted area.
3.  **Microcontroller-based decision making** to process sensor inputs.
4.  **Servo motor control** to operate a miniature gate.
5.  **LED, buzzer, and LCD-based indication** for visual and audible
    warnings.

The current prototype demonstrates the **IR-based person detection and
automatic gate-control concept**.

------------------------------------------------------------------------

## ⚙️ Working Principle

### Step 1 --- Monitor the Area

A water-level or water-detection sensor can be positioned near the
waterlogged area.

When the water reaches a predefined threshold, the system can classify
the location as hazardous.

### Step 2 --- Detect an Approaching Person

An IR sensor is positioned near the access point.

When a person approaches the gate, the IR sensor detects their presence
and sends a signal to the microcontroller.

### Step 3 --- Process the Sensor Data

The microcontroller evaluates the sensor conditions and determines the
appropriate action.

### Step 4 --- Control the Gate

A servo motor receives the control signal from the microcontroller and
operates the gate mechanism.

When the area is unsafe, the gate can remain closed or access can
otherwise be restricted.

### Step 5 --- Provide a Warning

The system can use an LCD, LED, and buzzer to communicate the condition
to the approaching person.

Example messages:

``` text
WATER LEVEL HIGH
DANGER - DO NOT ENTER
AREA RESTRICTED
```

------------------------------------------------------------------------

## 🔄 System Flow

``` text
        ┌─────────────────────┐
        │ Water Level /       │
        │ Water Detection     │
        │ Sensor              │
        └──────────┬──────────┘
                   │
                   ▼
        ┌─────────────────────┐
        │                     │
        │    MICROCONTROLLER  │
        │       (Arduino)     │
        │                     │
        └──────┬────────┬─────┘
               │        │
               │        │
               ▼        ▼
       ┌────────────┐  ┌──────────────┐
       │ Servo Motor│  │ Warning Unit │
       │ / Gate     │  │ LED + Buzzer │
       └────────────┘  │ + LCD        │
                       └──────────────┘
               ▲
               │
       ┌───────┴───────┐
       │   IR Sensor   │
       │ Person Detect.│
       └───────────────┘
```

------------------------------------------------------------------------

## 🧰 Components Used

  Component                              Purpose
  -------------------------------------- ---------------------------------------
  Arduino / Microcontroller              Main control and decision-making unit
  IR Sensor                              Detects an approaching person
  Water-level / Water-detection Sensor   Detects water accumulation
  SG90 Servo Motor                       Operates the miniature gate
  16×2 LCD                               Displays system status and warnings
  Buzzer                                 Provides audible warning
  LEDs                                   Provides visual indication
  Breadboard                             Prototype circuit assembly
  Jumper Wires                           Circuit connections
  5V Power Supply                        Provides power to the circuit

> **Note:** The exact water-sensing component can be changed depending
> on the final prototype implementation.

------------------------------------------------------------------------

## 🔌 Prototype Architecture

``` text
IR Sensor
    │
    ▼
┌───────────────┐
│               │
│    Arduino    │◄──── Water-Level Sensor
│               │
└───────┬───────┘
        │
   ┌────┼─────────────┐
   │    │             │
   ▼    ▼             ▼
Servo  LCD          Buzzer
Gate   Display      + LED
```

------------------------------------------------------------------------

## ✨ Key Innovation

The main concept of this project is the integration of:

**Environmental Hazard Detection + Human Detection + Warning + Physical
Access Control**

Instead of depending only on a warning board or electronic notification,
the proposed system can provide a **physical barrier** at the entrance
of a hazardous waterlogged area.

### Key innovative aspects

-   **Person-aware safety mechanism** using an IR sensor.
-   **Automatic gate control** instead of manual intervention.
-   **Local operation** without requiring continuous Internet
    connectivity.
-   **Low-cost and modular architecture**.
-   Can be expanded with additional environmental sensors.

------------------------------------------------------------------------

## 🚀 Advantages

-   Helps reduce the risk of people entering hazardous waterlogged
    areas.
-   Provides an immediate warning when a person approaches.
-   Automatic operation reduces the need for manual monitoring.
-   Low-cost components make the prototype affordable.
-   Can operate locally without depending entirely on Internet
    connectivity.
-   Modular design allows additional sensors to be integrated.
-   Can be adapted for different temporary or permanent restricted
    zones.

------------------------------------------------------------------------

## 📍 Potential Applications

The concept can be adapted for:

-   Flood-prone roads
-   Waterlogged streets
-   Low-lying areas
-   Underground passages
-   Drainage zones
-   Construction areas
-   Temporary flood barriers
-   Restricted environmental hazard zones

------------------------------------------------------------------------

## 🔮 Future Enhancements

The prototype can be further developed by adding:

### IoT Monitoring

Upload water-level and system status data to an online dashboard.

### GPS Integration

Transmit the location of a hazardous area.

### GSM Alerts

Send SMS notifications to responsible authorities when dangerous water
levels are detected.

### Solar Power

Use solar energy for outdoor deployment.

### Multi-Level Water Detection

``` text
LOW LEVEL
   ↓
SAFE

MEDIUM LEVEL
   ↓
CAUTION

HIGH LEVEL
   ↓
DANGER
   ↓
ACCESS RESTRICTION
```

### Multi-Sensor Hazard Detection

The system can combine:

-   Water level
-   Rainfall
-   Person detection
-   Road/environmental conditions

to improve the reliability of the safety decision.

------------------------------------------------------------------------

## 🧪 Prototype Demonstration

The prototype demonstrates the interaction between the **IR sensor,
Arduino, and servo-based gate mechanism**.

When a person is detected by the IR sensor, the Arduino processes the
sensor signal and controls the gate mechanism according to the
programmed condition.

The system can subsequently be integrated with a water-level detection
stage to create a complete flood/waterlogging access-control system.

------------------------------------------------------------------------

## 🛠️ Technologies Used

-   Arduino
-   Embedded C / Arduino IDE
-   IR sensing
-   Servo motor control
-   LCD interfacing
-   Basic sensor-based automation

------------------------------------------------------------------------

## 📊 System Logic

``` text
START
  │
  ▼
Monitor Area
  │
  ▼
Hazardous Water Condition?
  │
  ├── NO ──► Normal Mode
  │
  └── YES
        │
        ▼
   Activate Warning
        │
        ▼
   Detect Person
        │
        ▼
   Person Detected?
        │
        ├── NO ──► Continue Monitoring
        │
        └── YES
              │
              ▼
       Restrict / Control Access
              │
              ▼
       Continue Monitoring
```

------------------------------------------------------------------------

## 👥 Project Objective

The objective of this project is to develop a **simple, affordable, and
scalable safety mechanism** that can automatically regulate access to
potentially dangerous waterlogged areas and provide an immediate warning
to approaching people.

------------------------------------------------------------------------

## 📌 Conclusion

The Smart Flood / Waterlogging Access Control System demonstrates how
simple embedded-system components can be combined to address a
real-world safety problem.

By integrating **sensor-based hazard detection, IR-based human
detection, automatic gate control, and warning indicators**, the system
provides an active approach to restricting access to potentially
hazardous areas.

The prototype provides a foundation for future development into an
IoT-enabled, GPS-supported, solar-powered flood safety system.

------------------------------------------------------------------------

## 📄 Project Status

**Prototype Stage**

Current demonstration: - ✅ IR-based person detection - ✅
Microcontroller-based control - ✅ Servo-based gate mechanism - ✅ Basic
warning/indication interface

Planned/expandable: - ⬜ Water-level-based hazard detection - ⬜ IoT
monitoring - ⬜ GPS location reporting - ⬜ GSM emergency alerts - ⬜
Solar-powered operation

------------------------------------------------------------------------

## 👤 Author

**Shamini**

------------------------------------------------------------------------

## 🤝 Contributors

This project was developed as a team effort by **3 team members**, who
collaborated on the design, prototyping, and documentation of the
system:

-   **Shamini** — *(add your role, e.g. Documentation / Hardware / Coding)*
-   **[Team Member 2 Name]** — *(add their role)*
-   **[Team Member 3 Name]** — *(add their role)*

> Replace the placeholder names above with your teammates' names, and
> feel free to add what each person worked on (e.g. circuit design,
> coding, testing, documentation).

------------------------------------------------------------------------

## ⚠️ Safety Note

This prototype is intended for **educational and research demonstration
purposes**. A real-world deployment would require appropriate
waterproofing, electrical isolation, environmental testing, reliable
sensor calibration, mechanical safety testing, and validation under
actual flood conditions.
