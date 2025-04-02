# POV Wand v2

A Persistence of Vision (POV) display project for AT89S52 (8051) microcontroller, based on the original work from [LEAP #193 PoV Shake Stick Kit](https://leap.tardate.com/8051/povshakestickkit/).

## Overview

This project implements a handheld POV display that shows text and images when waved through the air. The device uses a column of 16 LEDs (8 on Port P0 and 8 on Port P2) and a motion sensor to trigger the display. The original code was developed by Zheng Zhong Xing (兴向荣) and has been translated from Chinese to English for better accessibility.

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

## Creating Custom Patterns

To create custom patterns for the POV wand, you can use the [POV Wand Pattern Generator](https://github.com/ahoskam/POV_wand_gen). This tool allows you to:

1. Design patterns using a graphical interface
2. Generate hex code compatible with this project
3. Copy the generated hex numbers and replace them in the code

Note: The current version generates hex code that needs to be manually inserted into the C file. Future versions aim to generate complete C files automatically.

### Pattern Format Notes

- The "Heart" format (64 columns) is recommended for English text and general patterns
- The "Hanzi" format (16 columns) is specifically designed for Chinese characters and may not work well with English text due to space constraints
- Each Chinese character typically occupies one word space, while English text requires more space per word