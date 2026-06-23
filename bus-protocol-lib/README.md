# 总线协议与端侧库

> 该库包含非自定义的标准协议相关代码，除了基本的协议栈，对于简单的外设协议（iic、spi 等）提供 io 模拟及设备扫描自适应识别功能。  
>
> #### 设备扫描
>
> 通过软件扫描的方式可检测含有哪些硬件，硬件的 ID 是多少，意义重大，可用于在设备初始化时进行设备检查。  
>
> #### 自适应识别
>
> 自适应识别是基于设备扫描的基础上，很多时候一款产品的芯片类型拥有多种，可根据设备扫描后的信息进行自适应识别匹配，避免遗漏旧的硬件设备。  
> 值得一说的是，每一种自适应识别都不相同，例如 i2c 可以通过检测应答来判断设备地址，而串口的波特率则需要通过检测起始帧和结束帧的时间来判断。  

## UART

> 串口的模拟除了使用普通的 GPIO 进行高低电平的外，还可以使用 PWM 模拟发送，ADC 模拟接收，这样速度和准确性会更强。  

### LwOW

![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwow) | ![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwow) | ![GitHub License](https://img.shields.io/github/license/MaJerle/lwow)

**链接**：[LwOW latest-develop documentation — LwOW documentation](https://docs.majerle.eu/projects/lwow/en/latest/)  
**特征**：专业的 1-Wire 协议库，允许通过 UART 或单 GPIO 通讯，提供线程安全的 API。  

#### 要点

- 硬件进行时序控制。

---

### MUDLink

![GitHub Repo stars](https://img.shields.io/github/stars/jakeread/mudlink) | ![GitHub last commit](https://img.shields.io/github/last-commit/jakeread/mudlink) | ![GitHub License](https://img.shields.io/github/license/jakeread/mudlink)

**链接**：[jakeread/mudlink: Modular UART Duplex Link: cobs, crc, flow-control and delivery guarantees on any UART port in Arduino](https://github.com/jakeread/mudlink)  
**特征**：将UART串口提升为一个链路/传输层，并保证成帧数据包的交付，此外还传输保证和流量控制。它还记录链路性能的统计信息等功能。  

#### 要点

---

## CDbus

![GitHub Repo stars](https://img.shields.io/github/stars/dukelec/cdbus) | ![GitHub last commit](https://img.shields.io/github/last-commit/dukelec/cdbus) | ![GitHub License](https://img.shields.io/github/license/dukelec/cdbus)

> 是（Controller Distributed Bus）的缩写，意为控制器分布式总线。是一种简单的协议，基于串行总线而设计。相对于其他通信协议问题，解析 AT 命令很麻烦、Modbus 只支持单方向查询、PPP 协议要转义、字符串协议效率低等问题做了改进。文档：[cdbus_doc/intro_zh.md at master · dukelec/cdbus_doc](https://github.com/dukelec/cdbus_doc/blob/master/intro_zh.md)

### <a name="cdbus-project"></a>CDBUS

**链接**：[dukelec/cdbus: CDBUS (Controller Distributed Bus) Protocol and IP Core](https://github.com/dukelec/cdbus)  
**特征**：一种简单高效的现场总线，基于且兼容 UART / RS-485 协议和硬件，引入了硬件分包和硬件仲裁等机制，各节点可以自由收发数据包。  

#### 要点

- 提供的[CDNET](https://github.com/dukelec/cdnet)上层协议可以支持数据表读写、打印、IAP、波形显示等功能；
- 提供的[CDNET TUN](https://github.com/dukelec/cdnet_tun)扩展可以把简单的串口数据包映射成电脑 IP/UDP 数据包；

---

## Modbus

### freemodbus

![GitHub Repo stars](https://img.shields.io/github/stars/cwalter-at/freemodbus) | ![GitHub last commit](https://img.shields.io/github/last-commit/cwalter-at/freemodbus) | ![GitHub License](https://img.shields.io/github/license/cwalter-at/freemodbus)

**链接**：[cwalter-at/freemodbus: BSD licensed MODBUS RTU/ASCII and TCP slave](https://github.com/cwalter-at/freemodbus)  
**特征**：由 armink 移植的 modbus 协议栈，同时支持主机和从机的功能。  

#### 要点

- ESP 封装版：[espressif/esp-modbus: ESP-Modbus - the officially suppported library for Modbus protocol (serial RS485 + TCP over WiFi or Ethernet).](https://github.com/espressif/esp-modbus)

---

### nanoMODBUS

![GitHub Repo stars](https://img.shields.io/github/stars/debevv/nanoMODBUS) | ![GitHub last commit](https://img.shields.io/github/last-commit/debevv/nanoMODBUS) | ![GitHub License](https://img.shields.io/github/license/debevv/nanoMODBUS)

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

![GitHub Repo stars](https://img.shields.io/github/stars/armink/SFUD) | ![GitHub last commit](https://img.shields.io/github/last-commit/armink/SFUD) | ![GitHub License](https://img.shields.io/github/license/armink/SFUD)

**链接**：[armink/SFUD: An using JEDEC's SFDP standard serial (SPI) flash universal driver library | 一款使用 JEDEC SFDP 标准的串行 (SPI) Flash 通用驱动库](https://github.com/armink/SFUD)  
**特征**：开源的串行 SPI Flash 通用驱动库，通过编写设备表，做到能适配各型号Flash芯片。  

#### 要点

---

## USB

### TinyUSB

![GitHub Repo stars](https://img.shields.io/github/stars/hathach/tinyusb) | ![GitHub last commit](https://img.shields.io/github/last-commit/hathach/tinyusb) | ![GitHub License](https://img.shields.io/github/license/hathach/tinyusb)

**链接**：[TinyUSB](https://tinyusb.org)  
**特征**：是一个用于嵌入式系统的开源跨平台 USB 主机/设备堆栈，设计为内存安全，没有动态分配，线程安全，所有中断事件都被延迟，然后在非 ISR 任务函数中处理。  

#### 要点

---

### CherryUSB

![GitHub Repo stars](https://img.shields.io/github/stars/cherry-embedded/CherryUSB) | ![GitHub last commit](https://img.shields.io/github/last-commit/cherry-embedded/CherryUSB) | ![GitHub License](https://img.shields.io/github/license/cherry-embedded/CherryUSB)

**链接**：[GitHub - cherry-embedded/CherryUSB: Tiny and portable USB Stack (device & host) for embedded system with USB IP](https://github.com/cherry-embedded/CherryUSB)  
**特征**：移植性高的、用于嵌入式系统(带 USB IP)的 USB 主从协议栈。  

#### 要点

---

## Thread

### OpenThread

![GitHub Repo stars](https://img.shields.io/github/stars/openthread/openthread) | ![GitHub last commit](https://img.shields.io/github/last-commit/openthread/openthread) | ![GitHub License](https://img.shields.io/github/license/openthread/openthread)

**链接**：[OpenThread](https://openthread.io/?hl=zh-cn)  
**特征**：Google 旗下的产品，是Thread的开源实现。  

#### 要点

- 参考：[Thread - ESP32 - — ESP-IDF 编程指南 latest 文档](https://docs.espressif.com/projects/esp-idf/zh_CN/latest/esp32/api-reference/network/esp_openthread.html)  
  ESP的封装层：[esp-idf/components/openthread at be06a6f5ffe36f9554cfc91fe2036e0fc85fea60 · espressif/esp-idf](https://github.com/espressif/esp-idf/tree/be06a6f5ffe36f9554cfc91fe2036e0fc85fea60/components/openthread)；

---

## Bluetooth

### bluetooth\_stack

![GitHub Repo stars](https://img.shields.io/github/stars/sj15712795029/bluetooth_stack) | ![GitHub last commit](https://img.shields.io/github/last-commit/sj15712795029/bluetooth_stack) | ![GitHub License](https://img.shields.io/github/license/sj15712795029/bluetooth_stack)

**链接**：[sj15712795029/bluetooth_stack: 这是一个开源的双模蓝牙协议栈(bluetooth.stack)(btstack),可以运行在STM32,Linux.，包含HCI,L2CAP,SDP,RFCOMM,HFP,SPP,A2DP,AVRCP,AVDTP,AVCTP,OBEX,PBAP等协议，后续会继续维护，以达到商用的目的](https://github.com/sj15712795029/bluetooth_stack)  
**特征**：一个开源的低功耗双模蓝牙协议栈，可以用于学习，作者有很多教程。  

#### 要点

---

### BTstack

![GitHub Repo stars](https://img.shields.io/github/stars/bluekitchen/btstack) | ![GitHub last commit](https://img.shields.io/github/last-commit/bluekitchen/btstack) | ![GitHub License](https://img.shields.io/github/license/bluekitchen/btstack)

**链接**：[BlueKitchen – BlueKitchen GmbH | Qualified Dual-mode Bluetooth Stack – Available in Source Code](https://bluekitchen-gmbh.com/)  
**特征**：是一个轻量级、开源的 蓝牙协议栈，专为嵌入式系统和资源受限设备设计，适合需要低功耗、高灵活性的场景。  

#### 要点

---

### NimBLE

![GitHub Repo stars](https://img.shields.io/github/stars/apache/mynewt-nimble) | ![GitHub last commit](https://img.shields.io/github/last-commit/apache/mynewt-nimble) | ![GitHub License](https://img.shields.io/github/license/apache/mynewt-nimble)

**链接**：[apache/mynewt-nimble： Apache mynewt](https://github.com/apache/mynewt-nimble)  
**特征**：从Apache Mynewt中分离出来的一个开源的蓝牙协议栈（包括主机和控制器） 完全取代了 Nordic 芯片组上的专有 SoftDevice。  

#### 要点

- RT-Thread将其进行了修改并移植：[RT-Thread-packages/nimble: An Apache open-source Bluetooth 5.0 stack porting on RT-Thread](https://github.com/RT-Thread-packages/nimble)；

---

## TCP/IP

### lwIP

![License: BSD 2--Clause](https://img.shields.io/badge/license-BSD%202--Clause-blue.svg)

**链接**：[lwIP - A Lightweight TCP/IP stack - Summary [Savannah]](http://savannah.nongnu.org/projects/lwip/)  
**特征**：小型开源的TCP/IP协议栈，使用最广泛的嵌入式网络协议栈，基本上物联网系统中都有它。  

#### 要点

- 指南：[[野火]LwIP应用开发实战指南—基于STM32 — [野火]LwIP应用开发实战指南—基于野火STM32 文档](https://doc.embedfire.com/net/lwip/zh/latest/index.html)
- 官方文档：[lwIP: Overview](https://www.nongnu.org/lwip)；
- contrib包是移植和应用LwIP的一些demo；
- 源文件本体里的test文件夹不是demo示例，而是测试LwIP内核性能的源码，可以获得许多与LwIP内核性能有关的指标，只有非常专业的人士才用的到;
- 应用层不包含MQTT服务协议；
- 目录下各源文件  
  ```plaintext
  lwip
   ┣ contrib                # demo例程，大多内容来自开源社区的贡献
   ┣ doc                    # 相关文档和指南。
   ┣ src                    # 源码文件
   ┃ ┣ api                  # NETCONN API和Socket API相关的源文件，只适合操作系统环境
   ┃ ┣ apps                 # 应用程序的源文件，包括常见的应用程序，如httpd、mqtt、tftp、sntp、snmp等
   ┃ ┣ core                 # 内核源文件
   ┃ ┃ ┣ ipv4               # IPv4模块相关的源文件
   ┃ ┃ ┣ ipv6               # IPv6模块相关的源文件
   ┃ ┃ ┣ altcp_xxx.c        # 程序分层TCP连接API，从TCP/IP线程使用，是一个抽象层，可以模拟应用程序的tcp回调API
   ┃ ┃ ┣ def.c              # 包含一些基础类函数，比如主机序和网络序的转换、字符串的查找和比较、整数转换成字符串等
   ┃ ┃ ┣ dns.c              # 实现了域名解析的功能
   ┃ ┃ ┣ inet_chksum.c      # 提供校验所需的功能
   ┃ ┃ ┣ init.c             # 初始化函数，并且提供了对用户宏配置进行了检查的功能
   ┃ ┃ ┣ ip.c               # IP协议相关的函数，也就是封装了ipv4和ipv6文件夹中的函数
   ┃ ┃ ┣ mem.c              # 实现动态内存池管理机制  
   ┃ ┃ ┣ memp.c             # 实现静态内存堆管理机制
   ┃ ┃ ┣ netif.c            # 实现了网卡的操作
   ┃ ┃ ┣ pbuf.c             # 对网络数据包的各种操作，数据包以pbuf结构体的形式存在，是使用RAW/Callback API进行网络应用程序开发的关键
   ┃ ┃ ┣ raw.c              # 一个传输层协议的框架，我们可以在它的基础上修改和添加代码，实现自定义的传输层协议，与UDP/TCP一样，它可以与IP层直接进行交互。
   ┃ ┃ ┣ stats.c            # 提供内核的统计功能，可以实时地查看LwIP内核对网络数据包的处理情况
   ┃ ┃ ┣ sys.c              # 提供了与临界区相关的操作
   ┃ ┃ ┣ tcp_xxx.c          # 实现了TCP协议
   ┃ ┃ ┣ timeouts.c         # 定义了内核的超时处理机制
   ┃ ┃ ┗ udp.c              # 实现了UDP协议
   ┃ ┣ include              # 所有模块对应的头文件
   ┃ ┗ netif                # 不同网卡的移植模板
   ┣ test                   # 测试内核性能的源码，只有非常专业的人士才用的到
   ┗ other                  # 迭代日记、许可证、简介等
  ```

---

### CycloneTCP

![License: GPL v2](https://img.shields.io/badge/license-GPL%20v2-orange.svg)

**链接**：[CycloneTCP | Embedded TCP/IP Stack for STM32, PIC32, ARM Cortex-M](https://www.oryx-embedded.com/products/CycloneTCP)  
**特征**：专用于嵌入式应用的双 IPv4/IPv6 栈，简化了互联网的部署。  

#### 要点

- 商用需授权；

---

### onps

![Gitee Repo stars](https://gitee.com/Neo-T/open-npstack/badge/star.svg?theme=gvp) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Neo-T/open-npstack&query=$.pushed_at&label=last%20commit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Neo-T/open-npstack&query=$.license&label=license)

**链接**：[Open-NPStack: onps是一个开源且完全自主开发的国产网络协议栈。设计目标与LwIp相同，onps栈的目标系统同样是资源受限的单片机系统。提供完整的tcp/ip协议族实现，同时提供sntp、dns、ping等网络工具，支持以太网环境下dhcp动态ip地址申请，也支持动态及静态路由表。协议栈还封装实现了一个伯克利套接字（Berkeley sockets）层。协议栈使用ANSI C语言开发。](https://gitee.com/Neo-T/open-npstack)  
**特征**：国产网络协议栈，设计目标与Lwip相同，适用于资源受限的单片机系统，提供完整地ethernet/ppp/tcp/ip协议族实现。  

#### 要点

---

## GNSS

> [ESA欧空局对相关开源项目的汇总](https://www.esa.int/Enabling_Support/Space_Engineering_Technology/Radio_Frequency_Systems/Open_Source_Software_Resources_for_Space_Downstream_Applications%20#Table1)

### LwGPS

![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwgps) | ![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwgps) | ![GitHub License](https://img.shields.io/github/license/MaJerle/lwgps)

**链接**：[LwGPS latest-develop documentation — LwGPS documentation](https://docs.majerle.eu/projects/lwgps/en/latest/)  
**特征**：简易的 NMEA 报文解析库，内置支持 4 个 GPS 报文：GPGGA、GPGSA、GPGSV、GPRMC，以及允许自定义报文。  

#### 要点

---

### RTKLIB

![GitHub Repo stars](https://img.shields.io/github/stars/tomojitakasu/RTKLIB) | ![GitHub last commit](https://img.shields.io/github/last-commit/tomojitakasu/RTKLIB) | ![GitHub License](https://img.shields.io/github/license/tomojitakasu/RTKLIB)

**链接**：[GitHub - tomojitakasu/RTKLIB · GitHub](https://github.com/tomojitakasu/RTKLIB)  
**针对低成本 GNSS 接收器版本**：[GitHub - rtklibexplorer/RTKLIB: A version of RTKLIB optimized for low cost GNSS receivers, especially u-blox receivers. It is based on RTKLIB 2.4.3. This software is provided “AS IS” without any warranties of any kind so please be careful, especially if using it in any kind of real-time application. Click on the "Releases" label below to see the latest Windows pre-release. · GitHub](https://github.com/rtklibexplorer/RTKLIB)  
**针对智能手机 GNSS 芯片的优化版本**：[GitHub - salmoshu/MobileGNSS-SPP: An EKF-based SPP system optimized for smartphone · GitHub](https://github.com/salmoshu/MobileGNSS-SPP)  
**特征**：RTK领域的标杆库，广泛应用于商业以及社区，同时也是教科书式的参考手册。  

#### 要点

- *src* 目录下各源文件的主要作用说明：  
  ```plaintext
  src
  ├── rcv                # 专用于解析不同品牌GNSS接收机的专有二进制格式
  │   ├── binex.c        # 解码BINEX（Binary Exchange）通用格式数据
  │   ├── crescent.c     # 解码Crescent接收机数据
  │   ├── javad.c        # 解码JAVAD接收机数据
  │   ├── novatel.c      # 解码NovAtel接收机二进制格式（如OEM4/5/6/7）
  │   ├── nvs.c          # 解码NVS接收机数据
  │   ├── rt17.c         # 解码Trimble RT17/RT27格式数据
  │   ├── septentrio.c   # 解码Septentrio接收机数据
  │   ├── skytraq.c      # 解码SkyTraq接收机数据
  │   ├── ss2.c          # 解码NovAtel Superstar II接收机数据
  │   └── ublox.c        # 解码u-blox接收机UBX二进制格式
  ├── convgpx.c          # 将定位结果转换为GPX格式
  ├── convkml.c          # 将定位结果转换为KML（Google Earth）格式
  ├── convrnx.c          # RINEX格式转换工具（如压缩、版本转换）
  ├── datum.c            # 大地基准面转换参数与函数
  ├── download.c         # 自动从网络（FTP/HTTP）下载精密星历、电离层产品等文件
  ├── ephemeris.c        # 广播星历的计算（卫星位置、速度、钟差）
  ├── geoid.c            # 大地水准面模型（如EGM96）计算，用于高程转换
  ├── gis.c              # 地理信息系统相关辅助函数（如坐标投影变换）
  ├── ionex.c            # IONEX格式电离层TEC地图的读取与插值
  ├── lambda.c           # LAMBDA方法实现，用于整周模糊度快速搜索与固定
  ├── options.c          # 命令行和配置文件的参数解析与处理
  ├── pntpos.c           # 单点定位模块，计算接收机近似位置、钟差，并为高精度定位提供初始值
  ├── postpos.c          # 后处理定位主程序，协调数据读取、解算和结果输出流程
  ├── ppp.c              # 精密单点定位（PPP）算法实现
  ├── ppp_ar.c           # PPP的模糊度固定（PPP-AR）算法
  ├── preceph.c          # 精密星历（SP3格式）的读取与插值计算
  ├── rcvraw.c           # 原始观测数据读取与接口管理，调用rcv/目录下的具体解码器
  ├── rinex.c            # RINEX格式（观测值/导航电文）的读取与生成
  ├── rtcm.c             # RTCM公共函数及版本兼容接口
  ├── rtcm2.c            # RTCM SC-104版本2.x差分数据编解码
  ├── rtcm3.c            # RTCM SC-104版本3.x差分数据编解码（基础）
  ├── rtcm3e.c           # RTCM 3.x的扩展消息支持（如MSM）
  ├── rtkcmn.c           # 公共函数库
  ├── rtklib.h           # 主头文件（定义所有结构体、常量、函数原型）
  ├── rtkpos.c           # RTK定位核心引擎，调用pntpos、relpos等实现实时/后处理定位解算
  ├── rtksvr.c           # RTK服务器核心，处理多基准站输入、生成差分改正数并播发
  ├── sbas.c             # SBAS（星基增强系统）数据解析与改正量应用
  ├── solution.c         # 解算结果的管理、滤波和输出格式化
  ├── stream.c           # 数据流处理（串口、TCP/IP、NTRIP、文件读写）
  ├── streamsvr.c        # 流服务器功能，支持多客户端连接和数据转发
  ├── tides.c            # 地球潮汐改正（固体潮、海潮、极潮）
  └── tle.c              # TLE两行轨道元素解析，用于低精度卫星位置计算（主要对GLONASS）
  ```
- 基于RTKLIB衍生的项目及学习研究：[rtkexplorer – Exploring low cost solutions for high precision GPS/GNSS](https://rtkexplorer.com/)
- 该库的中文翻译及使用讲解：[Winchell](https://salmoshu.github.io/)

---

### Ntrip

![GitHub Repo stars](https://img.shields.io/github/stars/ybzwyrcld/ntrip) | ![GitHub last commit](https://img.shields.io/github/last-commit/ybzwyrcld/ntrip) | ![GitHub License](https://img.shields.io/github/license/ybzwyrcld/ntrip)

**链接**：[GitHub - ybzwyrcld/ntrip: Simple ntrip caster/client/server example programs, using the NTRIP2.0 protocol](https://github.com/ybzwyrcld/ntrip)  
**特征**：C++编写的简易Ntrip协议库，包含流动站（Client）<sup>(Rover)</sup>、中央服务器（Caster）、基准站（CORS）<sup>(Server)</sup>。  

#### 要点

---
