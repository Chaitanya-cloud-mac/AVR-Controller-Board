# AVR Controller Board

**A custom AVR-based microcontroller development board designed for general-purpose interfacing, prototyping, and hardware control. This board features onboard power regulation, an ICSP programming interface, basic built-in I/O (LED, buzzer, tactile switch), and modular pin headers for easy expansion and integration with external peripherals.**

![Board Render](https://github.com/user-attachments/assets/d85cfee0-586b-42c2-8702-efcbb676858b)

This repository contains the complete open-source hardware design files required to view, modify, and manufacture this custom PCB. 

## 🗂️ Repository Contents

* **`/KiCad_Files`**: The raw KiCad schematic (`.kicad_sch`) and PCB layout (`.kicad_pcb`) files.
* **`/Gerbers_and_Drill`**: Production-ready Gerber (`.gbr`) and Excellon drill files. This folder can be zipped and uploaded directly to a PCB manufacturer (e.g., JLCPCB, PCBWay).
* **`/BOM`**: The Bill of Materials report listing all required components, reference designators, and quantities for assembly.
* **`/Footprints`**: A detailed footprint report mapping the schematic symbols to their physical PCB footprints.
* **`/Datasheets`**: PDF reference manuals for the critical components used on the board (e.g., AVR Microcontroller, Voltage Regulator, Darlington Array/Driver).

## ⚡ Hardware Features

* **Microcontroller:** AVR architecture (DIP-28 package)
* **High-Current Driver:** SOIC-18W footprint (e.g., ULN2803A) for driving external loads like relays, motors, or LEDs
* **Power Supply:** Standard DC Barrel Jack input with a TO-220 5V linear regulator (e.g., L7805)
* **Clock/Timing:** Standard through-hole crystal oscillator footprint (HC49-4H)
* **Programming Interface:** Standard 2x03 (6-pin) ICSP vertical header for firmware flashing
* **Onboard I/O:** * Tactile push button (6mm)
  * 3mm status LED
  * Active buzzer
* **Expansion/Interfacing:** Standard 2.54mm pitch vertical headers (1x06, 1x08) for modular connections

## 🛠️ Manufacturing & Assembly

1.  **Fabrication:** Download the contents of the `/Gerbers_and_Drill` folder as a `.zip` file and upload it to your preferred PCB fabrication house. Standard 1.6mm FR4 with a 1oz copper weight is recommended.
2.  **Assembly:** Reference the `/BOM` and `/Footprints` directories to place components. The board utilizes standard through-hole components alongside easy-to-solder SMD parts.
3.  **Flashing:** Connect a standard AVR ISP programmer (such as a USBasp or an Arduino configured as an ISP) to the 2x03 ICSP header to upload your C/C++ firmware or bootloader.
