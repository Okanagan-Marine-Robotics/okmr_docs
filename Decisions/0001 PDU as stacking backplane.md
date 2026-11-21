---
type: decision
status: accepted
date: 2026-11-21
deciders:
  - Electrical
systems:
  - PDU
  - Main PCB
---
# 0001 PDU as stacking backplane

## Context
The 2026–27 sub needs 16 V from the battery hulls distributed and stepped down for the main PCB, actuator board and other loads.

## Decision
The PDU is a stacking backplane PCB that takes 16 V in and holds the step-downs (16→12 V). The main PCB slots into it; regulation lives on the PDU, not on the main PCB.

## Alternatives considered
| Option | Pros | Cons | Why not |
| ------ | ---- | ---- | ------- |
| Regulation on the main PCB | | | TBD |
| Point-to-point harness | | | TBD |

## Consequences
Modularity and easy iteration: boards can be revised and swapped individually. Backplane connector pinout becomes an interface that needs its own page.
