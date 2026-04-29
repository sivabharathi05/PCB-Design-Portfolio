# ESP32-Based Multi-Sensor Environmental Monitoring PCB

## 📌 Project Overview
This project is a custom-designed PCB using KiCad for an ESP32-based environmental monitoring system. The board integrates multiple sensors to measure real-time environmental parameters and display the data.

---

## 🎯 Objective
To design a compact and efficient PCB capable of:
- Interfacing multiple sensors
- Processing both analog and digital signals
- Displaying real-time data
- Serving as a base for IoT applications

---

## ⚙️ Components Used

### 🔹 Microcontroller
- ESP32-WROOM-32

### 🔹 Sensors
- BME280 (Temperature, Humidity, Pressure)
- MQ2 Gas Sensor (Air quality / Smoke detection)
- LDR (Light intensity measurement)

### 🔹 Display
- 0.91" OLED Display (I2C)

### 🔹 Passive Components
- Resistors (Voltage divider + Pull-ups)
- Capacitors (0.1µF, 10µF for decoupling)

---

## 🔌 System Architecture

Sensors → ESP32 → Data Processing → OLED Display

---

## 🔄 Working Principle

1. ESP32 reads sensor data:
   - BME280 via I2C communication
   - MQ2 and LDR via ADC pins
2. Data is processed inside the ESP32
3. Processed values are displayed on the OLED screen
4. The system can be extended for IoT cloud connectivity

---

## 🔗 Communication Protocol

### I2C Bus:
- SDA (Data)
- SCL (Clock)

Used for:
- BME280 Sensor
- OLED Display

Pull-up resistors (4.7kΩ) are used for stable communication.

---

## ⚡ Power Design

- Operates at 3.3V
- Decoupling capacitors:
  - 0.1µF → High-frequency noise filtering
  - 10µF → Voltage stabilization

---

## 🧠 Design Considerations

- Proper I2C routing
- Short signal paths
- Ground plane implementation
- Antenna keep-out area for ESP32
- Separation of analog and digital signals

---

## 🖥️ PCB Details

- 2-layer PCB
- Designed using KiCad
- Includes:
  - Schematic design
  - PCB layout
  - Gerber generation

---

## 📂 Files Included

- Schematic (.kicad_sch)
- PCB Layout (.kicad_pcb)
- Gerber Files (Manufacturing)
- 3D PCB Render Images

---

## 🚀 Future Improvements

- WiFi-based cloud data logging
- Mobile app integration
- Additional sensors integration

---

## 🛠️ Tools Used

- KiCad (EDA Tool)

---

## 💡 Note

This project is part of my self-learning journey in Embedded Systems and PCB Design.

---

## 📬 Contact

Open to feedback and collaboration opportunities in Embedded Systems and PCB Design.
