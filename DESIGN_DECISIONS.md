# Design Decision Document

# Project Overview

The goal of this project was to create a motion-controlled USB air mouse using an MPU-6050 IMU sensor and an ATmega32U4 microcontroller. The device converts wrist motion into computer cursor movement while supporting left click, right click, and recalibration through physical buttons.

The project combines:
- Embedded firmware
- USB HID communication
- Custom PCB design
- KiCad schematic capture
- PCB layout
- Motion filtering
- Product enclosure visualization

---

# Major Design Decisions

## Decision 1 — Wired USB Instead of Wireless

### Objective
Create a reliable motion-controlled mouse while keeping development complexity manageable.

### Options Considered
- Wireless Bluetooth communication
- Wired USB communication

### Final Choice
Wired USB communication using a Micro-USB connection.

### Reasoning
Wireless communication would require:
- Battery charging circuitry
- Power management
- Bluetooth pairing
- Additional firmware complexity
- Increased debugging time

Using wired USB allowed the project to focus on reliable cursor control and USB HID functionality without introducing wireless communication challenges.

### Result
The wired USB design simplified development and improved reliability.

---

# Decision 2 — ATmega32U4 Microcontroller

### Objective
Select a microcontroller capable of acting as a USB mouse device.

### Options Considered
- ATmega328P
- ESP32
- ATmega32U4

### Final Choice
ATmega32U4

### Reasoning
The ATmega32U4 supports native USB HID communication. This allows the controller to appear directly as a standard USB mouse without requiring an additional USB interface chip.

The Arduino Mouse library also supports the 32U4 platform directly.

### Result
The microcontroller successfully handled:
- USB HID communication
- MPU6050 sensor reading
- Motion filtering
- Button handling

---

# Decision 3 — MPU-6050 IMU Sensor

### Objective
Select a motion sensor capable of tracking wrist movement.

### Options Considered
- Accelerometer-only sensors
- Gyroscope-only sensors
- Combined IMU sensors

### Final Choice
MPU-6050 IMU sensor

### Reasoning
The MPU-6050 combines:
- Gyroscope
- Accelerometer

into one compact device.

The gyroscope data was especially useful because rotational wrist movement maps naturally into cursor movement.

The sensor also communicates using I2C, simplifying wiring and PCB routing.

### Result
The MPU-6050 successfully provided motion data for cursor control.

---

# Decision 4 — Three Front Buttons

### Objective
Provide intuitive mouse interaction controls.

### Options Considered
- Two-button design
- Three-button design
- Touch controls

### Final Choice
Three tactile front-mounted buttons.

### Reasoning
The final layout included:
- Left click
- Right click
- Recalibration button

The recalibration button allows the user to quickly reset motion offsets during operation.

Front-mounted buttons also align naturally with handheld usage.

### Result
The interface remained simple and practical while improving usability.

---

# Decision 5 — Custom PCB Instead of Prototype Board

### Objective
Create a cleaner and more integrated hardware solution.

### Options Considered
- Breadboard prototype
- Development board wiring
- Custom PCB

### Final Choice
Custom KiCad PCB design.

### Reasoning
Prototype boards were useful during early testing, but the final goal was a compact integrated design.

The PCB combines:
- Controller
- IMU sensor
- Voltage regulation
- USB interface
- LEDs
- Buttons

onto one board.

### Result
The PCB improved organization, compactness, and overall presentation quality.

---

# Decision 6 — Motion Filtering and Cursor Stabilization

### Objective
Make cursor movement stable and usable.

### Problems Identified
Raw gyro data caused:
- Cursor drift
- Jitter
- Unstable movement

### Solutions Added
- Startup calibration
- Adaptive bias correction
- Deadzone filtering
- Motion smoothing
- Cursor scaling

### Reasoning
Without filtering, the cursor movement felt unstable and difficult to control.

The firmware processing became one of the most important parts of the project.

### Result
Cursor movement became significantly smoother and more controllable.

---

# Decision 7 — PCB Layout Strategy

### Objective
Create an organized and compact PCB layout.

### Layout Decisions
- Three buttons grouped at the front edge
- ATmega32U4 near board center
- Micro-USB connector at bottom edge
- MPU6050 placed close to controller
- Ground plane added for routing efficiency

### Reasoning
The layout was designed to:
- Reduce routing congestion
- Improve signal organization
- Match the enclosure concept
- Keep wiring compact

### Result
The PCB routing completed successfully with all major subsystems integrated.

---

# Decision 8 — Enclosure Visualization

### Objective
Present the project as a complete product concept.

### Final Choice
Create a rendered enclosure concept instead of a fabricated shell.

### Reasoning
The enclosure render communicates:
- Intended form factor
- Button placement
- Cable opening location
- Ergonomic direction

while avoiding fabrication delays.

### Result
The enclosure concept improved the professional presentation of the project.

---

# Final Engineering Outcome

The final project combines:
- Motion sensing
- USB HID communication
- Embedded firmware
- PCB design
- Mechanical visualization

into a complete engineering prototype for a wired USB air mouse.

The most important lesson learned during development was that stable cursor movement depends heavily on firmware filtering, calibration, and signal processing rather than raw sensor data alone.
