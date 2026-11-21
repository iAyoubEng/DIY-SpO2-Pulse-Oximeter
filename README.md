# DIY SpO2 Pulse Oximeter

A custom-designed pulse oximeter built from scratch using KiCad 9.0.

## Overview

This project is a blood oxygen saturation (SpO2) and heart rate monitor, designed as a learning exercise in PCB design and embedded electronics.

## Hardware

| Component | Description |
|-----------|-------------|
| Arduino Nano v3.x | Microcontroller |
| MAX30102 | Pulse oximeter & heart-rate sensor (I2C) |
| SSD1306 | 0.96" OLED display (I2C) |
| Push button | User input |
| LEDs, resistors, capacitors | Supporting circuitry |

## PCB

- **4-layer board** (F.Cu, In1.Cu, In2.Cu, B.Cu)
- Custom footprints for the MAX30102 and SSD1306 modules
- Gerber files included, ready for fabrication

## Project Structure

```
├── learning.kicad_sch       # Schematic
├── learning.kicad_pcb       # PCB layout
├── learning.kicad_pro       # Project settings
├── spo2_stuff.kicad_sym     # Custom symbol library
├── spo2_stuff.pretty/       # Custom footprint library
├── gerbers/                 # Fabrication files
└── DIYSpo2_gerbers.zip      # Gerbers (zipped, fab-ready)
```

## Tools

- [KiCad 9.0](https://www.kicad.org/) — Schematic & PCB design

## License

This project is open source. Feel free to use it as a reference for your own designs.
