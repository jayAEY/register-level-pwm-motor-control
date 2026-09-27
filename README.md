# ⚙️ Register Level PWM Motor Controller

A **software-based PWM DC motor speed controller** using an Arduino, a 2N2222 transistor, and three bitmasked push buttons to adjust the motor’s duty cycle (80%, 50%, 20%) through port registers.

---

## 🚀 Features

* **3 Speed Presets:** Instantly shifts between three duty cycle profiles via hardware inputs.
* **Direct Register I/O:** Uses direct PORT register manipulation instead of standard Arduino functions for faster execution.
* **Software PWM Control:** Generates the raw pulse-width modulation timing signal using tight delay loops.
* **Hardware Safety Built-In:** Configured with external pull-up resistors to prevent floating inputs on the pushbutton gates.

---

⚙️ Operating Modes

| Input Component | Target Speed | Duty Cycle | Output Behavior |
| :--- | :--- | :---: | :--- |
| **Button 3** | High Speed | 80% | Drives fast motor rotation |
| **Button 2** | Medium Speed | 50% | Drives medium motor rotation |
| **Button 1** | Low Speed | 20% | Drives slow motor rotation |

---
## 🔬 Testing

### 💻 Simulation & Schematics

* Built and verified the complete electrical circuit layout using the Tinkercad online simulation workspace.
* Checked the hardware paths using the schematic below to ensure proper transistor biasing and driver grounding.

![Project Preview](./img/arduino-dc-motor-siumulation.gif)
[![Tinkercad Design](https://img.shields.io/badge/Tinkercad-View%20Design-brightgreen?style=for-the-badge&logo=tinkercad)](https://www.tinkercad.com/things/hM7xuqlaAPW-arduino-dc-motor-controller?sharecode=fTR0VJ1MF7x52sB05V9uynOJFpLAZXVYweU7w-ntLRI)

![schematic](./img/arduino_dc_motor_controller1-schematic.jpg)

---

### 📍 Arduino Pin Mappings

| Port Pin | Arduino Hardware Pin | Description |
| :--- | :--- | :--- |
| **`PC0`** | Pushbutton 1 (Analog A0) | Selects 20% Low Speed |
| **`PC1`** | Pushbutton 2 (Analog A1) | Selects 50% Medium Speed |
| **`PC2`** | Pushbutton 3 (Analog A2) | Selects 80% High Speed |
| **`PD0`** | DC Motor Output (Digital D0) | PWM Transistor Base Drive |
