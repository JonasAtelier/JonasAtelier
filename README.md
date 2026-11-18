# Jonas Atelier

![Jonas Atelier embedded library workshop](assets/atelier-banner.svg)

I’m Jonas Chan. I build robots and write the C libraries that connect their sensors, motors, and controllers. My work spans portable control algorithms, ESP32 firmware, and STM32 drivers. I keep the code close to the hardware, with datasheet references for register settings and examples you can run on a bench or a laptop.

**Contents** · [Library search](#library-search) · [Featured libraries](#featured-libraries) · [On the bench](#on-the-bench)

## Library search

**[Open the full library index →](https://github.com/JonasAtelier/jonas-atelier-libraries#library-search)**

| What are you building? | Where to look |
| --- | --- |
| A board that reads a sensor or drives a motor | [ESP32 and STM32 drivers, indexed by part number](https://github.com/JonasAtelier/jonas-atelier-libraries#esp32-and-stm32-drivers) |
| A control loop, filter, or path follower | [Portable C libraries](https://github.com/JonasAtelier/jonas-atelier-libraries#portable-c-libraries) |
| An ESP32 project with CAN, a display, or an SD card | [ESP-IDF components](https://github.com/JonasAtelier/jonas-atelier-libraries#esp-idf-components) |
| Firmware for a robot or a custom board | [Robots and build tools](https://github.com/JonasAtelier/jonas-atelier-libraries#robots-and-build-tools) |

## Featured libraries

| [UPID feedback loop](https://github.com/JonasAtelier/upid) | [ESP32 CAN transceiver](https://github.com/JonasAtelier/esp-sn65hvd230-can) |
| :---: | :---: |
| [<img src="https://raw.githubusercontent.com/JonasAtelier/upid/stable/assets/control-loop.svg" height="118" alt="UPID feedback loop and simulated step response">](https://github.com/JonasAtelier/upid) | [<img src="https://raw.githubusercontent.com/JonasAtelier/esp-sn65hvd230-can/stable/doc/module.jpg" height="118" alt="SN65HVD230 CAN transceiver breakout">](https://github.com/JonasAtelier/esp-sn65hvd230-can) |
| Run a heater simulation on a laptop. Change the gains to see overshoot and settling time. [Run the example](https://github.com/JonasAtelier/upid#run-the-heater-example) · [Tuning measurements](https://github.com/JonasAtelier/upid/blob/HEAD/TUNING.md) | Connect two CAN nodes, receive a frame, then try filters and callbacks. Physical bench validation is pending. [Wiring and first frame](https://github.com/JonasAtelier/esp-sn65hvd230-can#receive-your-first-frame) |

## On the bench

Dingo turns walking commands into positions for twelve servos. Nova coordinates steering and drive on a swerve wheel. Flux uses rotor position and phase-current feedback to control a three-phase motor. These projects are where the sensor and control libraries come together. [Project directory](https://github.com/JonasAtelier/jonas-atelier-libraries#robots-and-build-tools)

I also build **termcode**, a Linux terminal editor with a Git review panel. [Downloads and user guide](https://github.com/JonasAtelier/termcode-releases)
