# Chip and Toolchain Adaptation Libraries
<!-- i18n:language-selector:start -->
[中文](README.md) | **English**
<!-- i18n:language-selector:end -->

> Support libraries for a specific type of chip or a designated toolchain. Manufacturers generally provide SDKs for these tasks, while support for some overly old chips is collected and provided by the community.

## 51

### 8051-ELL

[![Gitee Repo stars](https://gitee.com/gevico/mcs51-ell/badge/star.svg?theme=gvp)](https://gitee.com/gevico/mcs51-ell/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/gevico/mcs51-ell&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/gevico/mcs51-ell&query=$.license&label=license)]()

**Link** - [MCS51-ELL: A hardware abstraction platform specifically designed for enhanced 1T8051-core MCUs.](https://gitee.com/gevico/mcs51-ell)  
**Features** - An ELL (efficient low-layer) library that combines the programming concepts of HAL and LL libraries, primarily targeting the STC8 series.  

#### Key Points

---

### ECBM

[![Gitee Repo stars](https://gitee.com/ecbm/ecbm_library/badge/star.svg?theme=gvp)](https://gitee.com/ecbm/ecbm_library/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/ecbm/ecbm_library&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/ecbm/ecbm_library&query=$.license&label=license)]()

**Link** - [STC8-based ECBM function library V3: The V3 release of the ECBM library is a peripheral function library based on STC8 microcontrollers and now supports every STC8 model. Its peripheral support will be improved gradually. Because there are many STC8 models, it is not possible to test each one on physical hardware; please leave a message for incompatible models. STC8 is currently the most capable 51 microcontroller series, offering up to 8K SRAM, 64K Flash, five timers, and four serial ports. The entire series includes IIC and SPI, most models include ADC, and STC8H also includes hardware USB.](https://gitee.com/ecbm/ecbm_library)  
**ECBM library lite version** - [ECBM library lite version: While promoting ECBM library V3, I repeatedly heard that ECBM used too much space. Beginners unfamiliar with the library did not know how to optimize it, so they simply stopped using it. This is the official optimized lite version. It retains the distinctive ECBM features while removing many unnecessary, marginal functions, leaving an STC8 library focused on the essentials and a small footprint.](https://gitee.com/ecbm/ecbm-library-lite)  
**Features** - 51-chip peripheral function library; take whichever module you need.  

#### Key Points

- The lite library has fewer examples and no device layer compared with the standard library.

---

## AVR

---

## ST

### STM32F4 Discovery

[![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/stm32f429)](https://github.com/MaJerle/stm32f429/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/stm32f429)](https://github.com/MaJerle/stm32f429/commits) | [![GitHub License](https://img.shields.io/github/license/MaJerle/stm32f429)]()

**Link** - [MaJerle/stm32f429: Keil projects and libraries for STM32F4xx devices](https://github.com/MaJerle/stm32f429)  
**Features** - A collection of driver libraries for STM32F4-series microcontrollers, including implementation tutorials and examples for multiple peripherals and interfaces.  

#### Key Points

---

## ESP

### LwESP

[![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwesp)](https://github.com/MaJerle/lwesp/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwesp)](https://github.com/MaJerle/lwesp/commits) | [![GitHub License](https://img.shields.io/github/license/MaJerle/lwesp)]()

**Link** - [LwESP latest-develop documentation — LwESP documentation](https://docs.majerle.eu/projects/lwesp/en/latest/)  
**Features** - Professional AT parser library intended for communicating with ESP devices from other devices through AT commands.  

#### Key Points

- Supports Espressif AT software;
- Currently supports operating-system mode only;

---

### ESPUI

[![GitHub Repo stars](https://img.shields.io/github/stars/s00500/ESPUI)](https://github.com/s00500/ESPUI/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/s00500/ESPUI)](https://github.com/s00500/ESPUI/commits) | [![GitHub License](https://img.shields.io/github/license/s00500/ESPUI)]()

**Link** - [s00500/ESPUI: A simple web user interface library for ESP32 and ESP8266](https://github.com/s00500/ESPUI)  
**Features** - A simple web user interface library for ESP32 and ESP8266 devices. It lets users create and manage device web interfaces easily without HTML, CSS, or JavaScript frontend-development knowledge.  

#### Key Points

---

### FluidNC

[![GitHub Repo stars](https://img.shields.io/github/stars/bdring/FluidNC)](https://github.com/bdring/FluidNC/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/bdring/FluidNC)](https://github.com/bdring/FluidNC/commits) | [![GitHub License](https://img.shields.io/github/license/bdring/FluidNC)]()

**Link** - [bdring/FluidNC: The next generation of motion control firmware](https://github.com/bdring/FluidNC)  
**Features** - A CNC firmware library optimized for ESP32 controllers.  

#### Key Points

---

### Rabbit GRBL

[![GitHub Repo stars](https://img.shields.io/github/stars/SourceRabbit/RabbitGRBL)](https://github.com/SourceRabbit/RabbitGRBL/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/SourceRabbit/RabbitGRBL)](https://github.com/SourceRabbit/RabbitGRBL/commits) | [![GitHub License](https://img.shields.io/github/license/SourceRabbit/RabbitGRBL)]()

**Link** - [SourceRabbit/RabbitGRBL: Professional grade, 100% GRBL compatible motion control firmware for the ESP32](https://github.com/SourceRabbit/RabbitGRBL)  
**Features** - A CNC firmware library running on ESP32 processors, highly optimized to maintain stable, jitter-free control pulses up to 120 kHz.  

#### Key Points

---

## SIMCom

### LwCELL

[![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwcell)](https://github.com/MaJerle/lwcell/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwcell)](https://github.com/MaJerle/lwcell/commits) | [![GitHub License](https://img.shields.io/github/license/MaJerle/lwcell)]()

**Link** - [LwCELL latest-develop documentation — LwCELL documentation](https://docs.majerle.eu/projects/lwcell/en/latest/)  
**Features** - Professional AT parser library intended for communicating with SIMCom devices from other devices through AT commands.  

#### Key Points

---

## MDK

### flash\_blob

[![GitHub Repo stars](https://img.shields.io/github/stars/Aladdin-Wang/flash_blob)](https://github.com/Aladdin-Wang/flash_blob/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/Aladdin-Wang/flash_blob)](https://github.com/Aladdin-Wang/flash_blob/commits) | [![GitHub License](https://img.shields.io/github/license/Aladdin-Wang/flash_blob)]()

**Link** - [Aladdin-Wang/flash_blob: A flash driver adapted for almost any microcontroller model.](https://github.com/Aladdin-Wang/flash_blob)  
**Features** - Quickly generates generic flash drivers using MDK FLM files.  

#### Key Points

- Usage guide: [Generate generic flash drivers using MDK FLM files - CSDN Blog](https://blog.csdn.net/sinat_31039061/article/details/128350295)

---

## Driver

### LibDriver

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)

**Link** - [libdriver (LibDriver)](https://github.com/libdriver)  
**Features** - An open-source driver-development organization containing driver libraries for all common peripheral modules (140+).  

#### Key Points

---
