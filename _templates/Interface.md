---
type: interface
status: draft
owner:
bus:
endpoints:
  - 
  - 
updated: {{date}}
---
# {{title}}

> Side A ↔ Side B, what flows over it, who initiates.

## Physical layer
| Parameter          | Value |
| ------------------ | ----- |
| Bus                |       |
| Baud / bitrate     |       |
| Logic level        |       |
| Connector & pinout |       |
| Termination        |       |

## Framing
Byte layout of a frame: start byte, length, ID, payload, checksum (CRC type), endianness.

## Messages
| ID | Name | Direction | Payload (type, units, scaling) | Rate | Notes |
| -- | ---- | --------- | ------------------------------ | ---- | ----- |
|    |      |           |                                |      |       |

## Timeouts & failure behaviour
What each side does when the link drops, e.g. motors to neutral after N ms with no command.

## Implementation
- Side A code: 
- Side B code: 

## Change log
| Version | Date | Change | Breaking? |
| ------- | ---- | ------ | --------- |
|         |      |        |           |
