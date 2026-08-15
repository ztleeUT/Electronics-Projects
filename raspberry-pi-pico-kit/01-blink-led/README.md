# 01 — Blink LED

## Goal
The classic "hello world" of embedded systems: blink an external LED on and off at a fixed interval using GPIO output control.

## Components Used
- Raspberry Pi Pico
- 1x LED (5mm)
- 1x 220Ω resistor (current-limiting)
- Breadboard
- 2x jumper wires

## Circuit

```
Pico GPIO 15 ──> 220Ω resistor ──> LED anode (+, longer leg)
LED cathode (-, shorter leg) ──> Pico GND
```

*(Add a breadboard photo here: `images/circuit.jpg`)*

**Why the resistor matters**: the Pico's GPIO pins can only safely source a limited amount of current (~12mA recommended max per pin under most conditions). Without a current-limiting resistor, an LED will draw far more current than the pin — or the LED itself — can safely handle, risking damage to one or both. 220Ω is a standard safe value for a 3.3V GPIO driving a standard LED.

## Code
See [`code/blink.cpp`](./code/blink.cpp), built with CMake via the Raspberry Pi Pico C/C++ SDK.

**Build & flash:**
```bash
cd code
mkdir build && cd build
cmake .. -DPICO_BOARD=pico
make -j4
```
Hold **BOOTSEL** while plugging in the Pico via USB, then drag `build/blink_led.uf2` onto the mounted `RPI-RP2` drive.

## Result
LED blinks on/off at 1-second intervals.

*(Add a short GIF or photo here: `images/result.gif`)*

## Problems / Debugging Notes

*(Document any issues you actually hit here as you build this — for example: LED not lighting due to reversed polarity, wrong GPIO pin number vs. physical pin number, resistor value questions, etc. This section is the most valuable part of the writeup — it shows real debugging process, not just a working end result.)*

## What I'd Do Differently / Next Steps
- Try PWM-based fading instead of simple on/off (ties into Exercise 03)
- Add a second LED and alternate blinking between them
