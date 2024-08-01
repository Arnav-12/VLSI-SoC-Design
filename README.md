# Sky130 Day-1
## Introduction to QFN-48 Package,chips,pads,die, and core

The QFN-48 (Quad Flat No-lead, 48 pins) package is a compact, surface-mount integrated circuit package widely used in modern electronic devices due to its low-profile design and efficient heat dissipation. Measuring typically around 7mm x 7mm with a height of about 0.9mm, the QFN-48 package is designed to save space on printed circuit boards (PCBs). Unlike traditional leaded packages, the QFN-48 does not have leads extending from its sides, which helps to minimize its footprint and improve electrical performance.

![S1](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/Screenshots%20vsd/S1.png)

The pads on a QFN-48 package play a crucial role in establishing electrical connections between the chip and the PCB. These pads are located on the bottom of the package and are usually made of copper, plated with a thin layer of tin or gold to ensure reliable soldering. The pads are divided into peripheral pads, which are arranged around the perimeter for signal and power connections, and a larger thermal pad in the center. The thermal pad is primarily used for heat dissipation and often also serves as an electrical ground. This design helps manage heat more effectively, which is critical for maintaining the performance and longevity of the chip.

![S2](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/Screenshots%20vsd/S2.png)
At the heart of the QFN-48 package lies the core, the central part of the semiconductor die where the main circuitry is located. The core contains active and passive components, including transistors, resistors, capacitors, and interconnects, which collectively perform the chip's intended functions. The core's design is crucial for the chip's performance, as it dictates how efficiently the chip processes signals and performs computations.

The die, a small piece of silicon wafer, contains the integrated circuit and is the fundamental building block of the chip. The die is fabricated through processes like photolithography and etching to create the intricate circuits necessary for the chip's functionality. Once the die is completed, it is mounted onto the lead frame or substrate within the QFN-48 package. Connections between the die and the pads are made using bond wires or advanced methods like flip-chip bonding, ensuring reliable electrical pathways for signal transmission.

Intellectual Properties (IPs) are essential components of modern chip design, providing pre-designed and pre-verified blocks of logic or functions that can be integrated into the chip. IPs come in various forms, such as hard IPs, which are fixed layouts integrated directly into the silicon, and soft IPs, which are synthesizable RTL (Register Transfer Level) code that can be customized. Examples of IPs include processors, memory controllers, interfaces like USB and Ethernet, analog components like ADCs and DACs, and various other functional blocks. By incorporating IPs, designers can speed up the development process, reduce costs, and ensure the reliability of the chip by reusing proven components.

## Introduction to RISC-V

RISC-V (Reduced Instruction Set Computing, Version 5) is an open, free, and extensible instruction set architecture (ISA) that is rapidly gaining popularity in the field of computer architecture. Developed at the University of California, Berkeley, RISC-V aims to provide a standardized and streamlined ISA that can be used for a wide range of applications, from small embedded systems to large-scale data centers. Its open nature means that anyone can use, modify, and extend the ISA without licensing fees, fostering innovation and collaboration across the industry.
![S3](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/S3.png)

## From Software Application to Hardware
Here we get to know ,how software and hardware interacts
![S4](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/S4.png)

## Digital ASIC Design

The journey from Electronic Design Automation (EDA) tools to an Application-Specific Integrated Circuit (ASIC) involves several key stages. EDA tools, such as schematic capture software, are used to create detailed circuit diagrams, while simulation tools like SPICE for analog and ModelSim for digital designs verify the functionality of these circuits. Synthesis tools, such as Synopsys Design Compiler, then convert high-level RTL (Register Transfer Level) code into a gate-level netlist. Following this, Place and Route (P&R) tools, like Cadence Innovus or Synopsys IC Compiler, are used to physically layout the circuit on the chip, ensuring optimal performance and area efficiency.

![S5](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/S5.png)

## Simplified RTL2GDS flow

The RTL2GDS flow, transforming a high-level Register Transfer Level (RTL) design into a final GDSII (Graphic Data System II) format, is streamlined through several stages. Initially, RTL code written in hardware description languages like Verilog or VHDL is synthesized into a gate-level netlist using synthesis tools. This netlist, representing the logical structure of the circuit, undergoes Design-for-Test (DFT) enhancements to facilitate post-production testing. The design is then processed through Place and Route (P&R) tools, arranging the netlist components and routing interconnections on the silicon. Subsequent stages involve timing analysis, signal integrity checks, and power optimization to ensure the design meets all performance criteria. Finally, the completed layout is verified against the original design specifications before being exported in the GDSII format, ready for fabrication.

![S6](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/S6.png)

## Strive Chipsets
![S7](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/S7.png)

## OpenLANE Design Flow
![S8](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/S8.png)

## Day-1 Labs
![S8.1](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/S8.1.png)
![S9](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/S9.png)
![S10](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/S10.png)
![S11](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/S11.png)
![S12](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/S12.png)
![S13](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/S13.png)

# Sky130 Day-2
## Utilization Factor and width,height core of the die

### Utilization Factor

The utilization factor in chip design refers to the percentage of the core area of a die that is occupied by standard cells, macros, and other functional elements. It is a critical parameter in the physical design process, particularly during the place and route stages, as it influences the density, performance, and manufacturability of the integrated circuit (IC). A higher utilization factor means more of the core area is being used for active circuitry, potentially leading to more compact designs. However, it must be balanced carefully to avoid routing congestion and thermal issues. Typically, the utilization factor is kept below 80% to allow sufficient space for routing and to manage heat dissipation effectively.

### Core Width and Height of the Die
The core width and height refer to the dimensions of the central part of the die where the active circuitry is placed. This core area excludes the peripheral regions used for I/O pads and other non-core functions. The dimensions of the core are determined by the requirements of the design, including the number of standard cells, macros, and other components that need to be placed within the core. The core size is a key factor in determining the overall size of the die and directly influences the cost and performance of the final IC. Efficiently optimizing the core's width and height is crucial to achieving a balance between the chip's functionality, power consumption, and manufacturing yield.
![S14](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/Screenshots%20vsd/S14.png)
## Locations of Preplaced cells
**Locations of Preplaced Cells** refer to the specific, fixed positions within the chip's layout where certain standard cells, macros, or IP blocks are placed early in the physical design process. These cells are typically large or critical components, such as memory blocks, PLLs (Phase-Locked Loops), or other essential IPs, whose locations are predetermined based on design requirements, such as performance, signal integrity, or routing efficiency.

Preplacing these cells ensures that the most important components are optimally positioned to meet design constraints, such as minimizing signal delays or managing power distribution. Once preplaced, the rest of the standard cells are arranged around these fixed components during the Place and Route (P&R) process. This approach helps to streamline routing, reduce congestion, and ensure the overall efficiency of the chip's layout.
![S15](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/Screenshots%20vsd/S15.png)
## Logical Cell Placement Blockage
![S16](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/Screenshots%20vsd/S16.png)
## Amount of Switching Current
![S17](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/Screenshots%20vsd/S17.png)
## Day-2 Labs
![S18](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/Screenshots%20vsd/S18.png)

![S19](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/Screenshots%20vsd/S19.png)

![S20](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/Screenshots%20vsd/S20.png)

![S21](https://github.com/Arnav-12/VLSI-SoC-Design/blob/main/Screenshots%20vsd/S21.png)



