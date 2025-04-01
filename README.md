# POV Wand v2

A Persistence of Vision (POV) display project for AT89S52 (8051) microcontroller.

## Overview

This project implements a handheld POV display that shows text and images when waved through the air. The device uses a column of 16 LEDs (8 on Port P0 and 8 on Port P2) and a motion sensor to trigger the display.

## Features

- Multiple display patterns including text, emojis, and graphics
- User-selectable patterns via button press
- Motion-activated display using interrupt-driven design
- Optimized for 8051-based AT89S52 microcontroller

## Development Environment

- Keil µVision IDE and C51 compiler
- Target MCU: AT89S52 (8051-based, 8-bit architecture)

## Hardware Requirements

- AT89S52 microcontroller
- 16 LEDs arranged in a vertical column
- Motion sensor connected to INT0 (P3.2)
- Pattern selection button connected to P3.7
- Power supply (battery)

## Building the Project

1. Open `POVwand2.uvproj` in Keil µVision IDE
2. Build the project (F7 or Build button)
3. Program the resulting `Objects/POVwand2.hex` file to the AT89S52 microcontroller

## Usage

1. Power on the device
2. Press the button to select a display pattern
3. Wave the device back and forth to view the pattern