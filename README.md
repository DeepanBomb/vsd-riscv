
# Smart Fire Detection System (RISC-V Based)

## Overview

This project implements a **Smart Fire Detection System** using a custom-built **RV32I RISC-V processor core**. It reads inputs from a flame sensor and a temperature sensor, and triggers visual and audio alerts when fire-like conditions are detected. The system also transmits warning messages to a host device via UART.

---

## Components Required

| Component            | Description                             |
|---------------------|-----------------------------------------|
| RV32I Core (Verilog) | 32-bit RISC-V Processor Core            |
| Flame Sensor         | Detects fire or high heat source        |
| DHT11 / LM35         | Reads ambient temperature               |
| Buzzer / LED         | Fire alert actuator                     |
| UART Module          | Sends status messages to PC             |
| Power Supply         | 5V for logic and sensors                |
| Simulation Tools     | Icarus Verilog, GTKWave                |

---

## Pin Connection Table

| Peripheral      | RISC-V Pin    | Module Pin    | Function                   |
|----------------|---------------|---------------|----------------------------|
| Flame Sensor   | `gpio[0]`     | D0            | Detect flame               |
| Temp Sensor    | `gpio[1]`     | Signal        | Read temperature           |
| Buzzer         | `gpio[2]`     | +             | Trigger alert              |
| LED            | `gpio[3]`     | Anode         | Visual warning             |
| UART Tx        | `uart_tx`     | USB Rx        | Send data to PC            |
| GND            | -             | All GND       | Common ground              |

---


