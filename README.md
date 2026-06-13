# Die Casting SPS Machine S200 - PLC Automation System

## 📌 Project Overview
This repository contains the Programmable Logic Controller (PLC) firmware, hardware configurations, and sequence logic for the **SPS S200 Die Casting Machine**. The system is engineered to handle precise thermal monitoring, high-pressure injection control, mold clamping, and part ejection sequences required in heavy-duty aluminum or zinc die casting.

The codebase utilizes high-performance sequence tracking and memory management to ensure low latency and high reliability during continuous industrial cycles.

---

## 🏗️ System Architecture & Architecture Components

The automation firmware is built using structural blocks that manage specific hardware actions:

### 1. Main Sequencer (SPS Control)
* **Core Loop:** Orchestrates the step-by-step casting phase transitions (Clamping ➔ Injection ➔ Cooling ➔ Ejection).
* **Interlocking:** Strict safety logic prevents injection execution unless the mold is fully closed and locked under specified hydraulic pressures.

### 2. Injection & Pressure Profiles
* Controls multi-stage velocity and intensification pressures.
* Features real-time monitoring of real-time hydraulic pressures to prevent flash or short-shots.

### 3. Thermal & Core Management
* PID loops manage die pre-heating and continuous cooling cycles to maximize mold longevity and part quality.
* Manages core-pulling configurations (hydraulic cylinders moving internal die features).

---

## 📂 Repository Structure

```text
├── config/             # Hardware configuration files and network topologies
├── src/
│   ├── Main_Seq.scl    # Main operational sequence loop
│   ├── Injection.scl   # Injection speed & pressure intensification logic
│   ├── Safeties.scl    # E-Stop, safety gates, and pressure interlocks
│   └── Alarms.scl      # Error handling and diagnostic routines
├── hmi/                # HMI screen tags and layout assets
└── docs/               # IO mapping, electrical schematics, and timing diagrams
