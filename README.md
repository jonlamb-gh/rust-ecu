# rust-ecu

Electronic fuel injection and engine control unit written in Rust

Inspired by [rusEFI](https://github.com/rusefi/rusefi).

See their [hardware](https://rusefi.com/wiki/index.php?title=Manual:Hardware_Frankenso_board).

Initially targeting these two use use cases:

- 2005 Honda CBR 1000 RR motorcycle with a handful of engine mods
- 1993 Toyota 4x4 pickup, mostly stock with emission control system removed

For now, this is just a place holder for my experiments.

Short term goals:

- a reasonable Rust port of rusEFI, not sure if I'll stick with the interrupt driven design yet
- running on the same hardware, STM32F407 discovery board
- either bare-metal or maybe some RTOS

Long term goals:

- run on some heterogeneous multi-core SoC, like the [Nitrogen6 SoloX board](https://boundarydevices.com/product/nit6_solox-imx6/)
- M4 core runs hard real-time tasks, bare-metal or RTOS
- A9 core(s) run seL4 micro-kernel
- core-to-core IPC via shared memory and [RPMsg-lite](https://github.com/codeauroraforum/rpmsg-lite) or similar