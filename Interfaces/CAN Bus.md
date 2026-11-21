---
type: interface
status: draft
owner:
bus: CAN
endpoints:
  - Main PCB (STM32)
  - Actuator board (STM32)
  - BMS boards
updated: 2026-11-21
---
# CAN Bus

> Main PCB ↔ actuator board and BMS boards, daisy-chained. The in-sub BMS PCB exists partly to keep the chain simple.

## Physical layer
| Parameter          | Value |
| ------------------ | ----- |
| Standard           | TBD (CAN 2.0B / FD) |
| Bitrate            | TBD   |
| Transceiver        | TBD   |
| Connector & pinout | TBD   |
| Termination        | TBD (which two nodes carry the 120 Ω) |

## Node IDs
| Node | ID range | Board page |
| ---- | -------- | ---------- |
| Main PCB | | [Main PCB](../Systems/Main%20PCB/Main%20PCB.md) |
| Actuator board | | [Actuator Board](../Systems/Actuator%20Board/Actuator%20Board.md) |
| BMS hull A | | [BMS](../Systems/BMS/BMS.md) |
| BMS hull B | | [BMS](../Systems/BMS/BMS.md) |
| In-sub BMS | | [BMS](../Systems/BMS/BMS.md) |

## Messages
| ID | Name | Sender | Payload (type, units, scaling) | Rate | Notes |
| -- | ---- | ------ | ------------------------------ | ---- | ----- |
|    | BMS voltage/current telemetry | BMS | | | |
|    | Actuator command | Main PCB | | | arm, dropper, torpedoes |

## Timeouts & failure behaviour
TBD

## Change log
| Version | Date | Change | Breaking? |
| ------- | ---- | ------ | --------- |
| 0.1 | 2026-11-21 | Page created | — |
