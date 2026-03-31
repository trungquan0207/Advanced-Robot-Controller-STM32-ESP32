# Advanced-Robot-Controller-STM32-ESP32
📌 Project Overview
This repository contains the design and implementation of a high-performance Robot Control Board. The system leverages the computational power of the STM32F407VET6 for real-time motion control and the ESP32-S3 for wireless communication. It is specifically designed for mobile robots requiring high-torque motor driving, real-time data visualization, and PID-based precision.
🚀 Key Features
- Dual-Processor Architecture: STM32F407VET6 (ARM Cortex-M4): Handles core logic, high-speed PWM generation, and PID computation. ESP32-S3-WROOM-1-N4: Manages Wi-Fi/Bluetooth connectivity and acts as a gateway for wireless data transmission via UART.
- High-Power Motor Driving: Integrated interface for BTS7960 (43A Double DC Stepper Motor Driver) to handle heavy-duty motors.
- Closed-Loop Control: Implementation of PID (Proportional-Integral-Derivative) algorithms for precise speed and position control.
- Real-time Feedback: LCD Kit integration for displaying system parameters, battery levels, and sensor data.
- Industrial Communication: Reliable UART bridge between the two MCUs for seamless data telemetry.
🛠 Hardware Components
Component                             Function
MCU 1: STM32F407VET6      Main Controller (PID, PWM, Encoder processing)
MCU 2: ESP32-S3           Wireless Communication (Wi-Fi/BLE)
Driver: BTS7960           High-current H-Bridge for DC Motors
Display: LCD Module       User Interface & Debugging Display
Power Stage               Integrated 12V/5V/3.3V rails (from the previous Power Module design)
⚙️ Control Theory: PID AlgorithmThe system utilizes a PID controller to minimize the error between the desired setpoint and the actual motor feedback (Encoder).
Proportional (P): Fast response to current error.
Integral (I): Eliminates steady-state error.
Derivative (D): Dampens oscillations and improves stability.
