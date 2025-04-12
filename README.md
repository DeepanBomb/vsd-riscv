# Smart Light Control System (RISC-V Based)

## Project Overview

This project implements a **Smart Light Control System** using a custom **RV32I RISC-V processor**. The system automatically switches on a light (LED) when **motion is detected** and **ambient light is low** (i.e., it’s dark). It uses a **PIR motion sensor** and **LDR (Light Dependent Resistor)** for sensing, demonstrating basic automation for smart homes or outdoor lighting.

---

## 🔧 Components Required

| Component            | Description                                   |
|---------------------|-----------------------------------------------|
| RV32I Core (Verilog) | Custom 32-bit RISC-V soft-core processor      |
| PIR Sensor           | Detects human movement                        |
| LDR + Resistor       | Senses ambient light levels                   |
| LED                  | Smart light controlled by the processor       |
| UART Module (optional) | Serial log output to PC                    |
| Power Supply         | 5V DC                                         |
| Simulation Tools     | Icarus Verilog, GTKWave                       |

---

## 🔌 Pin Connection Table

| Peripheral       | RISC-V Pin    | Connected Module | Function                          |
|------------------|---------------|------------------|-----------------------------------|
| PIR Sensor       | `gpio[0]`     | Digital OUT      | HIGH when motion is detected      |
| LDR (via comparator) | `gpio[1]` | Digital HIGH/LOW | LOW when it's dark                |
| LED              | `gpio[2]`     | Anode            | ON when both motion & darkness    |
| UART TX (optional)| `uart_tx`    | Host RX (USB)    | Sends system logs                 |
| GND              | -             | All modules      | Ground connection                 |

---

