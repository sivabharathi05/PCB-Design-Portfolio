PROJECT TITLE:
ESP32-Based I2C Sensor Interface PCB

PURPOSE:
This project was developed as part of my PCB design learning to understand real-world hardware design practices such as signal routing, grounding, and RF-aware layout using KiCad.

SYSTEM OVERVIEW:
The board is designed to interface I2C-based sensors with an ESP32 module. Communication is established using the I2C protocol (SDA and SCL lines), with appropriate pull-up resistors to ensure reliable digital communication.

The system operates at 3.3V and is intended for low-power embedded applications such as sensor data acquisition and IoT prototyping.


PCB DESIGN DETAILS:

1. LAYER STACKUP:

* 2-layer PCB
* Top layer (F.Cu): Signal routing and component placement
* Bottom layer (B.Cu): Continuous ground plane

Rationale:
A 2-layer stackup was selected as the design involves low-speed digital signals (I2C) and low current, making it sufficient and cost-effective.


2. TRACK WIDTH SELECTION:

* Signal traces: 0.25 mm – 0.4 mm
* Power traces (3.3V, GND): Wider traces used

Rationale:
Track widths were chosen based on low current requirements (<100 mA), ensuring manufacturability and minimizing resistive losses.


3. GROUNDING STRATEGY:

* Full GND copper pour on bottom layer
* Additional GND fill on top layer
* Multiple stitching vias used

Rationale:
This ensures a continuous return path, reduces noise, and improves signal integrity.


4. RF CONSIDERATION (ESP32 ANTENNA):

* A strict keep-out region is maintained under the ESP32 antenna
* No copper, vias, or routing in this region

Rationale:
Prevents RF signal degradation and ensures proper wireless performance.


5. I2C SIGNAL DESIGN:

* SDA and SCL lines routed with minimal length
* Pull-up resistors used for stable logic levels

Rationale:
Ensures reliable communication and avoids signal distortion.


6. COMPONENT PLACEMENT:

* ESP32 centrally placed
* Decoupling capacitors placed close to power pins
* Connectors placed for easy access

Rationale:
Improves signal flow and reduces noise coupling.


7. DESIGN VALIDATION:

* ERC and DRC checks completed
* Gerber files generated and verified using viewer tools


TOOLS USED:

* KiCad for schematic and PCB layout
* Gerber Viewer for verification


LEARNING OUTCOME:
This project helped in understanding:

* PCB stackup selection
* Track width vs current considerations
* Ground plane implementation
* RF design constraints (antenna keep-out)
* End-to-end PCB workflow (design to fabrication)


NOTE:
This is a learning-focused project aimed at developing practical PCB design skills. The design is intended for low-power applications and not optimized for high-current or high-speed systems.