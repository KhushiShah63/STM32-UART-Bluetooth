# STM32 UART Bluetooth Communication

An STM32-based project demonstrating UART communication between an STM32 microcontroller and an HC-05 Bluetooth module using STM32 HAL and Embedded C.

---

## 📌 Project Overview

This project demonstrates wireless serial communication between the STM32 NUCLEO-F401RE and an HC-05 Bluetooth module.

The STM32 communicates with the HC-05 through the UART peripheral. Data received through Bluetooth is processed by the STM32 and transmitted back through UART.

---

## 🔧 Hardware Used

- STM32 NUCLEO-F401RE
- HC-05 Bluetooth Module
- USB Cable
- Jumper Wires
- Breadboard

---

## ⚙️ Software & Tools

- STM32CubeIDE
- STM32CubeMX
- Embedded C
- STM32 HAL Library
- UART Communication

---

## 🔌 Circuit Diagram

Add the circuit diagram here.

![STM32 UART Bluetooth Circuit Diagram](circuit-diagram.png)

---

## 🔌 Pin Connections

| HC-05 | STM32 |
|---|---|
| VCC | 5V |
| GND | GND |
| TX | UART RX |
| RX | UART TX |

> TX and RX are cross-connected: HC-05 TX → STM32 RX and HC-05 RX → STM32 TX.

---
##  Circuit Diagram 
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/a9b3fa47-de65-42b5-be04-e3a465f33e2d" />
---
## 🔄 Working Principle

```text
        Bluetooth
            │
            ▼
       ┌─────────┐
       │  HC-05  │
       └────┬────┘
            │ UART
            ▼
    ┌─────────────────┐
    │      STM32      │
    │  NUCLEO-F401RE  │
    └─────────────────┘
            │
            ▼
       UART Processing

---

⚙️ STM32 Configuration

The project was configured using STM32CubeMX and STM32CubeIDE.

Microcontroller: STM32F401RET6
Communication: UART
Firmware: STM32 HAL
Programming Language: Embedded C

The complete peripheral configuration is available in the .ioc file.

---

💻 Code Structure
File	Purpose
main.c	Main application and UART communication
.ioc	STM32CubeMX configuration
README.md	Project documentation

---

🚀 How to Use
Open the project in STM32CubeIDE.
Open the .ioc file.
Verify the UART configuration.
Connect the HC-05 to the STM32.
Build the project.
Flash the firmware using ST-LINK.
Pair the HC-05 with a Bluetooth-enabled device.
Send data through Bluetooth and observe the STM32 UART response.
