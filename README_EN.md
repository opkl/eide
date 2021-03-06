# EIDE

[![](https://vsmarketplacebadge.apphb.com/version/cl.eide.svg)](https://marketplace.visualstudio.com/items?itemName=CL.eide) [![](https://vsmarketplacebadge.apphb.com/installs/cl.eide.svg)](https://marketplace.visualstudio.com/items?itemName=CL.eide) [![](https://vsmarketplacebadge.apphb.com/downloads/cl.eide.svg)](https://marketplace.visualstudio.com/items?itemName=CL.eide) [![](https://vsmarketplacebadge.apphb.com/rating/cl.eide.svg)](https://marketplace.visualstudio.com/items?itemName=CL.eide)

## Summary 📑

A 8051/STM8/ARM **IDE** with multiple toolchains for Vs Code, A Keil C51/STM32 **project migration tool**. Provide development, compilation, burning, management functions for **8051/stm8/arm** projects on vscode.

**Keil 5 version is mainly supported.**

**Only for Windows platform**

***

![preview](./res/preview/show.png)

***

## Feature 🎉

* Import Keil uVision 5 project as a vscode workspace
* Export eide project as a Keil project file (.uvprojx, .uvproj)
* Create, Open eide project
* Create, Import eide project template
* Build, Fast build project; support all of Keil's toolchains, and additional toolchains
* Generate hex, bin, elf
* Download to device board
* Serialport monitor
* manage project
* Generate `cortex-debug` debug configurations for STM32 project

***

## Toolchain support 🔨

#### ![8051](https://img.shields.io/badge/-8051_:-grey.svg) ![status](https://img.shields.io/badge/Keil_C51-done-brightgreen.svg) ![status](https://img.shields.io/badge/SDCC-done-brightgreen.svg)


#### ![STM8](https://img.shields.io/badge/-STM8_:-grey.svg) ![status](https://img.shields.io/badge/IAR_STM8-done-brightgreen.svg)


#### ![ARM](https://img.shields.io/badge/-ARM_:-grey.svg) ![status](https://img.shields.io/badge/ARMCC_V5-done-brightgreen.svg) ![status](https://img.shields.io/badge/ARMCC_V6-done-brightgreen.svg) ![status](https://img.shields.io/badge/ARM_GCC-done-brightgreen.svg)

***

## Syntax support

* Standard C syntax highlights, code snippets
* 8051 C syntax highlights, code snippets
* 8051 assembly(A51) syntax highlights, code snippets

***

## Usage 📖

#### There is a simple [user's manual](https://github0null.github.io/eide-manual) for foreign friends

***

## Version changes 🔔

> #### Feedback 👉 [Github Issue](https://github.com/github0null/eide/issues)

### [v1.13.1]
- Changed: Adjust the compiled configuration format for arm-gcc. The old configuration format is no longer valid
- Changed: Complete the project build with relative paths
- Optimized: Display of view
- Optimized: Reduce the length of the command line
- Optimized: Remove useless functions
- Fixed: The custom jflash path has been overwrited
***

### [v1.13.0]
- New: IAR for STM8 toolchain support
- New: STM8-Debug debug configuration
- New: custom jflash file
- Fixed: can't delete include path
- Fixed: some bugs
***

### [v1.12.2]
- Fixed: ARMCC V5 C++ Parameter problems
- Fixed: some bugs
***

## Attention 🚩
  + **The multi-objective Keil project is not supported**
  + **Make sure that JLink is installed on your computer before using the ARM burn tool**
  + **Import keil project will be failed if Keil uVision's version is tool low**
  + **Import process: source files in Keil project structure will be copied to eide project directory, header search path, macro, compile configuration inherited from Keil**
