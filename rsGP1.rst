----------------------
Processor Architecture
----------------------
Natalie Garza

ARMv7 architecture:
-------------------
Raspberry pi 2 broadcom bcm2836 soc with a 900 mhz 32-bit quad-core ARM cortex-a7

- Von neumann architecture
- 32-bit core
- Risc architecture (reduced instruction set computer): cannot directly manipulate memory, must do so through loading registers with information from memory
- 37 total registers in the processor. split among seven different processor modes such as running user tasks and run operating system, or general use.
- Thumb: 16-bit instructions labeled thumb, reduced ARM instruction set.
- Application code compiled in thumb is 30% smaller on average than the same code compiled in ARM and normally 30% faster
- The core is successful mainly because of the extremely small but high performance processor - slightly more than 70,000 transistors in all an with extremely low power consumption.
- Three state pipeline(during normal operation while one instruction is being executed its successor is being decoded and a third instruction is being fetched from memory) used, so instructions are executed in three stages:
	+ Fetch: instruction fetched from memory
	+ Decode: decoding of registers used in instruction
	+ Execute: registers read from register bank perform shift and alu operations write registers back to register bank
.. image :: https://homepages.thm.de/~hg10013/Lehre/MMS/WS0304_SS04/Ioannis/Images/e16.gif 
- The program counter points to the instruction being fetched rather than to the instruction being executed. this is important because it means that the program counter value used in an executing instruction is always two instructions ahead of the address.

Figure 10 shows the register bank in the center of
thediagram, plus the required address bus and data
bus.The multiplier, in-line barrel shifter, and ALU are alsoshown.In addition,
the diagram illustrates the in-line decompression process of Thumb instructions while in
the decode stage of the pipeline. This process creates a 32-bit ARM equivalent instruction
from the 16-bit Thumb instruction, decodes the instruction,
and passes it on to theexecute stage.
.. image::https://homepages.thm.de/~hg10013/Lehre/MMS/WS0304_SS04/Ioannis/Images/e10.gif

Armv8 Architecture:
-------------------
Raspberry Pi 3 Broadcom BCM2837 SoC with a 1.2 GHz 64-bit quad-core ARM Cortex-A53

- The ARMv8 architecture introduces 64-bit support to the ARM architecture with a focus on power-efficient implementation while maintaining compatibility with existing 32-bit software.
- Increased availability of larger registers for general purpose and media instructions, a greater addressing range and cryptography instructions enable new categories of applications for superphone and tablet computing
- Two main execution states:
- AArch64 - The 64-bit execution state including exception model, memory model, programmers' model and instruction set support for that state
- AArch32 - The 32-bit execution state including exception model, memory model, programmers' model and instruction set support for that state
- T32 (Thumb) introduced as a 16-bit fixed-length instruction set, subsequently enhanced to a mixed- length 16- and 32-bit instruction set on the introduction of Thumb-2 technology. Part of the 32-bit architecture execution environment now referred to as AArch32.

Resources:
 https://homepages.thm.de/~hg10013/Lehre/MMS/WS0304_SS04/Ioannis/PDF/arm.pdf
 http://www.atmel.com/Images/DDI0029G_7TDMI_R3_trm.pdf
 http://www.arm.com/products/processors/armv8-architecture.php
