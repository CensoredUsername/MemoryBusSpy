Project requirements
=====================

- Modify a Pac-Man and a Space Invaders cabinet such that we can keep track of Hi-scores of them on a dedicated monitor.

- Do something interesting

Chosen approach
===============

Develop a generic DIP-40 CPU snooper. This system would be placed inbetween the actual CPU and the CPU socket. From there it could monitor all the memory bus lines, and keep track of all the activity on there.

It would also be able to draw power straight from the CPU power bus.

Design
======

Physical constraints
-------------------

The CPUs we want to monitor are generally on big PCBs on the side of cabinets with nothing above them. However, there will be plenty of chips and other components around the CPU location.

Therefore, the hardware design will have to use the space above the CPU socket. To keep the added length to traces short, this is probably best done using some kind of vertical PCB on which the host CPU as well as the monitoring system are mounted. This PCB would then be mounted 90 degrees rotated on the original host CPU socket.

Processor
---------

The hardware will probably be based on the RP 2350 chip. The PIO subsystems allow monitoring 32 GPIOs per PIO, with real-time guaranteed state machines, at speeds fast enough to easily outpace the CPU that is being monitored.

It is also a dual-core system, meaning that we can use one core to handle the real-time part of the system (managing PIO FIFOs, keeping a copy of the memory state, and guarding for events that we're interested in), while the second core can handle communication with other systems (for instance via wifi).

We could solder the CPU directly, but that involves a lot of extra work. Using a breakout board is probably faster for a low production quantity.

Breakout boards of interest:

- Pi Pico 2 XL
- PICO2-XXL
- RP2350-B-Plus-W development board

Additional hardware requirements
--------------------------------

THe RP2350 pins only accept voltages between 0 and 3.3V. However, the CPUs we want to monitor do not share a consistent pinout, and they use voltages between -5V and +12V. We want to be independent of pinout, i.e, just connect 40 GPIOs to each pin on the socket and then select the ones that we want to monitor in software.

Therefore we'll need 40x some kind of protection/clamping circuit that ensures that only voltages between 0 and 3.3V go into the RP2350. Any lower/higher voltages will have to be clamped to this range, and preferably this circuitry should draw as little current on the bus lines as possible, to prevent any problems for the host system.

Software
--------

Rust, probably. Embassy on the RP2350 is pretty nice.
