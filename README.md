# Hardware-Based Traffic Light Controller 🚦

A purely hardware-driven traffic light sequence controller designed using basic digital logic gates and an asynchronous up-counter. This project was developed without the use of microcontrollers or software programming.

This project was developed for the **Digital Logic Design** course at **Addis Ababa Science and Technology University (AASTU)**.

## 🎯 Project Overview
The objective of this project is to regulate a traffic light sequence using fundamental sequential logic. The system is modeled as a 14-state Finite State Machine (FSM) driven by an asynchronous (ripple) up-counter built from JK flip-flops. 

It simulates realistic traffic light behavior by cycling through specific states, and uses a NAND-gate reset mechanism to automatically loop the system back to state 0 once it reaches state 14 (binary `1110`).

## 🛠️ Tools & Simulation
* **Simulation Software:** Proteus Design Suite
* **Design Type:** Pure Hardware / Sequential Digital Logic

## 🧩 Components Used
* **JK Flip-Flops (7473 IC):** Used to build the 4-bit asynchronous up-counter.
* **Basic Logic Gates:** AND, OR, NOT, NAND gates used to decode the binary states and trigger specific LEDs.
* **BCD to 7-Segment Decoder (74LS47):** Used to visually display the current binary state (0 to 13) in real-time.
* **LED Indicators:** Standard Red, Yellow, and Green LEDs to simulate the traffic pole.
* **Clock Source:** Provides the falling-edge pulses to advance the counter.

## ⏱️ State Breakdown & Timing
The system transitions through 14 distinct states before resetting:

| State Range | Duration | Active Lights | Description |
| :--- | :--- | :--- | :--- |
| **0–3** | 4 seconds | 🔴 **Red** | Vehicles must stop. |
| **4–7** | 3 seconds | 🔴 **Red** + 🟡 **Yellow** | Transition: Prepare to go. |
| **8–11** | 4 seconds | 🟢 **Green** | Vehicles can go. |
| **12–13** | 2 seconds | 🟡 **Yellow** | Transition: Prepare to stop. |
| **14 (1110)** | — | **RESET** | Instantly resets counter to 0. |

## 🚀 How to Run the Simulation
1. Clone this repository to your local machine.
2. Open **Proteus Design Suite**.
3. Open the `.pdsprj` simulation file included in this repository.
4. Click the **Play (Run)** button at the bottom left of the Proteus window.
5. Watch the 7-segment display count upward while the logic gates decode the signals to change the traffic lights!

## 👥 Developer
**Addis Ababa Science and Technology University (AASTU)**  
*College of Engineering | Dept. of Electromechanical Engineering*

* **Desalegn Lulie**
