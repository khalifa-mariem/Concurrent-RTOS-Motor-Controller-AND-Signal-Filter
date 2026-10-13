# Concurrent RTOS Motor Controller & Digital Signal Filter

A multi-threaded **FreeRTOS** application written in C++ designed to manage concurrent sensor data acquisition, digital signal filtering, and PWM motor speed control.

## Tech Stack & Tools
* **Real-Time OS:** FreeRTOS (Tasks, Queues, Mutexes, Semaphores)
* **Programming Language:** C++
* **Modeling & DSP:** MATLAB / Simulink (FIR/IIR filter design)
* **Environment:** VS Code / QEMU Simulator

## Core Tasks Architecture
* **`SensorTask` (High Priority):** Samples simulated sensor streams and applies digital low-pass filtering.
* **`ControlTask` (Medium Priority):** Computes closed-loop PWM motor speed parameters.
* **`TelemetryTask` (Low Priority):** Packages and passes thread-safe data structures using FreeRTOS Queues.

## MATLAB / Simulink Verification
Digital low-pass filtering and signal noise reduction performance were modeled and verified against raw data sets inside Simulink blocks prior to firmware deployment.
