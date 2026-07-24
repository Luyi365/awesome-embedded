# 板级总线协议库

> **设备扫描**：通过软件扫描的方式可检测含有哪些硬件，硬件的 ID 是多少，意义重大，可用于在设备初始化时进行设备检查。
> 
> **自适应识别**：自适应识别是基于设备扫描的基础上，很多时候一款产品的芯片类型拥有多种，可根据设备扫描后的信息进行自适应识别匹配，避免遗漏旧的硬件设备。  
> 另外，每一种自适应识别都不相同，例如 i2c 可以通过检测应答来判断设备地址，而串口的波特率则需要通过检测起始帧和结束帧的时间来判断。  

## UART

> 串口的模拟除了使用普通的 GPIO 进行高低电平的外，还可以使用 PWM 模拟发送，ADC 模拟接收，这样速度和准确性会更强。  

### LwOW

[![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwow)](https://github.com/MaJerle/lwow/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwow)](https://github.com/MaJerle/lwow/commits) | [![GitHub License](https://img.shields.io/github/license/MaJerle/lwow)]()

**链接**：[LwOW latest-develop documentation — LwOW documentation](https://docs.majerle.eu/projects/lwow/en/latest/)  
**特征**：专业的 1-Wire 协议库，允许通过 UART 或单 GPIO 通讯，提供线程安全的 API。  

#### 要点

- 硬件进行时序控制。

---

### MUDLink

[![GitHub Repo stars](https://img.shields.io/github/stars/jakeread/mudlink)](https://github.com/jakeread/mudlink/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/jakeread/mudlink)](https://github.com/jakeread/mudlink/commits) | [![GitHub License](https://img.shields.io/github/license/jakeread/mudlink)]()

**链接**：[jakeread/mudlink: Modular UART Duplex Link: cobs, crc, flow-control and delivery guarantees on any UART port in Arduino](https://github.com/jakeread/mudlink)  
**特征**：将UART串口提升为一个链路/传输层，并保证成帧数据包的交付，此外还传输保证和流量控制。它还记录链路性能的统计信息等功能。  

#### 要点

---

## CDbus

[![GitHub Repo stars](https://img.shields.io/github/stars/dukelec/cdbus)](https://github.com/dukelec/cdbus/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/dukelec/cdbus)](https://github.com/dukelec/cdbus/commits) | [![GitHub License](https://img.shields.io/github/license/dukelec/cdbus)]()

> 是（Controller Distributed Bus）的缩写，意为控制器分布式总线。是一种简单的协议，基于串行总线而设计。相对于其他通信协议问题，解析 AT 命令很麻烦、Modbus 只支持单方向查询、PPP 协议要转义、字符串协议效率低等问题做了改进。文档：[cdbus_doc/intro_zh.md at master · dukelec/cdbus_doc](https://github.com/dukelec/cdbus_doc/blob/master/intro_zh.md)

### CDBUS

**链接**：[dukelec/cdbus: CDBUS (Controller Distributed Bus) Protocol and IP Core](https://github.com/dukelec/cdbus)  
**特征**：一种简单高效的现场总线，基于且兼容 UART / RS-485 协议和硬件，引入了硬件分包和硬件仲裁等机制，各节点可以自由收发数据包。  

#### 要点

- 提供的[CDNET](https://github.com/dukelec/cdnet)上层协议可以支持数据表读写、打印、IAP、波形显示等功能；
- 提供的[CDNET TUN](https://github.com/dukelec/cdnet_tun)扩展可以把简单的串口数据包映射成电脑 IP/UDP 数据包；

---

## Modbus

### freemodbus

[![GitHub Repo stars](https://img.shields.io/github/stars/cwalter-at/freemodbus)](https://github.com/cwalter-at/freemodbus/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/cwalter-at/freemodbus)](https://github.com/cwalter-at/freemodbus/commits) | [![GitHub License](https://img.shields.io/github/license/cwalter-at/freemodbus)]()

**链接**：[cwalter-at/freemodbus: BSD licensed MODBUS RTU/ASCII and TCP slave](https://github.com/cwalter-at/freemodbus)  
**特征**：由 armink 移植的 modbus 协议栈，同时支持主机和从机的功能。  

#### 要点

- ESP 封装版：[espressif/esp-modbus: ESP-Modbus - the officially suppported library for Modbus protocol (serial RS485 + TCP over WiFi or Ethernet).](https://github.com/espressif/esp-modbus)

---

### nanoMODBUS

[![GitHub Repo stars](https://img.shields.io/github/stars/debevv/nanoMODBUS)](https://github.com/debevv/nanoMODBUS/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/debevv/nanoMODBUS)](https://github.com/debevv/nanoMODBUS/commits) | [![GitHub License](https://img.shields.io/github/license/debevv/nanoMODBUS)]()

**链接**：[debevv/nanoMODBUS: A compact MODBUS RTU/TCP C library for embedded/microcontrollers](https://github.com/debevv/nanoMODBUS)  
**特征**：精简的 modbus 库，可按需裁剪功能，旨在资源有限的环境中运行。  

#### 要点

- 使用介绍：[嵌入式开发者的Modbus救星：2000行代码实现全功能工业通信](https://mp.weixin.qq.com/s/v57aGCb9d-IS_Z957vtktQ)

---

## I2C

### i2c_scanner

**链接**：[I2C 设备扫描 - 代码片段 - Gitee.com](https://gitee.com/Luyi365/codes/7yob95ircndjx2mzv14l013)  
**特征**：i2c 设备扫描库，摘自 Nordic 的 SDK 库，能够扫描板载的 i2c 设备个数及设备地址。  

#### 要点

---

## SPI

### SFUD

[![GitHub Repo stars](https://img.shields.io/github/stars/armink/SFUD)](https://github.com/armink/SFUD/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/armink/SFUD)](https://github.com/armink/SFUD/commits) | [![GitHub License](https://img.shields.io/github/license/armink/SFUD)]()

**链接**：[armink/SFUD: An using JEDEC's SFDP standard serial (SPI) flash universal driver library | 一款使用 JEDEC SFDP 标准的串行 (SPI) Flash 通用驱动库](https://github.com/armink/SFUD)  
**特征**：开源的串行 SPI Flash 通用驱动库，通过编写设备表，做到能适配各型号Flash芯片。  

#### 要点

---

## USB

### TinyUSB

[![GitHub Repo stars](https://img.shields.io/github/stars/hathach/tinyusb)](https://github.com/hathach/tinyusb/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/hathach/tinyusb)](https://github.com/hathach/tinyusb/commits) | [![GitHub License](https://img.shields.io/github/license/hathach/tinyusb)]()

**链接**：[TinyUSB](https://tinyusb.org)  
**特征**：是一个用于嵌入式系统的开源跨平台 USB 主机/设备堆栈，设计为内存安全，没有动态分配，线程安全，所有中断事件都被延迟，然后在非 ISR 任务函数中处理。  

#### 要点

---

### CherryUSB

[![GitHub Repo stars](https://img.shields.io/github/stars/cherry-embedded/CherryUSB)](https://github.com/cherry-embedded/CherryUSB/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/cherry-embedded/CherryUSB)](https://github.com/cherry-embedded/CherryUSB/commits) | [![GitHub License](https://img.shields.io/github/license/cherry-embedded/CherryUSB)]()

**链接**：[GitHub - cherry-embedded/CherryUSB: Tiny and portable USB Stack (device & host) for embedded system with USB IP](https://github.com/cherry-embedded/CherryUSB)  
**特征**：移植性高的、用于嵌入式系统(带 USB IP)的 USB 主从协议栈。  

#### 要点

---

## 板间通信

### ESSL

[![GitHub Repo stars](https://img.shields.io/github/stars/espressif/idf-extra-components)](https://github.com/espressif/idf-extra-components/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/espressif/idf-extra-components?path=esp_serial_slave_link)](https://github.com/espressif/idf-extra-components/commits?path=esp_serial_slave_link) | [![GitHub License](https://img.shields.io/github/license/espressif/idf-extra-components)]()

**链接**：[idf-extra-components/esp_serial_slave_link at master · espressif/idf-extra-components](https://github.com/espressif/idf-extra-components/tree/master/esp_serial_slave_link)  
**特征**：ESP 旗下的串行从机链路，该组件能让主机通过总线驱动和相应的协议与从机进行通信。也可以说就是双 mcu 通讯，只是在上面套了一层壳。  

#### 要点

---

### SACP

[![GitHub Repo stars](https://img.shields.io/github/stars/Snapmaker/SnapmakerController-IDEX)](https://github.com/Snapmaker/SnapmakerController-IDEX/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/Snapmaker/SnapmakerController-IDEX?path=snapmaker/protocol)](https://github.com/Snapmaker/SnapmakerController-IDEX/commits?path=snapmaker/protocol) | [![GitHub License](https://img.shields.io/github/license/Snapmaker/SnapmakerController-IDEX)]()

**链接**：[SnapmakerController-IDEX/snapmaker/protocol at main · Snapmaker/SnapmakerController-IDEX](https://github.com/Snapmaker/SnapmakerController-IDEX/tree/main/snapmaker/protocol)  
**特征**：是 Snapmaker 设备的数据通信协议，基于 C++ 的专用于整机多设备的设备间通信。  

#### 要点

- 使用介绍：[一个可用于多设备间的 C/C++ 嵌入式通信协议的设计与实现-SACP 协议](https://mp.weixin.qq.com/s/Kj-9V5xJBlQQTgMj97O-Yw)
- 相关：[MVC 模式](./appendix.md#mvc-模式)

---
