# Air Mouse Project Definition

## Project Overview

The goal of this project is to design and develop a handheld motion-controlled USB air mouse using an MPU6050 motion sensor and an ATmega32U4 microcontroller. The device allows a user to control a computer cursor through wrist movement instead of using a traditional desk mouse.

The project combines embedded systems design, firmware development, schematic creation, PCB layout, USB HID communication, and enclosure planning into a single integrated system.

---

## Original Objectives

- Create a handheld motion-controlled cursor device
- Use gyroscope motion data for cursor movement
- Implement USB HID mouse functionality
- Include left click, right click, and recalibration buttons
- Design a custom schematic and PCB
- Create a compact enclosure concept
- Improve cursor stability through firmware filtering

---

## Hardware Used

### Main Components
- ATmega32U4 microcontroller
- MPU6050 6-axis gyroscope and accelerometer
- Micro-USB connector
- AP2112K-3.3 voltage regulator
- Push buttons
- Status LEDs
- Supporting resistors and capacitors

---

## Software and Firmware Goals

The firmware was designed to:
- Read gyro data through I2C communication
- Convert hand motion into X/Y cursor movement
- Apply calibration and adaptive drift correction
- Add deadzone filtering and smoothing
- Send USB HID mouse reports to the computer
- Handle button input for clicking and recalibration

---

## Design Decisions and Changes

### Wired USB Instead of Wireless
The original concept considered wireless communication, but wired USB was chosen to simplify power management, communication reliability, and debugging.

### Gyroscope-Based Control
The MPU6050 gyroscope was selected because rotational wrist motion maps naturally to cursor movement.

### Custom PCB Development
The project evolved from prototype-style testing into a full custom PCB layout to improve organization, integration, and presentation quality.

### Firmware Filtering Improvements
During development, raw motion data proved unstable. Additional smoothing, deadzone filtering, adaptive bias correction, and calibration logic were added to improve usability.

---

## Current Project Status

Completed:
- Schematic design
- PCB layout
- 3D PCB rendering
- USB HID firmware
- Motion tracking implementation
- Three-button interface
- Calibration system
- Design documentation

Remaining future improvements:
- Physical PCB fabrication
- Enclosure manufacturing
- Additional ergonomic refinement
- Advanced sensor fusion improvements
- Wireless version exploration

---

## Final Definition Summary

The Air Mouse project successfully demonstrates a complete embedded systems design process involving hardware development, firmware engineering, PCB design, and user interaction design. The final system converts wrist motion into usable cursor movement while maintaining stable USB HID communication and user input functionality.
