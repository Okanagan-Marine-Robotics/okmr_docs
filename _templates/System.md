---
type: system
status: concept
owner:
subteams:
  - electrical
rev:
altium:
firmware:
updated: {{date}}
---
# {{title}}

> One line: what this does on the sub and why it exists.

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
