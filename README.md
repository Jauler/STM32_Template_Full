STM32F4 Full Template
=====================

A code template for STM32F4 series processors with full DSP and StdPerph libraries.

This Template:
- Defines interrupt table at the start of Flash memory
- Builds full DSP and StdPeriph from sources
- Initializes stack on CCM memory
- Initializes .data
- Initializes .bss to zero
- Calls main

### Building

Just issue:

```
$ make
```

This assumes that make tools and toolchain is already installed and working.


### Specifying toolchain

Toolchain can be specified with environment variables.
Currently variables CROSS, CC, OBJCOPY, SIZE are used for toolchain specification
- CROSS: Specifies prefix for toolchain (e.g arm-none-eabi-), default: arm-none-eabi-
- CC: Specifies C and Assembler compiler (e.g. gcc), default: gcc
- OBJCOPY: specifies objcopy program, default: objcopy
- SIZE: specifies size program, default: size

Example:
```
make CROSS=arm-randomos-eabi- CC=cc
```



