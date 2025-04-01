# POV Wand v2 Development Guide

## Project Overview
Persistence of Vision (POV) display for AT89S52 (8051) microcontroller that shows text/images when waved in air.

## Development Environment
- Keil µVision IDE and C51 compiler
- Output: Objects/POVwand2.hex for device programming
- Build command: Use Keil IDE (F7 or Build button)

## Code Style Guidelines
- Use macros: `uchar` for unsigned char, `uint` for unsigned int
- 2-space indentation with consistent spacing
- Add comments above functions explaining purpose
- Use descriptive variable names (avoid single-letter except in loops)
- Store display patterns with `code` qualifier for ROM storage
- Initialize variables at declaration when possible
- Use P0/P2 ports for LED outputs (always invert with bitwise ~ operator)
- Define hardware pins with descriptive names (e.g., KEY for button)
- Keep display functions consistent using common timing patterns
- Include proper button debounce when reading inputs

## Testing
- Use simulator in Keil IDE to validate timing
- Test individual patterns separately using display functions
- Verify interrupt handling with breakpoints
- Adjust DelayUs values to calibrate display timing

## Common Issues
- Timing calibration critical for readable display
- Interrupt counting must handle motion sensor triggers correctly
- Button debounce required for reliable operation