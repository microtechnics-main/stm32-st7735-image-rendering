# STM32 ST7735 image rendering

<img src="https://microtechnics.ru/wp-content/uploads/2021/08/vyvod-izobrazheniya.jpg" width="200">

Image uploading and rendering with the use of my [STM32 ST7735 library](https://github.com/microtechnics-main/stm32-st7735-library). Necessary steps for image preparing:

- creating the .png image
- converting it to RGB565 format
- saving pixels' values inside the array
- rendering stored data

All of this in detail - in my [post](https://microtechnics.ru/displej-na-baze-st7735-i-stm32-vyvod-izobrazheniya/). Example can be built with IAR Embedded Workbench (project files included) or can be used with any other IDE. The migrating process just includes copying .c and .h library files:

- st7735.c
- st7735.h
- st7735_image.c (for image data)

Project hardware and software set:

- STM32F103RE
- IAR Embedded Workbench
- STM32CubeMx
- HAL Driver

Physical connection:

- SPI1 for communication (only MOSI ans SCK needed - PB5 for MOSI signal, PB3 for SCK)
- PB7 (Reset)
- PC11 (CS)
- PB6 (DC)
