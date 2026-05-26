# ATmega328P Custom Development Board

An industry-standard, standalone microcontroller development board designed using **KiCad 10.0**. This project serves as a robust hardware platform for learning circuit design, power regulation, and microcontroller prototyping.

## 📌 Project Overview
The board breaks out all digital and analog pins of the ATmega328P microcontroller to standard 2.54mm pin headers while integrating a clean power management section to ensure stable operation.

### Key Hardware Features:
* **Microcontroller:** ATmega328P (Through-Hole DIP-28 package for easy hand-soldering).
* **Power Supply:** On-board **LM7805** linear voltage regulator supplying a stable +5V DC output. Accepts a wide input voltage range via a 2-pin Screw Terminal.
* **Decoupling Network:** Optimized parallel capacitor configuration ($0.1\mu F$ Ceramic + $10\mu F$ Electrolytic) placed closest to the IC pins to suppress high-frequency noise.
* **Clock Source:** High-precision $16\text{MHz}$ Crystal Oscillator with matching $22\text{pF}$ loading capacitors.
* **Status Indicators:** On-board Power LED with a $330\Omega$ current-limiting resistor.
* **Form Factor:** Compact Single-Layer/Double-Layer routing with a solid **Ground Plane (Copper Pour)** for EMI mitigation and thermal dissipation.

## 🛠️ Design Parameters & Integrity
* **Software Used:** KiCad PCB Editor
* **Design Rule Check (DRC):** Passed with **0 Errors / 0 Warnings**
* **Track Widths:** * Signal Lines: 0.25mm - 0.3mm
  * Power Lines (VCC/GND): 0.5mm - 0.6mm (Optimized for trace current density)

## 🛠️ Visuals & Design Layout
### 1. 📸 3D Render Preview
<img width="3450" height="1886" alt="ATmega controller board" src="https://github.com/user-attachments/assets/8a147d75-6841-4bfe-bad3-aa8b877fb6de" />

### 2. PCB Layout (Top & Bottom Layers)
#### Top Layer Layout
<img width="2245" height="1691" alt="Screenshot (20)" src="https://github.com/user-attachments/assets/9c8a8b24-557e-4ddd-8fbe-88ac15985a18" />

#### Bottom Layer Layout
<img width="2248" height="1654" alt="Screenshot (21)" src="https://github.com/user-attachments/assets/a598e82d-b49f-4e3f-8227-e199580887b5" />

## 📁 Repository Structure

This repository contains all the native design assets and manufacturing files required to replicate or modify this project.

### 🛠️ Core EDA Design Files (KiCad)
* **[`ATmega controller board.kicad_sch`](./ATmega%20controller%20board.kicad_sch)** - Schematic capture showing the ATmega328P microcontroller core, LM7805 voltage regulation circuit, decoupling networks, and crystal loading capacitors.
* **[`ATmega controller board.kicad_pcb`](./ATmega%20controller%20board.kicad_pcb)** - Physical PCB layout featuring optimized signal trace routing, 45° angles, and solid ground planes.

### 📦 Manufacturing & Fabrication Outputs
* **[`Gerber.zip`](./Gerber.zip)** - Production-ready manufacturing package containing all necessary layers (Copper, Solder Mask, Silkscreen) and NC Drill files, ready to upload directly to JLCPCB, PCBWay, etc.
