# Electronics & EE Projects

A portfolio of hands-on electronics and embedded systems projects, documenting circuits, code, and the debugging process behind each build. Built as I work toward roles in electrical/embedded engineering.

Each project folder includes: stated goal, components used, circuit details, code, results (photos/notes), project costs, problems encountered and how they were resolved, and next steps.

## Projects

| Project | Description | Skills Demonstrated |
|---|---|---|
| [Raspberry Pi Pico Kit](./raspberry-pi-pico-kit/) | Beginner-tier progression through GPIO, PWM, I2C, and sensor interfacing | C++, CMake, GPIO, PWM, I2C, digital I/O |
| *(more coming soon)* | | |

## Planned / In Progress

- Wi-Fi Signal Heatmap (Pico 2 W)
- FM Radio Transmitter Circuit
- Home Environmental Monitor
- Music-Reactive LED Lighting
- Regulated Power Supply Design
- Custom PCB Fabrication (KiCad → JLCPCB)

## Skills Demonstrated Across This Repo

- **Microcontroller programming**: MicroPython on RP2040/RP2350 (Raspberry Pi Pico family)
- **Digital I/O**: GPIO control, interrupts, debouncing
- **Communication protocols**: I2C, SPI, UART
- **Analog electronics**: op-amp circuits, filters, signal conditioning
- **RF/wireless**: Wi-Fi (RSSI/networking), basic RF oscillator design
- **Power electronics**: linear/switching regulators, battery characterization
- **Test & measurement**: multimeter, oscilloscope, systematic debugging
- **PCB design**: schematic capture and layout in KiCad
- **Tools**: breadboard prototyping, soldering, 3D-printed prototyping aids

## Tools & Environment

- **Language**: C++ (primary, via the Raspberry Pi Pico C/C++ SDK), MicroPython where noted for rapid prototyping
- **Build system**: CMake, cross-compiled with arm-none-eabi-gcc
- **Hardware**: Raspberry Pi Pico 2 W, Lafvin Pico starter kit, Cationsky component assortment
- **Design tools**: KiCad, LTspice
- **Test equipment**: Digital multimeter, oscilloscope

## License

This repository is licensed under the MIT License; see [LICENSE](./LICENSE) for details.
