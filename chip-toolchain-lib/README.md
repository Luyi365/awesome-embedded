# 芯片和工具链适配库

> 对某单一类型芯片或指定工具链进行的支持库，一般厂商会提供 SDK 来做这些事。但对于一些太过于老旧的芯片则由网友们提供收集。

## 51

### 8051-ELL

**链接**：[MCS51-ELL: 这是一个专门为增强型1T8051内核MCU设计的硬件抽象平台。](https://gitee.com/gevico/mcs51-ell)  
**特征**：结合了 HAL 库和 LL 库的编程思想编写的 ELL(efficient low-layer)库，以 STC8 系列为主。  

#### 要点

---

### ECBM

**链接**：[基于 STC8 系列的 ECBM 函数库 V3: 该库为 ECBM 的发行版的 V3 版本，是基于 STC8 单片机的外设函数库，目前已经支持 STC8 全型号。外设部分会逐渐完善，同时由于 stc8 型号众多，不能一一实机测试，如有不适配的型号请留言。 STC8 是目前 51 单片机里最好用的系列，拥有最多 8K 的 SRAM、64K 的 Flash、5 个定时器、4 个串口。全系列都带 IIC 和 SPI，大部分带 ADC。STC8H 还带有硬件 USB。](https://gitee.com/ecbm/ecbm_library)  
**ECBM 库精简版**：[ECBM 库精简版: 在推广 ECBM 库 V3 的过程中，不止一次的听说 ECBM 占用空间太大了，然后新手对库不了解就不知道怎么优化，于是就干脆不用了。这回我专门推出官方优化精简版！在保证了 ecbm 特色的情况下，去除大量用不到的鸡肋功能，只为了核心和精简而存在的 STC8 库。](https://gitee.com/ecbm/ecbm-library-lite)  
**特征**：全中文注解的外设函数库，简单易用。  

#### 要点

- 精简库比标准库少了例子和 device 层。

---

## AVR

---

## ST

### STM32F4 Discovery

**链接**：[MaJerle/stm32f429: Keil projects and libraries for STM32F4xx devices](https://github.com/MaJerle/stm32f429)  
**特征**：面向STM32F4系列微控制器的驱动库集合，包含多个外设、接口的实现教学及配套示例。  

#### 要点

---

## ESP

### LwESP

**链接**：[LwESP latest-develop documentation — LwESP documentation](https://docs.majerle.eu/projects/lwesp/en/latest/)  
**特征**：AT 解析器库，旨在其他设备通过 AT 命令与 ESP 设备进行通信。  

#### 要点

- 支持乐鑫的 AT 软件；
- 目前仅支持操作系统模式；

---

### ESPUI

**链接**：[s00500/ESPUI: A simple web user interface library for ESP32 and ESP8266](https://github.com/s00500/ESPUI)  
**特征**：为 ESP32 和 ESP8266 设备设计的简单的网络用户界面库。它使用户能够轻松地创建和管理设备的 Web 界面，无需任何 HTML、CSS 或 JavaScript 前端开发知识。  

#### 要点

---

### FluidNC

**链接**：[bdring/FluidNC: The next generation of motion control firmware](https://github.com/bdring/FluidNC)  
**特征**：针对 ESP32 控制器优化的 CNC 固件库。  

#### 要点

---

### Rabbit GRBL

**链接**：[SourceRabbit/RabbitGRBL: Professional grade, 100% GRBL compatible motion control firmware for the ESP32](https://github.com/SourceRabbit/RabbitGRBL)  
**特征**：运行在 ESP32 处理器上的 CNC 固件库，经过高度优化，能够保持高达 120khZ 的稳定、无抖动的控制脉冲。  

#### 要点

---

## SIMCom

### LwCELL

**链接**：[LwCELL latest-develop documentation — LwCELL documentation](https://docs.majerle.eu/projects/lwcell/en/latest/)  
**特征**：用于控制 SIMCom 的 SIM800 / SIM900 或 SIM7000 / SIM7020（NB-Iot LTE）设备。  

#### 要点

---

## MDK

### flash\_blob

**链接**：[Aladdin-Wang/flash_blob: 一个适配几乎任意单片机型号的flash驱动](https://github.com/Aladdin-Wang/flash_blob)  
**特征**：利用MDK的FLM文件快速生成通用flash驱动。  

#### 要点

- 使用介绍：[利用MDK的FLM文件生成通用flash驱动-CSDN博客](https://blog.csdn.net/sinat_31039061/article/details/128350295)

---

## Driver

### LibDriver

**链接**：[libdriver (LibDriver)](https://github.com/libdriver)  
**特征**：一个开源的驱动开发组织，包含了所有常用的外设模块驱动库（140+）。  

#### 要点

---
