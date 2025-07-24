# basic-heater-control-system
# 🔥 Basic Heater Control System using Arduino and DS18B20

This project reads temperature using the *DS18B20 digital temperature sensor* and controls a heater system with *three LEDs*:

- 🟢 Green LED – Heater ON (Temp < 25°C)
- 🟡 Yellow LED – Idle Mode (Temp between 25°C and 30°C, blinks)
- 🔴 Red LED – Overheat Warning (Temp > 35°C, blinks)

---

## 📦 Components Used

- Arduino UNO
- DS18B20 Temperature Sensor
- 4.7kΩ Resistor (pull-up for DS18B20)
- 3 x LEDs (Green, Yellow, Red)
- 3 x 220Ω Resistors (for LEDs)
- Breadboard and jumper wires

---

## 🔌 Circuit Connections

### DS18B20 Sensor:
| Pin  | Arduino |
|------|---------|
| VDD  | 5V      |
| GND  | GND     |
| DQ   | D2      |

🔁 Pull-up resistor: 4.7kΩ between DQ and VDD

### LEDs:
| LED         | Arduino Pin | Color   |
|-------------|-------------|---------|
| Heater LED  | D8          | Green   |
| Idle LED    | D9          | Yellow  |
| Overheat LED| D10         | Red     |

All LED cathodes connect to GND through resistors.

---

## 🧠 How It Works

1. DS18B20 reads the current temperature.
2. Based on temperature:
   - Below 25°C → Heater ON (Green LED ON)
   - 25–30°C → Idle mode (Yellow LED blinks)
   - 30–35°C → All OFF (Normal range)
   - Above 35°C → Overheat (Red LED blinks)

---

## 🛠 Simulation

You can simulate this project on [Wokwi](https://wokwi.com/) (online simulator for Arduino).

---

## 📁 Files

- Basic heater control
- README.md – This file

## 🧑‍💻 Author

Made by a beginner learning Arduino and Embedded C! 😊
