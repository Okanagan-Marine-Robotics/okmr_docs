# OKMR Docs

Start here. Everything is organized by system, not by subteam: each system page covers its electrical, software and mechanical sides.

## Big picture
- [System Overview](Architecture/System%20Overview.md): block diagram of the 2026–27 sub
- `Tracker.base`: live tables of every system, interface, decision and test report (open it in Obsidian)

## Systems
- [Main PCB](Systems/Main%20PCB/Main%20PCB.md)
- [PDU](Systems/PDU/PDU.md)
- [BMS](Systems/BMS/BMS.md)
- [Actuator Board](Systems/Actuator%20Board/Actuator%20Board.md)
- [Killswitch](Systems/Killswitch/Killswitch.md)
- [Acoustics](Systems/Acoustics/Acoustics.md)
- [Magnetic Task](Systems/Magnetic%20Task/Magnetic%20Task.md)
- [Leak Sensor](Systems/Leak%20Sensor/Leak%20Sensor.md)

## Interfaces
- [MCU-to-Jetson UART](Interfaces/MCU-to-Jetson%20UART.md)
- [CAN Bus](Interfaces/CAN%20Bus.md)

## Decisions
- [0001 PDU as stacking backplane](Decisions/0001%20PDU%20as%20stacking%20backplane.md)
- [0002 BMS without balancing](Decisions/0002%20BMS%20without%20balancing.md)
- [0003 Zynq to Jetson over Ethernet](Decisions/0003%20Zynq%20to%20Jetson%20over%20Ethernet.md)

## Testing
- [Pool Test](Test%20Plans/Pool%20Test/Pool%20Test.md)
- [Sim Test](Test%20Plans/Sim%20Test/Sim%20Test.md)

## Contributing
Read [CONTRIBUTING](CONTRIBUTING.md) before your first PR.
