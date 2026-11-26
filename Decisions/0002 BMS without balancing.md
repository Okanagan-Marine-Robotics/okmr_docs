---
type: decision
status: accepted
date: 2026-11-21
deciders:
  - Electrical
systems:
  - BMS
---
# 0002 BMS without balancing

## Context
Battery is four 2S LiPo packs wired as two 4S strings (2S+2S in series) in parallel. Packs are charged and balanced outside the sub on an external charger/balancer.

## Decision
The BMS board does no balancing. It provides hardware-level overcurrent and overvoltage protection, plus voltage/current telemetry to an MCU that reports over CAN to the main MCU.

## Alternatives considered
| Option | Pros | Cons | Why not |
| ------ | ---- | ---- | ------- |
| On-board passive balancing | | | TBD |

## Consequences
Balancing depends on the charging procedure, so it needs to be in the battery handling checklist. Revisit if packs drift between charges.
