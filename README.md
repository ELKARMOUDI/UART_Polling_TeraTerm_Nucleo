# STM32F411 Nucleo UART Polling / Tera Term 

![STM32F411](https://img.shields.io/badge/STM32F411-Nucleo-blue) 
![UART](https://img.shields.io/badge/USART2-Polling_Mode-green)


![F3770F69-2E8E-4C95-96C4-A38BE586D5B6](https://github.com/user-attachments/assets/6a5dc50a-091e-4e05-9cbc-4efb27df663f)




Basic UART communication in polling mode using STM32F411 Nucleo.

## Features
- **USART2** at 115200 baud
- **Polling Mode** transmission
- **Fixed Message** ("Hello from CubeMX")
- **10ms Transmission** interval
- **HSI Clock** (16MHz)

## Hardware Setup
| Signal | Nucleo Pin | Connection |
|--------|------------|------------|
| USART2_TX | PA2 (D1)  | → USB-TTL RX |
| USART2_RX | PA3 (D0)  | ← USB-TTL TX |
| GND       | GND       | ↔ USB-TTL GND |

*Note: On Nucleo boards, USART2 is connected to ST-Link virtual COM port*

## Technical Details
### UART Configuration 
```c
Baud Rate: 115200 (16MHz clock)
Data Format: 8-bit, No Parity, 1 Stop Bit
Oversampling: 16x
Mode: TX/RX enabled
