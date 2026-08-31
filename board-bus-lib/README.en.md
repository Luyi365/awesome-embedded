# Board-Level Bus Protocol Libraries

<!-- i18n:language-selector:start -->
[中文](README.md) | **English**
<!-- i18n:language-selector:end -->

> **Device scanning**: Uses software scanning to detect connected hardware and identify hardware IDs. It is important for checking devices during initialization.
> 
> **Adaptive identification**: Adaptive identification builds on device scanning. A product may use multiple chip types, and scan results can be used to identify and match them adaptively, avoiding omissions for older hardware.  
> Each adaptive-identification method differs; for example, I2C can detect responses to determine device addresses, whereas UART baud rate can be identified by measuring the timing of start and end frames.  

## UART

> Besides using standard GPIO pins to simulate UART high and low levels, PWM can simulate transmission and ADC can simulate reception, providing greater speed and accuracy.  

### LwOW

[![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwow)](https://github.com/MaJerle/lwow/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwow)](https://github.com/MaJerle/lwow/commits) | [![GitHub License](https://img.shields.io/github/license/MaJerle/lwow)]()

**Link** - [LwOW latest-develop documentation — LwOW documentation](https://docs.majerle.eu/projects/lwow/en/latest/)  
**Features** - A professional 1-Wire protocol library that supports communication through UART or a single GPIO and provides thread-safe APIs.  

#### Notes

- Hardware performs timing control.

---

### MUDLink

[![GitHub Repo stars](https://img.shields.io/github/stars/jakeread/mudlink)](https://github.com/jakeread/mudlink/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/jakeread/mudlink)](https://github.com/jakeread/mudlink/commits) | [![GitHub License](https://img.shields.io/github/license/jakeread/mudlink)]()

**Link** - [jakeread/mudlink: Modular UART Duplex Link: cobs, crc, flow-control and delivery guarantees on any UART port in Arduino](https://github.com/jakeread/mudlink)  
**Features** - Elevates UART serial communication to a link/transport layer, guarantees framed-packet delivery, and provides delivery assurance, flow control, and link-performance statistics.  

#### Notes

---

## CDbus

[![GitHub Repo stars](https://img.shields.io/github/stars/dukelec/cdbus)](https://github.com/dukelec/cdbus/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/dukelec/cdbus)](https://github.com/dukelec/cdbus/commits) | [![GitHub License](https://img.shields.io/github/license/dukelec/cdbus)]()

> An abbreviation for Controller Distributed Bus. It is a simple protocol designed around serial buses. It improves on the difficulty of parsing AT commands, Modbus's single-direction querying, PPP escaping, and the low efficiency of string protocols. Documentation: [cdbus_doc/intro_zh.md at master · dukelec/cdbus_doc](https://github.com/dukelec/cdbus_doc/blob/master/intro_zh.md)

### CDBUS

**Link** - [dukelec/cdbus: CDBUS (Controller Distributed Bus) Protocol and IP Core](https://github.com/dukelec/cdbus)  
**Features** - A simple, efficient fieldbus compatible with UART and RS-485 protocols and hardware. It introduces hardware packet segmentation and arbitration, allowing every node to send and receive packets freely.  

#### Notes

- The provided [CDNET](https://github.com/dukelec/cdnet) upper-layer protocol supports data-table access, printing, IAP, waveform display, and more.
- The [CDNET TUN](https://github.com/dukelec/cdnet_tun) extension maps simple serial packets to PC IP/UDP packets.

---

## Modbus

### freemodbus

[![GitHub Repo stars](https://img.shields.io/github/stars/cwalter-at/freemodbus)](https://github.com/cwalter-at/freemodbus/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/cwalter-at/freemodbus)](https://github.com/cwalter-at/freemodbus/commits) | [![GitHub License](https://img.shields.io/github/license/cwalter-at/freemodbus)]()

**Link** - [cwalter-at/freemodbus: BSD licensed MODBUS RTU/ASCII and TCP slave](https://github.com/cwalter-at/freemodbus)  
**Features** - A Modbus protocol stack ported by armink, supporting both master and slave functionality.  

#### Notes

- ESP wrapper: [espressif/esp-modbus: ESP-Modbus - the officially suppported library for Modbus protocol (serial RS485 + TCP over WiFi or Ethernet).](https://github.com/espressif/esp-modbus)

---

### nanoMODBUS

[![GitHub Repo stars](https://img.shields.io/github/stars/debevv/nanoMODBUS)](https://github.com/debevv/nanoMODBUS/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/debevv/nanoMODBUS)](https://github.com/debevv/nanoMODBUS/commits) | [![GitHub License](https://img.shields.io/github/license/debevv/nanoMODBUS)]()

**Link** - [debevv/nanoMODBUS: A compact MODBUS RTU/TCP C library for embedded/microcontrollers](https://github.com/debevv/nanoMODBUS)  
**Features** - A compact Modbus library that can be feature-trimmed as needed and is intended for resource-constrained environments.  

#### Notes

- Introduction: [An embedded developer's Modbus savior: a full industrial communication implementation in 2,000 lines](https://mp.weixin.qq.com/s/v57aGCb9d-IS_Z957vtktQ)

---

## I2C

### i2c_scanner

**Link** - [I2C device scan - Gitee Code Snippet](https://gitee.com/Luyi365/codes/7yob95ircndjx2mzv14l013)  
**Features** - An I2C device-scanning library extracted from Nordic's SDK that can scan the number and addresses of onboard I2C devices.  

#### Notes

---

## SPI

### SFUD

[![GitHub Repo stars](https://img.shields.io/github/stars/armink/SFUD)](https://github.com/armink/SFUD/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/armink/SFUD)](https://github.com/armink/SFUD/commits) | [![GitHub License](https://img.shields.io/github/license/armink/SFUD)]()

**Link** - [armink/SFUD: An using JEDEC's SFDP standard serial (SPI) flash universal driver library | 一款使用 JEDEC SFDP 标准的串行 (SPI) Flash 通用驱动库](https://github.com/armink/SFUD)  
**Features** - An open-source universal serial SPI Flash driver library that supports a range of Flash chips through device tables.  

#### Notes

---

## USB

### TinyUSB

[![GitHub Repo stars](https://img.shields.io/github/stars/hathach/tinyusb)](https://github.com/hathach/tinyusb/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/hathach/tinyusb)](https://github.com/hathach/tinyusb/commits) | [![GitHub License](https://img.shields.io/github/license/hathach/tinyusb)]()

**Link** - [TinyUSB](https://tinyusb.org)  
**Features** - An open-source cross-platform USB host/device stack for embedded systems. It is memory-safe, uses no dynamic allocation, is thread-safe, and defers all interrupt events for handling in non-ISR task functions.  

#### Notes

---

### CherryUSB

[![GitHub Repo stars](https://img.shields.io/github/stars/cherry-embedded/CherryUSB)](https://github.com/cherry-embedded/CherryUSB/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/cherry-embedded/CherryUSB)](https://github.com/cherry-embedded/CherryUSB/commits) | [![GitHub License](https://img.shields.io/github/license/cherry-embedded/CherryUSB)]()

**Link** - [GitHub - cherry-embedded/CherryUSB: Tiny and portable USB Stack (device & host) for embedded system with USB IP](https://github.com/cherry-embedded/CherryUSB)  
**Features** - A USB host/device protocol stack for embedded systems (with USB IP). It is portable across platforms and suits chips that lack a built-in USB protocol stack.  

#### Notes

---

## Interboard Communication

### ESSL

[![GitHub Repo stars](https://img.shields.io/github/stars/espressif/idf-extra-components)](https://github.com/espressif/idf-extra-components/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/espressif/idf-extra-components?path=esp_serial_slave_link)](https://github.com/espressif/idf-extra-components/commits?path=esp_serial_slave_link) | [![GitHub License](https://img.shields.io/github/license/espressif/idf-extra-components)]()

**Link** - [idf-extra-components/esp_serial_slave_link at master · espressif/idf-extra-components](https://github.com/espressif/idf-extra-components/tree/master/esp_serial_slave_link)  
**Features** - ESP's serial slave link component, allowing a host to communicate with slaves through bus drivers and the corresponding protocol. In essence, it is MCU-to-MCU communication with an additional layer.  

#### Notes

---

### SACP

[![GitHub Repo stars](https://img.shields.io/github/stars/Snapmaker/SnapmakerController-IDEX)](https://github.com/Snapmaker/SnapmakerController-IDEX/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/Snapmaker/SnapmakerController-IDEX?path=snapmaker/protocol)](https://github.com/Snapmaker/SnapmakerController-IDEX/commits?path=snapmaker/protocol) | [![GitHub License](https://img.shields.io/github/license/Snapmaker/SnapmakerController-IDEX)]()

**Link** - [SnapmakerController-IDEX/snapmaker/protocol at main · Snapmaker/SnapmakerController-IDEX](https://github.com/Snapmaker/SnapmakerController-IDEX/tree/main/snapmaker/protocol)  
**Features** - Snapmaker's device data-communication protocol, implemented in C++ for communication among multiple devices in a complete machine.  

#### Notes

- Introduction: [Design and implementation of SACP, an embedded C/C++ communication protocol for multiple devices](https://mp.weixin.qq.com/s/Kj-9V5xJBlQQTgMj97O-Yw)
- Related: [MVC Pattern](./appendix.en.md#mvc-pattern)

---
