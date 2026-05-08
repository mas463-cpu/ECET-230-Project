# Project Logbook

## Project Idea
The goal of this project is to design an air mouse that allows a user to control a computer cursor by pointing a handheld device at the screen.

## Initial Planning
- Selected Arduino Leonardo due to USB HID capability
- Selected MPU6050 for motion sensing
- Decided to include physical buttons for user input

## Design Progress
- Created block diagram
- Identified required hardware components
- Planned basic system functionality

- ## Schematic Development

- Created the schematic design in KiCad using the ATmega32U4 microcontroller
- Added the MPU6050 motion sensor for air mouse movement tracking
- Designed USB Micro connections for power and USB communication
- Added push buttons, LEDs, resistors, capacitors, and voltage regulation circuitry
- Configured crystal oscillator connections for stable clock timing
- Verified signal and power connections throughout the schematic
- Corrected wiring issues and updated component connections during development

## PCB Development

- Converted the schematic into a PCB layout using KiCad PCB Editor
- Positioned components to reduce routing congestion and improve organization
- Routed USB D+ and D- traces between the USB connector and microcontroller
- Added vias and multi-layer routing to simplify PCB trace paths
- Implemented a full-board ground plane for grounding and routing efficiency
- Routed 3.3V and UVCC power connections across the board
- Adjusted component placement and traces to reduce air wire crossings
- Finalized PCB routing with all unrouted connections completed
- Generated PCB screenshots and archived final KiCad project files for presentation purposes

## Notes
- Cursor drift may require calibration
- Sensitivity tuning will be needed for smooth movement
