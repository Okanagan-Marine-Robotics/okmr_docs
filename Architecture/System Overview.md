---
type: overview
owner:
updated: 2026-11-21
---
# System Overview (2026–27)

How the major boards and computers on Ogopogo connect. Each block has its own page under `Systems/`; each arrow should have a page under `Interfaces/`.

```mermaid
flowchart LR
  subgraph Power
    BATT["Battery hulls<br/>4× 2S LiPo as 2× 4S strings in parallel"]
    PDU["PDU stacking backplane<br/>16 V in, 16→12 V step-down"]
    BMS["BMS ×2 (one per hull)<br/>+ in-sub BMS board"]
  end
  subgraph Compute
    CAM["USB camera"]
    JET["Jetson Orin Nano"]
  end
  MAIN["Main PCB<br/>STM32 · IMU/mag/gyro · killswitch"]
  ACT["Actuator board (STM32)<br/>arm · dropper · torpedoes"]
  THR["Thrusters"]
  subgraph Acoustics
    HYD["4× Aquarian AS-1 hydrophones"]
    AFE["Analog front end<br/>amplify + filter"]
    FPGA["Zynq FPGA<br/>localization"]
  end
  BATT -->|16 V| PDU
  PDU ---|backplane slot| MAIN
  PDU -->|12 V| ACT
  CAM -->|USB| JET
  JET -->|UART: motor commands| MAIN
  MAIN -->|PWM| THR
  MAIN <-->|CAN| ACT
  MAIN <-->|CAN| BMS
  HYD --> AFE --> FPGA
  FPGA -->|Ethernet| JET
```

Not placed on the diagram yet: acoustic modem (main sub ↔ minisub), magnetic task, leak sensor.

## Interfaces
| Link | Bus | Spec |
| ---- | --- | ---- |
| Jetson → Main PCB | UART | [MCU-to-Jetson UART](../Interfaces/MCU-to-Jetson%20UART.md) |
| Main PCB ↔ Actuator board, BMS | CAN | [CAN Bus](../Interfaces/CAN%20Bus.md) |
| Zynq → Jetson | Ethernet | TBD |
| Main PCB → Thrusters | PWM | TBD |
| PDU backplane | Power + signals | TBD |

## Systems
See [Index](../Index.md) or the `Systems` view in `Tracker.base`.
