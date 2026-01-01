
Capstone Project Proposal

Custom Zynq-7000 FPGA Development Board (Arty Z7–Compatible)
Overview

This project is a custom FPGA development board inspired by the Digilent Arty Z7 platform, designed around the Xilinx Zynq-7000 SoC.
The board is intended as a general-purpose hardware development and learning platform with emphasis on:

FPGA + ARM (PS/PL) co-design
Proper power integrity and signal integrity practices
Manufacturable, industry-style PCB layout
Realistic interfaces used in embedded and FPGA systems

The design targets entry-level to junior FPGA / hardware engineering roles and demonstrates practical board-level engineering rather than a minimal breakout board.

Key Features

Xilinx Zynq-7000 SoC (Z7-20 / XC7Z020 class)
DDR3 SDRAM (PS memory)
HDMI interface (video output)
Ethernet PHY (10/100/1000 Mbps)
USB interface (JTAG/UART or host/device depending on configuration)
QSPI Flash (boot storage)
microSD card support
PMOD / GPIO headers
40pin Raspberry pi interface
On-board oscillators for PS and PL
User LEDs, buttons, and switches
Multi-rail power tree with switching regulators and LDOs

Design Goals

This board was designed with the following goals in mind:

Follow Xilinx Zynq hardware design guidelines
Implement correct decoupling, grounding, and plane usage
Use controlled-impedance routing for high-speed interfaces
Be compatible with low-cost PCB manufacturing and assembly
Serve as a portfolio-quality hardware project

Hardware Architecture
Zynq SoC
ARM Cortex-A9 Processing System (PS)
Programmable Logic (PL) fabric
PS-to-PL interconnect exposed for custom designs

Boot modes supported via QSPI / SD Memory

DDR3 SDRAM connected to the PS
Length-matched address, control, and data groups
Proper VREF routing and decoupling

Power Tree

Input Sources:

7-15V Barrel jack
Raspberry pi 5V
USB 5V

Generated rails:

1.0 V (FPGA core)

1.5 V (DDR3)

1.8 V (aux, IO)

3.3 V (IO and peripherals)

Switching regulators for high-current rails
Bulk and local decoupling implemented per rail
Emphasis on low loop inductance and stable PDN behavior

PCB Design Details

8-layer PCB stackup
Dedicated solid ground plane
Power planes for core rails
Signal layers for controlled routing

Controlled impedance routing for:
DDR3
HDMI
Ethernet
USB
SD

Differential pair routing with symmetry and spacing control
Thermal via stitching under FPGA ground regions
Designed for JLCPCB advanced fabrication and assembly
