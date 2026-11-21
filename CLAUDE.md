# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a KiCad 9.0 hardware project — a DIY SpO2 (pulse oximeter) device. It is **not a software project**; there are no build/test/lint commands.

## Key Components

- **MCU**: Arduino Nano v3.x
- **Sensor**: MAX30102 pulse oximeter/heart-rate module (custom symbol+footprint)
- **Display**: SSD1306 OLED module (custom symbol+footprint)
- **Other**: push button switch, LEDs, resistors, capacitors
- Communication between modules uses I2C

## PCB

- 4-layer board (F.Cu, In1.Cu, In2.Cu, B.Cu)
- Gerbers are exported to `gerbers/` and `DIYSpo2_gerbers.zip`

## Project File Structure

- `learning.kicad_sch` — schematic
- `learning.kicad_pcb` — PCB layout
- `learning.kicad_pro` — project settings
- `spo2_stuff.kicad_sym` — custom symbol library (MAX30102_module, SSD1306_module)
- `spo2_stuff.pretty/` — custom footprint library (MAX30102_module.kicad_mod, SSD1306.kicad_mod)
- `sym-lib-table` / `fp-lib-table` — library tables referencing the custom libs via `${KIPRJMOD}`
- `learning-backups/` — KiCad auto-backups (zip archives)

## Working with KiCad Files

- KiCad files are S-expression text format; they can be read and edited, but prefer using KiCad GUI for schematic/PCB changes to avoid corruption.
- The `fp-info-cache` is a large auto-generated file — do not manually edit.
- When scripting KiCad tasks, use `kicad-cli` for operations like exporting gerbers, BOMs, or running DRC/ERC.
