---
type: interface
status: draft
owner:
bus: UART
endpoints:
  - Jetson Orin Nano
  - Main PCB (STM32)
updated: 2026-11-21
---
# MCU-to-Jetson UART

> Jetson Orin Nano → main PCB STM32. Carries motor commands; the STM32 turns them into PWM for the thrusters. Software + electrical both own this page.

## Physical layer
| Parameter          | Value |
| ------------------ | ----- |
| Bus                | UART  |
| Baud               | TBD   |
| Logic level        | TBD (check Jetson header voltage vs STM32 pins) |
| Connector & pinout | TBD   |
| Flow control       | TBD   |

## Framing
TBD: start byte, length, message ID, payload, CRC, endianness.

## Messages
| ID | Name | Direction | Payload (type, units, scaling) | Rate | Notes |
| -- | ---- | --------- | ------------------------------ | ---- | ----- |
|    | Motor command | Jetson → MCU | | | |
|    | Telemetry / IMU | MCU → Jetson | | | Confirm if this goes over this link |
|    | Killswitch state | MCU → Jetson | | | Confirm if this goes over this link |

## Timeouts & failure behaviour
TBD: what the STM32 does with thrusters when commands stop arriving.

## Implementation
- Jetson side: 
- STM32 side: 

## Change log
| Version | Date | Change | Breaking? |
| ------- | ---- | ------ | --------- |
| 0.1 | 2026-11-21 | Page created from placeholder | — |
