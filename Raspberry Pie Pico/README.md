# Raspberry Pi Pico Starter Kit

My entry-level progression through core embedded systems concepts using a Lafvin Raspberry Pi Pico starter kit. Each numbered folder is a self-contained exercise: goal, circuit, code, results, and problems encountered.

This is intentionally the **beginner-tier** section of my electronics portfolio — later projects build on the skills established here (GPIO, I2C, PWM, interrupts) before moving into wireless, analog, and RF work.

## Exercises

| # | Project | Concepts Covered | Status |
|---|---|---|---|
| 01 | [Blink LED](./01-blink-led/) | GPIO output, timing, C++/CMake basics | ✅ Complete |
| 02 | [Button Input](./02-button-input/) | GPIO input, pull-up/pull-down resistors, debouncing | 🔲 In progress |
| 03 | PWM Servo Control | PWM, duty cycle, servo timing | ⬜ Planned |
| 04 | I2C LCD1602 Display | I2C protocol, character displays | ⬜ Planned |
| 05 | PIR Motion Sensor | Digital input, interrupts (IRQ) | ⬜ Planned |

## Hardware Used

- Raspberry Pi Pico (RP2040) — for these introductory exercises
- Lafvin starter kit components (breadboard, jumper wires, resistors, LEDs, buttons, IIC LCD1602, HC-SR501 PIR sensor)
- Cationsky electronic component assortment (2050 pcs) — for op-amps and additional passives

## Skills Demonstrated

GPIO control · PWM · I2C communication · interrupt-driven programming · C++ · CMake / cross-compiled build systems · breadboard prototyping · datasheet reading · systematic hardware debugging

## Setup

All exercises are written in **C++** using the official [Raspberry Pi Pico C/C++ SDK](https://github.com/raspberrypi/pico-sdk), built with CMake. This mirrors the toolchain (C/C++, CMake, cross-compilation) commonly expected for embedded/EE roles.

**Recommended: VS Code + Raspberry Pi Pico extension** (easiest path — handles SDK, toolchain, and CMake setup automatically):
1. Install [VS Code](https://code.visualstudio.com/) and the official **Raspberry Pi Pico** extension from the marketplace
2. Use the extension's "Import Project" or "New Project" command, pointing it at a given exercise's `code/` folder
3. Build and flash directly from the VS Code sidebar

**Manual/terminal setup** (Linux/macOS):
1. Install the ARM cross-compiler toolchain: `arm-none-eabi-gcc`, `cmake`, `build-essential`
2. Clone the SDK: `git clone -b master https://github.com/raspberrypi/pico-sdk.git && cd pico-sdk && git submodule update --init`
3. Set the environment variable: `export PICO_SDK_PATH=/path/to/pico-sdk`
4. In each exercise's `code/` folder: `mkdir build && cd build && cmake .. && make -j4`
5. Hold **BOOTSEL** while plugging in the Pico via USB, then drag the generated `.uf2` file onto the mounted `RPI-RP2` drive

Each exercise's `code/` folder is a self-contained CMake project (`CMakeLists.txt` + `pico_sdk_import.cmake` + source).
