# ECET-230 Air Mouse Project

This project is a custom motion-controlled USB air mouse that uses an MPU-6050 IMU sensor and an ATmega32U4 microcontroller to convert wrist motion into real-time computer cursor movement. The system combines embedded firmware, USB HID communication, custom PCB design, KiCad schematic capture, and enclosure visualization into a complete engineering project.

## Overview
- Arduino Leonardo with USB HID support
- Gyroscope for motion and orientation sensing
- Buttons for click, scroll, and reset
- USB connection to PC

The Arduino reads gyroscope data, processes it, and sends mouse commands to the computer.

## Development Process

- Created schematic in KiCad
- Designed PCB layout and routed traces
- Added MPU6050 motion sensor support
- Implemented USB HID communication
- Added ground plane and multi-layer routing
- Tested routing and component placement

## Future Improvements

- Improve cursor smoothing and motion filtering
- Add rechargeable battery support
- Reduce PCB size for a more compact handheld design
- Add wireless Bluetooth functionality
- Improve button placement and ergonomics

## Hardware Components

- ATmega32U4 microcontroller
- MPU-6050 gyroscope + accelerometer
- AP2112K-3.3 voltage regulator
- Micro-USB connector
- Three tactile switches
- Status and power LEDs
- USB HID interface support
- Custom KiCad PCB layout

## Firmware Features

- Startup gyro calibration
- Adaptive drift correction
- Cursor deadzone filtering
- Motion smoothing
- USB HID mouse reporting
- Recalibration button support
- Cursor scaling and axis mapping
- Three-button mouse control

## Challenges Encountered

- Cursor drift caused by gyro bias
- Jitter from raw sensor noise
- I2C communication stability
- Button debounce handling
- Cursor smoothing refinement
- USB HID tuning and scaling
- PCB routing and component placement

## Final Status

Current project status:

- Custom PCB completed
- KiCad schematic completed
- PCB layout completed
- Firmware logic completed
- USB HID functionality implemented
- Motion-to-cursor pipeline implemented
- 3D PCB render completed
- Enclosure concept completed
- BOM and fabrication files generated
