# Proj1 MicroC2 Sess3 - Matrix Interface Tester

This repository contains my first school project for **243-33A-MO: Microcontroleur 2**. The project is a PlatformIO/Arduino test tool for the course matrix interface, built for an Arduino Mega 2560 and a 64x32 RGB LED matrix.

The program reads the board inputs, shows their state on the matrix, sends button events through the serial port, and includes a few animation modes to validate the display.

## Features

- Live display of potentiometer, photoresistor, and rotary encoder values.
- Matrix visualization for the seven push buttons: up, down, left, right, A, B, and C.
- Interrupt-based rotary encoder reading.
- RGB LED testing through the A, B, and C buttons.
- Serial output for button press events.
- Multiple matrix modes:
  - `Left + Down + B` toggles the color sweep animation.
  - `Up + Down + C` toggles the custom `Projet 1` animation.

## Hardware And Tools

- Arduino Mega 2560
- MOMO RGB Matrix / 64x32 RGB LED matrix
- Push buttons, rotary encoder, potentiometer, photoresistor, and RGB LEDs
- PlatformIO
- Arduino framework
- C++

## Project Structure

```text
.
|-- platformio.ini          # PlatformIO board and framework configuration
|-- src/main.cpp            # Main program logic
|-- src/bits_manip.cpp      # Bit manipulation helper implementation
|-- include/bits_manip.h    # Bit manipulation helper declarations
|-- lib/MOMO_RGB_Matrix/    # Local RGB matrix library
`-- README.md
```

## Build And Upload

Install PlatformIO, connect the Arduino Mega 2560, then run:

```bash
pio run
pio run -t upload
```

To view serial output:

```bash
pio device monitor
```

## Notes

This was created as a school project, so the code is focused on demonstrating the required microcontroller concepts: digital inputs, analog inputs, interrupts, serial communication, RGB LED control, and matrix drawing.

## License

Released under the Unlicense. See [LICENSE](LICENSE) for details.
