---
type: decision
status: accepted
date: 2026-11-21
deciders:
  - Acoustics
systems:
  - Acoustics
---
# 0003 Zynq to Jetson over Ethernet

## Context
The 4-hydrophone array is processed on a Zynq FPGA. Localization results need to reach the Jetson.

## Decision
The Zynq sends results to the Jetson over Ethernet.

## Alternatives considered
| Option | Pros | Cons | Why not |
| ------ | ---- | ---- | ------- |
| UART | | | TBD |
| Via main PCB over CAN | | | TBD |

## Consequences
Needs an Ethernet interface page (addressing, protocol, message format) and an Ethernet port budget on the Jetson.
