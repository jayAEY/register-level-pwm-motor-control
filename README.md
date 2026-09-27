# ⚙️ Register Level PWM Motor Controller

[![Tinkercad Design](https://img.shields.io/badge/Tinkercad-View%20Design-brightgreen?style=for-the-badge&logo=tinkercad)](https://www.tinkercad.com/things/hM7xuqlaAPW-arduino-dc-motor-controller?sharecode=fTR0VJ1MF7x52sB05V9uynOJFpLAZXVYweU7w-ntLRI)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

A **software-based PWM DC motor speed controller** using an Arduino, a 2N2222 transistor, and three bitmasked push buttons to adjust the motor’s duty cycle (80%, 50%, 20%) through port registers.

---
### 🖼️ Project Preview

![Project Preview](./img/arduino-dc-motor-siumulation.gif)

---

### Features
- 3 speed levels using push buttons (1 at bottom):
- **Button 3** → 🚀 **80% Duty Cycle**
- **Button 2** → ⚡ **50% Duty Cycle**
- **Button 1** → 🐢 **20% Duty Cycle**
- Pure software PWM using `delay()`
- Uses **PORT registers** for fast I/O

---

### Pinouts
| Component         | Arduino Pin |
|-------------------|-------------|
| Push Button 1     | PC0 (A0)    |
| Push Button 2     | PC1 (A1)    |
| Push Button 3     | PC2 (A2)    |
| DC Motor          | PD0 (D0)    |

> 💡 **Hardware Note:** Always use **10kΩ pull-up resistors** on the push buttons or enable internal pull-ups.

![schematic](./img/arduino_dc_motor_controller1-schematic.jpg)

---
