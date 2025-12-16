# 💻 **Multi-Sensor-Based Finite State Machine (FSM) Control Architecture**

### *An HDL and Supervisory C# Implementation Study for Automated Liquid Filling Systems*

---

## 👩‍💻 **Author**

**Sintia Ompusunggu_2042241113**
Department of Instrumentation Engineering
Institut Teknologi Sepuluh Nopember (ITS)

📅 **Year:** 2025

---

## 📘 **Project Overview**

This repository contains the complete **HDL design, simulation results, and Supervisory C# implementation** supporting the research paper:

> **“Multi-Sensor-Based Finite State Machine (FSM) Control Architecture for Optimized Liquid Filling Precision:
> An HDL and Supervisory C# Implementation Study.”**

The project presents an **Automatic Bottle Filling System** controlled using an **8-State Mealy Finite State Machine (FSM)** integrating **multi-sensor inputs**, **safety logic**, and **actuator coordination**.
The system is further analyzed using **state transition matrices** and extended into a **quantum logic representation** to demonstrate design scalability toward reversible and quantum computation models.

---

## 🎯 **Research Objectives**

The main objectives of this work are:

* ✅ Design a deterministic **FSM-based control architecture** for liquid filling automation
* ✅ Integrate **6 digital sensors** and **6 actuators** under safety constraints
* ✅ Implement FSM logic using **HDL (Verilog)** and verify it through waveform simulation
* ✅ Develop a **Supervisory Control Application using C#** to validate state transitions
* ✅ Represent FSM behavior using **matrix representation and bra–ket notation**
* ✅ Demonstrate the feasibility of **quantum gate mapping** (Toffoli, CNOT) for critical actuators

---

## 🧩 **System Architecture Overview**

```
┌────────────────────────────┐
│      Supervisory Layer     │
│        C# Application      │
│  (State Monitoring & GUI)  │
└──────────────┬─────────────┘
               │
┌──────────────▼─────────────┐
│     FSM Control Logic      │
│   HDL (Verilog - Mealy)    │
│   8 States, 3 JK FFs       │
└──────────────┬─────────────┘
               │
┌──────────────▼─────────────┐
│ Sensors & Actuators Layer  │
│ I1–I6  →  O1–O6             │
│ (Filling, Safety, Motion)  │
└────────────────────────────┘
```

---

## ⚙️ **System Specifications**

### 🔹 Input Sensors

| Code | Sensor Type        | Function                  |
| ---- | ------------------ | ------------------------- |
| I1   | Level Sensor       | Detects bottle fill level |
| I2   | Speed Feedback     | Ensures filling precision |
| I3   | Position Sensor    | Nozzle positioning        |
| I4   | Pressure Sensor    | Safety condition          |
| I5   | Proximity Sensor   | Bottle detection          |
| I6   | Temperature Sensor | Safety condition          |

---

### 🔹 Output Actuators

| Code | Actuator       | Function               |
| ---- | -------------- | ---------------------- |
| O1   | Solenoid Valve | Main liquid flow       |
| O2   | Pump Motor     | Liquid supply          |
| O3   | Stepper Motor  | Conveyor movement      |
| O4   | Servo Motor    | Nozzle positioning     |
| O5   | Cleaning Motor | Nozzle cleaning        |
| O6   | Safety Lock    | Alarm & emergency stop |

---

## 🔁 **Finite State Machine (FSM) Design**

* **FSM Type:** Mealy Machine
* **Number of States:** 8 (S0–S7)
* **Flip-Flops Used:** 3 JK Flip-Flops
* **Safety Condition:**
  [
  C = I4 \cdot I6
  ]

### 🧠 Key States

* **S0:** Idle
* **S2:** Positioning
* **S4:** Stable Filling
* **S7:** ALARM (Safety Lock Active)

The Mealy architecture allows **immediate actuator response** (e.g., Safety Lock activation) without waiting for the next clock cycle.

---

## 🧪 **Verification & Simulation**

### 🔹 HDL Simulation

* Implemented using **Icarus Verilog**
* Verified:

  * Correct state transitions
  * Proper actuator activation during filling
  * Immediate alarm response under unsafe conditions

### 🔹 Supervisory C# Simulation

* FSM logic monitored via **C# supervisory application**
* Confirms:

  * State transition correctness
  * Real-time output response
  * Agreement with HDL waveform results

---

## ⚛️ **Quantum Logic Representation**

Critical actuator logic (e.g., **O1 – Solenoid Valve**) is mapped into:

* ✔ Reversible Boolean Logic
* ✔ Quantum Gate Representation (Toffoli, CNOT, Pauli-X)
* ✔ Bra–Ket State Notation

This demonstrates that the FSM design is **compatible with reversible and quantum computation models**.

---

## 📁 **Repository Structure**

```
PAPER-IEEE-ELDIG/
│── Design_icarus_verilog.txt     # FSM HDL design
│── Testbench_icarus_verilog.txt  # HDL testbench
│── CODINGAN_C#_FINAL.txt         # Supervisory C# application
│── main.tex                      # Paper (LaTeX)
│── README.md                     # Project documentation
```

---

## 📊 **Key Results**

* ✔ Deterministic FSM behavior
* ✔ Zero unsafe transitions
* ✔ Mealy-based safety response validated
* ✔ HDL and C# simulations fully consistent
* ✔ Quantum mapping logically valid

---

## 🎓 **Academic Context**

This project was developed as part of an academic research study in **Digital Logic Design, Instrumentation Systems, and Control Architecture**, and is suitable for:

* Industrial automation research
* FSM-based control systems
* Safety-critical system design
* HDL verification studies
* Introductory quantum logic modeling

---

## 📌 **Citation & Reproducibility**

All source code and simulations are provided to ensure **transparency and reproducibility** of the proposed FSM design.

🔗 **GitHub Repository:**
[https://github.com/sintiiaa08-cyber/PAPER-IEEE-ELDIG](https://github.com/sintiiaa08-cyber/PAPER-IEEE-ELDIG)

---

## 🏁 **Project Status**

✔ Completed
✔ Verified
✔ Academically validated
✔ Ready for paper submission and evaluation

---

*For any academic or technical inquiries, please refer to the accompanying paper.*
