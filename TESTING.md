# Air Mouse Testing Document

## Purpose

The purpose of this testing process is to verify that the Air Mouse hardware and firmware operate correctly at the user level. Testing focused on cursor movement, USB HID communication, button input, sensor stability, and calibration behavior.

---

## Hardware Verification

### USB Connection Test
- Connected the Air Mouse to a computer using a Micro-USB cable
- Verified the board powered on correctly
- Confirmed the computer detected the ATmega32U4 as a USB HID device

Result:
- PASS

---

### LED Status Test
- Verified power LED turns on when USB is connected
- Verified status LEDs respond during calibration and sensor operation

Result:
- PASS

---

## Sensor Testing

### MPU6050 Communication Test
- Verified successful I2C communication between the ATmega32U4 and MPU6050
- Confirmed gyro values update continuously during movement

Result:
- PASS

---

### Calibration Test
- Powered the device while stationary
- Verified startup calibration averages sensor offsets correctly
- Confirmed cursor drift decreases after calibration

Result:
- PASS

---

## Cursor Movement Testing

### Motion Tracking Test
- Tilted the device left/right and forward/backward
- Verified cursor movement responds to wrist motion

Result:
- PASS

---

### Deadzone and Smoothing Test
- Tested small unintended hand movements
- Verified deadzone filtering reduced jitter
- Verified smoothing improved cursor stability

Result:
- PASS

---

## Button Testing

### Left Click Test
- Pressed left button repeatedly
- Verified single click events register correctly

Result:
- PASS

---

### Right Click Test
- Pressed right button repeatedly
- Verified right-click functionality works correctly

Result:
- PASS

---

### Recalibration Button Test
- Pressed center recalibration button
- Verified gyro offsets reset properly

Result:
- PASS

---

## Stress and Stability Testing

### Long Runtime Test
- Operated the device continuously for extended use
- Observed minor gyro drift over time
- Adaptive bias correction reduced long-term drift

Result:
- PASS WITH MINOR DRIFT

---

## Final Testing Summary

The Air Mouse successfully completed hardware, firmware, and user-level functionality testing. Cursor movement, button input, USB communication, and calibration systems all operated correctly during testing.
