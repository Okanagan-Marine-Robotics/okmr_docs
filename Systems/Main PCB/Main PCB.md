---
type: system
status: concept
owner:
subteams:
  - electrical
  - software
rev:
altium:
firmware:
updated: 2026-11-21
---
# Main PCB

> Main STM32 board: takes UART motor commands from the Jetson and outputs PWM to the thrusters. Carries a dedicated IMU/magnetometer/gyro, CAN/I2C/SPI/UART, and the killswitch. Slots into the PDU.

## Overview

## Interfaces
| Connector | Signal / bus | Connects to | Notes |
| --------- | ------------ | ----------- | ----- |
|           |              |             |       |

Link the full spec in the `Interfaces/` page for each bus rather than repeating it here.

## Electrical
- Schematic PDF (latest released rev): 
- Altium 365 project: 
- Power in / rails / expected current: 

## Firmware
- Repo / path: 
- MCU / toolchain: 

## Mechanical
- Hull / mounting location: 
- Connectors / penetrators: 

## Bring-up checklist
- [ ] Visual inspection, continuity check for rail-to-GND shorts
- [ ] First power-up on a current-limited supply, record idle current
- [ ] Check every rail voltage under load
- [ ] Programming / debug interface works (SWD, UART bootloader)
- [ ] Each peripheral / bus tested, results in a test report

## Known issues / errata
> [!warning] Rev X
> Problem, symptom, workaround, fixed in rev?

## Revision history
| Rev | Date | Changes |
| --- | ---- | ------- |
|     |      |         |

## Related
- Decisions: 
- Test reports: 
