# Awesome-Embedded

[![GitHub last commit](https://img.shields.io/github/last-commit/Luyi365/Awesome-Embedded)](https://github.com/Luyi365/Awesome-Embedded/commits)

## 🚀关于

> 一个精心整理的嵌入式开源代码库集合，并按照功能进行了细致的分类，涵盖了💥**绝大部分** 的开发场景！
> 与大多数[awesome](https://github.com/sindresorhus/awesome)库不同的是：除了对相关代码库进行收集整理，还对部分库的**使用要点**进行了记录📝。

一个好的开源项目是社区共同努力的结果🤗，如果下面有你感兴趣的部分，十分欢迎大家通过 Issues 进行留言：

- 推荐或自荐好的嵌入式开源库（甚至代码片段也可以）；
- 为已记录的开源库编写使用心得（好的入门教程、踩过的大坑……总之你想让大家知道关于库的一些什么）；
- 文档中存在的错误以及一些建议（我们会积极对待任何好的想法）；

<ins>分类细则&其他汇总库可查看[✨额外](#额外)部分。</ins>

#### TODO

- [x] 增加许可证信息；
- [x] 审查链接的有效性
- [ ] 优化排版及格式
- [ ] 考虑增加英文说明
- [ ] 重写部分库的使用要点（最初是给我自己看的，所以有些内容是建立在已知的情况下而写，需要优化）

---

## [IO与PWM库](./io-pwm-lib/README.md#io与pwm库)

### [按键](./io-pwm-lib/README.md#按键)

- ~~[key_detect](./io-pwm-lib/README.md#key_detect)：简易的按键检测组件，采用注册事件，提供最基本的按键功能。~~（待发布）
- [key_module](./io-pwm-lib/README.md#key_module)：简单易用的按键检测模块，采用事件回调，提供除矩阵按键的其他基本功能。
- [FlexibleButton](./io-pwm-lib/README.md#flexiblebutton)：超轻量的按键库，采用轮询扫描检测，简单易用。
- [MultiButton](./io-pwm-lib/README.md#multibutton)：标准的按键库，每个按键结构以面向对象的思想单独管理。
- [cotKey](./io-pwm-lib/README.md#cotkey)：监听型按键识别库，可以实现单击、双击、多击、短按和长按等多种要求的功能，但只支持单一按键功能。
- [key_board](./io-pwm-lib/README.md#key_board)：极丰富的按键库，带有矩阵键盘和组合的功能。
- [LwBTN](./io-pwm-lib/README.md#lwbtn)：专业的按键事件管理库，配置方面十分丰富，但有点晦涩难懂。

### [LED](./io-pwm-lib/README.md#led)

- [cotLed](./io-pwm-lib/README.md#cotled)：轻量级的 LED 控制模块，可以实现 LED 灯多种模式状态。
- [led_module](./io-pwm-lib/README.md#led_module)：基于面向对象和简单工厂模式的通用 LED 显示模块。

---

## [TIMER与TIME库](./timer-time-lib/README.md#timer与time库)

### [定时器](./timer-time-lib/README.md#定时器)

- [MultiTimer](./timer-time-lib/README.md#multitimer)：模拟的软件定时器模块，取代传统的标志位判断方式，操作与硬件定时器几乎一致。
- [SmartTimer](./timer-time-lib/README.md#smarttimer)：裸机下十分好用的定时器调度器，除了基本轮询回调外，还可以设置轮询次数。
- [microseconds](./timer-time-lib/README.md#microseconds)：基于 Cortex-M 内核的 SysTick 做的微秒级别定时器库，有阻塞和非阻塞延迟。一般的厂商都有提供定时器函数，这个主要针对芯片、定时器模块需要更换的场景。
- [perf_counter](./timer-time-lib/README.md#perf_counter)：基于 Cortex-M 内核的 SysTick，不仅拥有基本的定时器功能，还具有代码段的周期测量、定时服务等功能，且支持 RTOS。代码看起来复杂，适合公司级项目。

### [看门狗](./timer-time-lib/README.md#看门狗)

- [LwWDG](./timer-time-lib/README.md#lwwdg)：轻量级的看门狗库，主要针对操作系统， 监视多个线程并在其中一个线程失败时重置系统。

### [TIME 相关](./timer-time-lib/README.md#time-相关)

- [LwDTC](./timer-time-lib/README.md#lwdtc)：用于日期、时间和 cron 实用程序库，支持 tm 数据结构，解析速度快。

---

## [内存与文件系统库](./mem-fs-lib/README.md#内存与文件系统库)

### [内存管理](./mem-fs-lib/README.md#内存管理)

- [memory](./mem-fs-lib/README.md#memory)：功能极简的内存管理模块，仅提供内存申请与释放，无其他额外功能。
- [mem_malloc](./mem-fs-lib/README.md#mem_malloc)：简单实用的内存管理模块，不会产生内存碎片。
- [tlsf](./mem-fs-lib/README.md#tlsf：tlsf)：TLSF 算法的堆内存分配库，支持动态添加、删除内存池区域，分配时间复杂度为 O(1)，不注重线程安全。
- [LwMEM](./mem-fs-lib/README.md#lwmem)：专业内存管理库，允许使用碎片内存，注重 RTOS 的线程安全。
- [jemalloc](./mem-fs-lib/README.md#jemalloc)：高性能的内存分配器，适合处理多线程环境下大规模内存分配和释放的场景。
- [LWMalloc](./mem-fs-lib/README.md#lwmalloc)：适用于 Linux 的轻量级动态内存分配器，旨在替代默认分配器 ptmalloc，性能和内存使用量都更优。

### [读写封装层](./mem-fs-lib/README.md#读写封装层)

- [flashMultipleErase](./mem-fs-lib/README.md#flashmultipleerase)：用 FLASH 模拟 EEPROM，采用顺序写入的方法，以实现高达 100 万次以上的存储次数。
- [eepromfs](./mem-fs-lib/README.md#eepromfs)：基于 EEPROM 的简易类文件数据读写库，它并不属于真正的文件系统，只是把数据读写模拟成文件的方式。
- [Dhara](./mem-fs-lib/README.md#dhara)：用于小型单片机的 NAND 闪存转换层(FTL)。主要用来对 FLASH 读、写、抹除操作的管理。处于 FLASH 设备与文件系统层之间。
- [kFlashFile](./mem-fs-lib/README.md#kflashfile)：基于 NOR Flash 的轻量级文件数据存储方案，主要用于需要断电数据保存的项目。
- [esp_partition](./mem-fs-lib/README.md#esp_partition)：ESP 旗下的分区表库，允许以块为单位访问 flash。
- [NVS](./mem-fs-lib/README.md#nvs)：ESP 旗下的非易失性存储库，主要用于在 flash 中存储键值格式的数据。配合 ESP 旗下的其他工具，支持加密、生成分区镜像等功能。

### [文件系统](./mem-fs-lib/README.md#文件系统)

- [FatFs](./mem-fs-lib/README.md#fatfs)：赫赫有名的文件系统库，极易移植，支持 exFAT 文件系统、64 位 LBA 和 GPT，可根据功能进行宏配置，注重线程安全。
- [JesFs](./mem-fs-lib/README.md##jesfs)：专为资源受限的嵌入式系统设计的轻量级串行 NOR 闪存文件系统，适用于各种物联网应用场景，例如数据采集、事件记录和固件更新等。
- [RanFs](./mem-fs-lib/README.md#ranfs)：轻量型文件系统模块，提供 POSIX 兼容的文件操作，注重高效和数据可靠性。
- [littlefs](./mem-fs-lib/README.md#littlefs)：专为微处理器设计的安全文件系统，具有掉电保护、擦写均衡、低资源消耗等功能。
- [SPIFFS](./mem-fs-lib/README.md#spiffs)：专为低内存（<=128MB）而设计文件系统，使用静态大小的 ram 缓冲区，具有擦写均衡等功能。

---

## [总线协议与端侧库](./bus-protocol-lib/README.md#总线协议与端侧库)

### [UART](./bus-protocol-lib/README.md#uart)

- [LwOW](./bus-protocol-lib/README.md#lwow)：专业的 1-Wire 协议库，允许通过 UART 或单 GPIO 通讯，提供线程安全的 API。
- [MUDLink](./bus-protocol-lib/README.md#mudlink)：将 UART 串口提升为一个链路/传输层，并保证成帧数据包的交付，此外还传输保证和流量控制。它还记录链路性能的统计信息等功能。

### [CDbus](./bus-protocol-lib/README.md#cdbus)

- [CDBUS](./bus-protocol-lib/README.md#cdbus-project)：一种简单高效的现场总线，基于且兼容 UART / RS-485 协议和硬件，引入了硬件分包和硬件仲裁等机制，各节点可以自由收发数据包。

### [Modbus](./bus-protocol-lib/README.md#modbus)

- [freemodbus](./bus-protocol-lib/README.md#freemodbus)：由 armink 移植的 modbus 协议栈，同时支持主机和从机的功能。
- [nanoMODBUS](./bus-protocol-lib/README.md#nanomodbus)：精简的 modbus 库，可按需裁剪功能，旨在资源有限的环境中运行。

### [I2C](./bus-protocol-lib/README.md#i2c)

- ~~[i2c_scanner](./bus-protocol-lib/README.md#i2c_scanner)：i2c 设备扫描库，摘自 Nordic 的 SDK 库，能够扫描板载的 i2c 设备个数及设备地址。~~(待发布)

### [SPI](./bus-protocol-lib/README.md#spi)

- [SFUD](./bus-protocol-lib/README.md#sfud)：开源的串行 SPI Flash 通用驱动库，通过编写设备表，做到能适配各型号 Flash 芯片。

### [USB](./bus-protocol-lib/README.md#usb)

- [TinyUSB](./bus-protocol-lib/README.md#tinyusb)：是一个用于嵌入式系统的开源跨平台 USB 主机/设备堆栈，设计为内存安全，没有动态分配，线程安全，所有中断事件都被延迟，然后在非 ISR 任务函数中处理。
- [CherryUSB](./bus-protocol-lib/README.md#cherryusb)：用于嵌入式系统(带 USB IP)的 USB 主从协议栈。可以移植各个平台，适用于自身不带 USB 协议栈的芯片。

### [Thread](./bus-protocol-lib/README.md#thread)

- [OpenThread](./bus-protocol-lib/README.md#openthread)：Google 旗下的产品，是 Thread 的开源实现。

### [Bluetooth](./bus-protocol-lib/README.md#bluetooth)
- [bluetooth_stack](./bus-protocol-lib/README.md#bluetooth_stack)：一个开源的低功耗双模蓝牙协议栈，可以用于学习，作者有很多教程。
- [BTstack](./bus-protocol-lib/README.md#btstack)：是一个轻量级、开源的 蓝牙协议栈，专为嵌入式系统和资源受限设备设计，适合需要低功耗、高灵活性的场景。
- [NimBLE](./bus-protocol-lib/README.md#nimble)：从 Apache Mynewt 中分离出来的一个开源的蓝牙协议栈（包括主机和控制器） 完全取代了 Nordic 芯片组上的专有 SoftDevice。

### [TCP/IP](./bus-protocol-lib/README.md#tcpip)
- [lwIP](./bus-protocol-lib/README.md#lwip)：小型开源的 TCP/IP 协议栈，使用最广泛的嵌入式网络协议栈，基本上物联网系统中都有它。
- [CycloneTCP](./bus-protocol-lib/README.md#cyclonetcp)：专用于嵌入式应用的双 IPv4/IPv6 栈，简化了互联网的部署。
- [onps](./bus-protocol-lib/README.md#onps)：国产网络协议栈，设计目标与 Lwip 相同，适用于资源受限的单片机系统，提供完整地 ethernet/ppp/tcp/ip 协议族实现。有非常详细的介绍，很适合国人读阅。

### [GNSS](./bus-protocol-lib/README.md#gnss)

- [LwGPS](./bus-protocol-lib/README.md#lwgps)：简易的 NMEA 报文解析库，内置支持 4 个 GPS 报文：GPGGA、GPGSA、GPGSV、GPRMC。
- [RTKLIB](./bus-protocol-lib/README.md#rtklib)：RTK 领域的标杆库，广泛应用于商业以及社区，同时也是教科书式的参考手册。
- [Ntrip](./bus-protocol-lib/README.md#ntrip)：C++ 编写的简易 Ntrip 协议库，包含流动站（Client）、中央服务器（Caster）、基准站（CORS）。

---

## [数据库与格式解析（传输协议）库](./db-format-parser-lib/README.md#数据库与格式解析（传输协议）库)

### [数据库](./db-format-parser-lib/README.md#数据库)

- [cotParam](./db-format-parser-lib/README.md#cotParam)：采用表驱动方式进行参数管理，包括缺省值、最小值和最大值等。
- [EasyFlash](./db-format-parser-lib/README.md#easyflash)：Key-Value 型简易数据库，主要提供：变量的 KV 配对，可 IAP 数据修改（可用于升级），log 存储等功能。
- [FlashDB](./db-format-parser-lib/README.md#flashdb)：提供 KV 和 TS 两种数据库，比起 EasyFlash 更专注于数据库本身，而不提供过多的额外功能。
- [Nanopb](./db-format-parser-lib/README.md#nanopb)：轻量的、支持 C 语言的 Protobuf，Protobuf 是 Google 公司开发的一种数据格式。可用于数据存储、通信协议等方面，且不依赖于语言和平台，也就是说可以不同设备端进行数据通讯。
- [ITTIA DB](./db-format-parser-lib/README.md#ittia-db)：功能强大的实时嵌入式数据库，主要用于嵌入式系统和物联网设备，用于在设备上本地监控，存储和分析时间序列数据，需要商业许可。
- [linq4c](./db-format-parser-lib/README.md#linq4c)：在 C 语言里实现了 C# 的 linq 方法。
- [SQLite](./db-format-parser-lib/README.md#sqlite)：业界用的最多的嵌入式标准的数据库，使用 SQL 语法，可使用磁盘文件。

### [数据流](./db-format-parser-lib/README.md#数据流)

- ~~[uart_stream](./db-format-parser-lib/README.md#uart_stream)：数据流缓冲处理库，针对 UART 数据，但有一定的通用性。~~（待发布）
- [xprintf](./db-format-parser-lib/README.md#xprintf)：嵌入式字符串函数，代替不足以实现常规 printf 功能，可以动态的将字符串写入不同外设。主要用途是与多个外设交互，而不是终端交互
- [CMSIS-Stream](./db-format-parser-lib/README.md#cmsis-stream)：ARM 官方出品的数据流处理组件，提供图形表示，适合专业级项目和多设备数据流处理。

### [压缩库](./db-format-parser-lib/README.md#压缩库)

- [lz4](./db-format-parser-lib/README.md#lz4)：极快的无损压缩算法库，适合通信时的数据压缩。
- [heatshrink](./db-format-parser-lib/README.md#heatshrink)：超低资源消耗的嵌入式解压缩库。相关文档较少。
- [TJpgDec](./db-format-parser-lib/README.md#tjpgdec)：针对嵌入式系统优化的 JPEG 图像解压缩模块。

### [URL](./db-format-parser-lib/README.md#url)

- [url](./db-format-parser-lib/README.md#url-project)：简单的解析 url 模块，可以解析不同段的信息。

### [SSH](./db-format-parser-lib/README.md#ssh)

- [tinyssh](./db-format-parser-lib/README.md#tinyssh)：一个简约的 SSH 服务器，它只实现了 SSHv2 功能的子集，适合嵌入式使用。

### [MQTT](./db-format-parser-lib/README.md#mqtt)

- [Paho MQTT](./db-format-parser-lib/README.md#paho-mqtt)：嵌入式平台的 MQTT 客户端库。
- [mqttclient](./db-format-parser-lib/README.md#mqttclient)：高性能、高稳定性的跨平台 MQTT 客户端，拥有简洁的 API，无缝衔接 Mbed TLS 库，提供在线代码生成工具。
- [Mosquitto](./db-format-parser-lib/README.md#mosquitto)：Eclipse 旗下的一个开源的消息代理（broker），主要用于实现 MQTT 协议。它设计轻巧，资源占用少，适合物联网领域的企业级项目。

### [AT](./db-format-parser-lib/README.md#at)

- [AT Command](./db-format-parser-lib/README.md#at-command)：AT 命令通信解析模块，适用于 Modem、WIFI 模块、蓝牙等使用 AT 命令或者 ASCII 命令行通信的场景。
- [Xradio_atcmd](./db-format-parser-lib/README.md#xradio_atcmd)：Xradio SDK 里提取的 AT 命令解析库，命令实例丰富，基于 RTOS。

### [Base64](./db-format-parser-lib/README.md#base64)

- [base64](./db-format-parser-lib/README.md#base64-project1)：极简单的 base64 编解码库。
- [base64](./db-format-parser-lib/README.md#base64-project2)：支持 SIMD 和 OpenMP 加速的 base64 编解码库，不使用动态内存，注重线程安全。

### [CSV](./db-format-parser-lib/README.md#csv)

- [MiniCSV](./db-format-parser-lib/README.md#minicsv)：极简的 CSV 解析库，能够解决多行、转义行、转义列中的转义字符、空行、列数可变的行、Windows 或 Unix 风格的行结尾等问题。
- [CRStrLib](./db-format-parser-lib/README.md#crstrlib)：解析 csv 格式/其他格式的字符串， 提取数值，帧头帧尾校验。
- [fast-cpp-csv-parser](./db-format-parser-lib/README.md#fast-cpp-csv-parser)：基于 C++ 的 CSV 解析器，小型、易于使用且快速的仅标头库。

### [INI](./db-format-parser-lib/README.md#ini)
- [libinimini](./db-format-parser-lib/README.md#libinimini)：适用单片机的 ini 极简解析库，内存空间占用可控。最简单的键值配对文件格式。
- [inih](./db-format-parser-lib/README.md#inih)：基于 C 编写的 ini 解析库，适合嵌入式系统。带有语法与解析选项。
- [iniparser](./db-format-parser-lib/README.md#iniparser)：基于 C 编写的 ini 解析库，可移植嵌入式系统，注重线程安全。

### [TLV](./db-format-parser-lib/README.md#tlv)
- ~~[ITLV](./db-format-parser-lib/README.md#itlv)：TLV（Tag、Length、Value）格式数据的优化版本，极简轻量的数据传输格式，可以以此为基础自定义数据格式，附带 CRC 检验。~~（待发布）
- [TLV](./db-format-parser-lib/README.md#tlv-project)：TLV 格式编码实现。

### [JSON](./db-format-parser-lib/README.md#json)
- [cJSON](./db-format-parser-lib/README.md#cjson)：ANSI C 中的超轻量级 JSON 解析器，也是最原生的 JSON 解析库，用起来会有点麻烦，不太推荐直接使用。
- [struct2json](./db-format-parser-lib/README.md#struct2json)：基于 cJSON，超简便的 C 结构体与 JSON 快速互转库。
- [cson](./db-format-parser-lib/README.md#cson)：基于 cJSON，运行于 C 语言平台的 json-struct 模型解析工具。使 JSON 解析更加方便。
- [json](./db-format-parser-lib/README.md#json-project)：简单高效的 C 语言 json 生成和解析库，适合简单项目的使用。
- [JSMN](./db-format-parser-lib/README.md#jsmn)：超简约、极快的 JSON 解析器，无动态内存分配，无解析纠正。适合小型项目的 JSON 解析。
- [lwjson](./db-format-parser-lib/README.md#lwjson)：针对嵌入式系统优化的通用 JSON 解析器库。适合厂商项目的 JSON 解析。
- [MojoJson](./db-format-parser-lib/README.md#mojojson)：通用的 JSON 解析库，采用面向对象的思想实现，提供 C 语言版本。
- [LJSON](./db-format-parser-lib/README.md#LJSON)：号称最快的 JSON 解析库，功能极为强大，几乎覆盖了 JSON 解析的所有需要。
- [json-parser](./db-format-parser-lib/README.md#json-parser)：简单、规范、实用的 JSON 库，包括解析和生成。
- [Frozen](./db-format-parser-lib/README.md#frozen)：类似 scanf/printf 的 JSON 解析和生成库，内置 base64 编码器和二进制数据解码器。
- [sj.h](./db-format-parser-lib/README.md#sjh)：极简的 C 语言 JSON 解析库，采用零拷贝策略，直接在原数据上解析。

### [XML](./db-format-parser-lib/README.md#xml)
- [simple_xml](./db-format-parser-lib/README.md#simple_xml)：XML 解析库，具有完备的功能，支持双向解析。
- [TinyXML-2](./db-format-parser-lib/README.md#tinyxml-2)：基于 C++ 的 XML 解析库，它使用文档对象模型（DOM），可以很方便的将 XML 和 C++ 对象互相加息转换。

### [TOML](./db-format-parser-lib/README.md#toml)
- [TOML](./db-format-parser-lib/README.md#toml-project)：比 INI 的扩展性强、又没有层层嵌套的 JSON 和 YAML 的缩进语法，一种人们不常了解的数据标记格式。

### [其他](./db-format-parser-lib/README.md#其他)
- [LwPKT](./db-format-parser-lib/README.md#lwpkt)：通用数据包协议库，可变数据长度，支持理论上无限的数据包长度，允许在网络中使用发件人地址和收件人地址进行多个注释，附带 CRC 检验。
- [xpack](./db-format-parser-lib/README.md#xpack)：用于在 C++ 结构体和 json/xml/yaml/bson/mysql/sqlite 之间互相转换，仅有头文件。
- [ESSL](./db-format-parser-lib/README.md#essl)：ESP 旗下的串行从机链路，该组件能让主机通过总线驱动和相应的协议与从机进行通信。也可以说就是双 mcu 通讯，只是在上面套了一层壳。
- [Uart_Transfer_BIN_to_exFlash](./db-format-parser-lib/README.md#uart_transfer_bin_to_exflash)：基于串口通讯，增加帧属性，从而方便、可靠的将数据传输到 Flash 中。
- [SACP](./db-format-parser-lib/README.md#sacp)：是 Snapmaker 设备的数据通信协议，基于 C++ 的专用于整机多设备的设备间通信。
- [rtty](./db-format-parser-lib/README.md#rtty)：通过 Web 访问设备的终端，适合嵌入式 Linux，有点意思。
- [Nanomsg](./db-format-parser-lib/README.md#nanomsg)：是一个“可扩展协议”的套接字库，它提供了几种常见的通信模式。可扩展协议的任务是定义多个应用系统如何通信，从而组成一个大的分布式系统。

---

## [日志与终端交互库](./log-term-lib/README.md#日志与终端交互库)

### [LOG 日志](./log-term-lib/README.md#log-日志)

- [dbuglib](./log-term-lib/README.md#dbuglib)：精小的的日志库，仅提供输出显示功能，可以修改日志的级别用于过滤特定级别的日志，相当于一般 SDK 自带的 printf 功能；
- [log.c](./log-term-lib/README.md#logc)：极简的日志库，仅提供输出显示和记录功能。基于 C99 标准，不太适用于嵌入式领域。
- [log](./log-term-lib/README.md#log)：小巧的日志模块，输出内容包括时间、日志类型、内容、文件名、行号、函数名等信息。
- [alog](./log-term-lib/README.md#alog)：功能精简的输出日志组件，带颜色带互斥锁。
- [LwPRINTF](./log-term-lib/README.md#lwprintf)：安全简约的标准输出功能库，允许重定向多个输出流，所有 API 均可重入。
- [EasyLogger](./log-term-lib/README.md#easylogger)：功能较全面的日志库，支持动态过滤和颜色选择，注重线程安全，且支持异步输出及缓冲输出模式。
- [zlog](./log-term-lib/README.md#zlog)：是一个高可靠性、高性能、线程安全、灵活、概念清晰的纯 C 日志函数库，不支持内容过滤和解析。

### [终端交互](./log-term-lib/README.md#终端交互)

- [cmd-parser](./log-term-lib/README.md#cmd-parser)：极简的命令解析库，就是通过字符串来触发函数，挺有意思的做法。
- [LwSHELL](./log-term-lib/README.md#lwshell)：轻量级 shell 库，简单易用，附带命令描述。
- [debugcmd](./log-term-lib/README.md#debugcmd)：功能完善的命令行解析库，提供 Tab 补全、帮助查看、子命令注册等功能。
- [Argtable3](./log-term-lib/README.md#argtable3)：规范的命令行解析库，用于自定义操作命令，遵循 POSIX 接口。
- [nr_micro_shell](./log-term-lib/README.md#nr_micro_shell)：标准的命令行交互库，提供 Tab 键命令补全，查询历史命令等功能。
- [letter shell](./log-term-lib/README.md#letter-shell)：功能强大的嵌入式命令行交互库，几乎提供 shell 拥有的所有功能，且能通过函数地址直接执行函数。
- [Xradio_console](./log-term-lib/README.md#xradio_console)：从全志科技 xr806 芯片里提取的控制台库，命令采用分层结构，适合有多命令的时候，基于 RTOS。
- [easyShell](./log-term-lib/README.md#easyshell)：简单易用的单片机 shell，支持 tab 补全。

---

## [校验、安全与引导、升级库](./secure-boot-update-lib/README.md#校验、安全与引导、升级库)

### [校验和安全](./secure-boot-update-lib/README.md#校验和安全)

- [crc-lib-c](./secure-boot-update-lib/README.md#crc-lib-c)：极简的 CRC 库，包含很多常用的 CRC 参数模型实现，无其他扩展功能。
- [tiny-AES-c](./secure-boot-update-lib/README.md#tiny-aes-c)：小巧易移植的 AES 算法库，提供 ECB、CTR 和 CBC 三种加密模式。
- ~~[key](./secure-boot-update-lib/README.md#key)：极简的加密算法，配合密钥使用，功能单一但实用，适合网络加密等领域。~~（待发布）
- [wolfssl](./secure-boot-update-lib/README.md#wolfssl)：是一个轻量级的、可移植的、基于 C 语言的 SSL/TLS 库，它主要针对 IoT、嵌入式和 RTOS 环境。
- [Mbed TLS](./secure-boot-update-lib/README.md#mbed-tls)：可信旗下的项目，业内流行的 SSL/TLS 库。

### [引导和升级](./secure-boot-update-lib/README.md#引导和升级)

- [Tiny Bootloader](./secure-boot-update-lib/README.md#tiny-bootloader)：适用于 8 位和 32 位微控制器的简单引导程序，消耗极少的资源，支持多种总线通讯方式。
- [OpenBLT](./secure-boot-update-lib/README.md#openblt)：著名的微控制器的引导加载程序库，支持 8、16、32 位微控制器。
- [wolfBoot](./secure-boot-update-lib/README.md#wolfboot)：适用于 32 位微控制器的安全引导加载程序解决方案，支持固件身份验证和固件更新机制。
- [mOTA](./secure-boot-update-lib/README.md#mota)：专为 32 位 MCU 开发的升级组件，通过 YModem-1K 协议传输。
- [MicorBoot](./secure-boot-update-lib/README.md#micorboot)：引导加载模块，专为嵌入式单片机设备的升级而优化，提供断电保护、断点续传等功能。
- [MCUboot](./secure-boot-update-lib/README.md#mcuboot)：可信的旗下的项目，通用的 32 位微控制器的安全引导加载程序，不依赖于特定的系统和硬件。

---

## [UI与菜单库](./ui-menu-lib/README.md#ui与菜单库)

### [HMI](./ui-menu-lib/README.md#hmi)

- [tslib](./ui-menu-lib/README.md#tslib)：嵌入式中使用最广泛的电阻触摸屏校正算法库，但好像只能用在 Linux 上。
- [tslib_for_mcu](./ui-menu-lib/README.md#tslib_for_mcu)：linux 下裁剪的一个电阻屏触摸校准库。

### [单色](./ui-menu-lib/README.md#单色)

- [ECBM_GUI](./ui-menu-lib/README.md#ecbm_gui)：超基础的单色 GUI 库，仅通过内建缓存来存放画面内容实现 GUI 功能。适合于自己玩的小项目。
- [SimpleGUI](./ui-menu-lib/README.md#simplegui)：针对单色显示屏设计的 GUI 库，提供简单的绘制功能。适合于像素较低的单色点阵屏。
- [U8g2](./ui-menu-lib/README.md#u8g2)：单色显示器库，提供多种控制器支持和基本图形绘制。
- [MonoGUI](./ui-menu-lib/README.md#monogui)：针对黑白屏幕的小电子设备开发的专用 GUI 系统，功能全面，附带输入法功能。适合电子词典、标签打印机等设备。
- [WouoUI](./ui-menu-lib/README.md#wououi)：模仿自稚晖君暂未开源的 MonoUI，用于实现类似 UltraLink 的丝滑界面，使用编码器作为控制器，还有个特流畅好看的升级版。
- [astra UI](./ui-menu-lib/README.md#astra-ui)：基于 C++ 的 OLED 多级菜单 UI，带有丝滑的过渡动画效果。
- [GLCD](./ui-menu-lib/README.md#glcd)：微控制器嵌入式系统图形 LCD 库，包含硬件驱动、文本及基础图形绘制。

### [彩色](./ui-menu-lib/README.md#彩色)

- [GuiLite](./ui-menu-lib/README.md#guilite)：超轻量级 GUI 库，支持多平台，支持第三方库。
- [Olive.c](./ui-menu-lib/README.md#olivec)：适用于 C 语言的简单 2D 图形库，仅使用画布特征进行绘制。
- [microui](./ui-menu-lib/README.md#microui)：一个微小而便携的 UI 库，其特点是占用极少的内存空间，适用于任何可以绘制矩形和文本的渲染系统。
- [LingLongGUI](./ui-menu-lib/README.md#linglonggui)：高效的 GUI 生成库，配套有图形化编辑界面，方便之间生成代码使用。
- [LingDongGUI](./ui-menu-lib/README.md#lingdonggui)：对 Arm-2D 进行二次封装的 GUI 库，旨在提高易用性，同时也支持原生 API 的使用。
- [AAGUI](./ui-menu-lib/README.md#aagui)：跨平台通用型 GUI，旨在嵌入式里实现类安卓的高级 UI 开发。可使用半声明式（json）编程，适合类似于手机应用的项目开发。
- [GT-HMI](./ui-menu-lib/README.md#gt-hmi)：高通旗下专为国人使用的 UI 库，带有多种语种多字库，带有模拟器和上位机。RTOS、裸机均可使用，适合实用的项目级产品。
- [LVGL](./ui-menu-lib/README.md#lvgl)：轻量级通用图形库，开源免费，几乎拥有 GUI 所需的一切。适用于项目级设备。
- [AWTK](./ui-menu-lib/README.md#awtk)：功能强大的 GUI 图形库。
- [TouchGFX](./ui-menu-lib/README.md#touchgfx)：STM32 旗下的 GUI 图形库，一般只适用于 STM32 的开发。
- [GUIX](./ui-menu-lib/README.md#guix)：Azure RTOS 提供的 GUI 图形库，开发十分成熟和方便，开源免费。
- [emWin](./ui-menu-lib/README.md#emwin)：又名(uCGUI)，是 Segger 旗下的 GUI 图形库，很多知名大厂芯片都是可以授权使用的。
- [Embedded Wizard GUI](./ui-menu-lib/README.md#embedded-wizard-gui)：超强大的 GUI 图形库，但需要收钱。
- [Qt for MCU](./ui-menu-lib/README.md#qt-for-mcu)：QT 旗下的 GUI 图形库，适合有 QT 经验的开发者，需要收费。
- [μGFX](./ui-menu-lib/README.md#μgfx)：可用于触摸屏的轻量级 UI 库，注重性能，非商用免费。
- [MiniGUI](./ui-menu-lib/README.md#minigui)：多平台、高度可定制的 UI 库，可用于不同性能的芯片，适合移动设备及工业等领域，非商用免费。
- [μGUI](./ui-menu-lib/README.md#μgui)：开源的极简图形库，独立于平台，仅一个源文件。
- [Clay](./ui-menu-lib/README.md#clay)：高性能 2D UI 布局库，提供响应式布局能力，适合嵌入式 Web 的制作。
- [Aeropoint GUI](./ui-menu-lib/README.md#aeropoint-gui)：使用 PPT 方式进行 GUI 的创建，需要收费，且没有试用版。
- [Nuklear](./ui-menu-lib/README.md#nuklear)：无依赖的图形用户界面工具包，通过使用输入状态和绘制命令来构建图形，适合快速响应的应用。
- [LinaVG](./ui-menu-lib/README.md#linavg)：适用于 2D 矢量图形的渲染库。
- [BlurHash](./ui-menu-lib/README.md#blurhash)：开源的图片占位符算法和实现，能够在图片预载时先显示框图和缩略图，嵌入式领域可能会用得到。
- [OpenGL](./ui-menu-lib/README.md#opengl)：跨语言、跨平台的 2D/3D 渲染库，主要使用 C 语言开发，但也可以支持 C++、Python、Java 等语言开发，功能极其强大，适合游戏开发、科学可视化、虚拟现实等领域。
- [Rawdraw](./ui-menu-lib/README.md#rawdraw)：跨平台无依赖的 UI 绘制系统，为 OpenGL 提供良好的接口抽象。
- [TinyGL](./ui-menu-lib/README.md#tinygl)：是 OpenGL 的小型实现，适用于嵌入式系统。将复杂的接口精简为更易于理解和操作的形式。
- [foolrenderer](./ui-menu-lib/README.md#foolrenderer)：用 C 语言实现的软件渲染器，不依赖图形库，仅用几千行代码，实现了一套类似 OpenGL 的基本图形功能，以及应用于游戏开发的实时渲染技术，如阴影、切线空间法线映射、基于物理的材质系统等。
- [EmberGL](./ui-menu-lib/README.md#embergl)：用于 MCU 的类似于 OpenGL 的实时 2D / 3D 光栅渲染库。
- [GUIslice](./ui-menu-lib/README.md#guislice)：简单好用的开源 GUI 框架，极客的风格，无动态内存分配，并提供布局上位机。

### [加速](./ui-menu-lib/README.md#加速)

- [Arm-2D](./ui-menu-lib/README.md#arm-2d)：针对 Cortex-M 处理器优化的 2D 图形加速库，处于 GUI 库和驱动层之间。

### [图形](./ui-menu-lib/README.md#图形)

- [qrencode](./ui-menu-lib/README.md#qrencode)：二维码生成库，适用于单片机。
- [QR Code generator library](./ui-menu-lib/README.md#qr-code-generator-library)：通用的QR码生成库，包含多个语言版本，旨在用更少的代码实现更好的性能。
- [QRCode](./ui-menu-lib/README.md#qrcode)：QR码生成库，参考了QR Code generator library，并针对处理器和内存受限的系统进行了优化，支持从 Version 1 到 Version 40 的所有规格。
- [oledlib](./ui-menu-lib/README.md#oledlib)：一个开源的 oled 图形库，带有一些适合做屏保的图形。

### [字形](./ui-menu-lib/README.md#字形)

- [MCUFont](./ui-menu-lib/README.md#mcufont)：专用于字体的库，实现字体压缩、解压缩和文本渲染（调节）功能。
- [Unicorn](./ui-menu-lib/README.md#unicorn)：基于 C99 的 Unicode 编解码库，提供对此编码格式的基本算法和功能。

### [多媒体](./ui-menu-lib/README.md#多媒体)

- [FFmpeg](./ui-menu-lib/README.md#ffmpeg)：业界极为知名的一个跨平台音视频处理框架，提供一组音视频编解码开发套件。

### [菜单框架](./ui-menu-lib/README.md#菜单框架)

- [zBitsView](./ui-menu-lib/README.md#zbitsview)：虚拟多层菜单，仅存在于逻辑层，与有无屏幕无关。
- [emenu](./ui-menu-lib/README.md#emenu)：不寻常的菜单框架，在代码上就可以反映菜单结构。
- ~~[Menu](./ui-menu-lib/README.md#menu)：简单实用的菜单框架，适合在公司小型项目上使用。~~（待发布）
- [cotMenu](./ui-menu-lib/README.md#cotmenu)：采用链表方式实现多级深度菜单，相当于显示的逻辑层，与按键、显示屏完全解耦。
- [MiaoUI](./ui-menu-lib/README.md#miaoui)：基于 U8g2 的 OLED 菜单 UI 框架，支持列表与图标类菜单、非线性动画、任务弹窗等功能。
- [MultMenu](./ui-menu-lib/README.md#multmenu)：多级菜单 + 单色 OLED 非线性动画库，组合使用，移植简单方便，适合类似需求的创客项目。
- [SMF](./ui-menu-lib/README.md#smf)：基于 C++ 的菜单框架，提供多级菜单、菜单对象，适合项目级工程。
- [PageManager](./ui-menu-lib/README.md#pagemanager)：基于 C++ 的页面生命周期管理库，提供完整的页面调度功能，适合项目级工程。

---

## [控制库](./control-lib/README.md#控制库)

### [PID](./control-lib/README.md#PID)

- [pid_temperature_control](./control-lib/README.md#pid_temperature_control)：PID 温度控制，很好的一个示例，通过这个可以把 PID 控制发散至其他领域。

### [CNC](./control-lib/README.md#cnc)

- [Grbl](./control-lib/README.md#grbl)：行业著名的开源 CNC 代码，可用于激光切割机、自动手动写字机、钻孔机、涂鸦画家和古怪的绘图机等，是创客们的首选，也是行业标准。
- [µCNC](./control-lib/README.md#µcnc)：用于微控制器的通用 CNC 固件。

---

## [内核与基层框架库](./kernel-framework-lib/README.md#内核与基层框架库)

### [事件](./kernel-framework-lib/README.md#事件)

- [cpost](./kernel-framework-lib/README.md#cpost)：超轻量的上下文切换和任务解耦库，采用事件分发机制，适合于裸机系统。
- [LwEVT](./kernel-framework-lib/README.md#lwevt)：专业的事件模块库，可选数据结构的自定义类型，且挂载指定函数，可理解为事件和消息的结合，进行事件的分发和回调处理。

### [消息](./kernel-framework-lib/README.md#消息)

- [YAMI4](./kernel-framework-lib/README.md#yami4)：专为分布式系统设计的消息传递库，特别关注控制和监控系统。
- [ZeroMQ](./kernel-framework-lib/README.md#zeromq)：一个高性能异步消息传递库，旨在用于分布式或并发应用程序。
- [CDIPC](./kernel-framework-lib/README.md#cdipc)：一种进程间通信 （IPC） 机制和库，适合在实时系统中协调感知、控制驱动程序和算法。

### [管道](./kernel-framework-lib/README.md#管道)

- [readerwriterqueue](./kernel-framework-lib/README.md#readerwriterqueue)：基于 C++ 的单生产者、单使用者无锁队列，意义同通管道框架，速度快且易用，无需锁也能注重线程安全。

### [邮箱](./kernel-framework-lib/README.md#邮箱)

- [DataCenter](./kernel-framework-lib/README.md#datacenter)：基于 C++ 的消息发布订阅框架，提供完整的邮箱服务，适合项目级工程。

### [线程管理](./kernel-framework-lib/README.md#线程管理)

- [C Thread Pool](./kernel-framework-lib/README.md#c-thread-pool)：轻量级的嵌入式线程池库，用于管理线程的创建和生命周期，解决频繁地创建和销毁线程所带来较大开销的问题。

### [驱动框架](./kernel-framework-lib/README.md#驱动框架)

- ~~[initcall](./kernel-framework-lib/README.md#initcall)：提取 RT-Thread 的初始化框架，使初始化工作在内核中完成。~~（待发布）
- ~~[platform_dev](./kernel-framework-lib/README.md#platform_dev)：模仿 Linux 的简化版驱动框架，设计中不使用动态内存分配，适合低资源的芯片使用。~~（待发布）
- [c-periphery](./kernel-framework-lib/README.md#c-periphery)：基于 Linux 的硬件外设抽象层模板。

### [传感器框架](./kernel-framework-lib/README.md#传感器框架)

- ~~[senser_algorithm](./kernel-framework-lib/README.md#senser_algorithm)：适用于 RTOS 的传感器数据处理框架。~~（待发布）

### [模组框架](./kernel-framework-lib/README.md#模组框架)

- [RIL](./kernel-framework-lib/README.md#ril)：专门为嵌入式平台开发的无线通信模组(GSM/GPRS/CatM1/NB-Iot)管理软件。

### [状态机](./kernel-framework-lib/README.md#状态机)

- [EFSMC](./kernel-framework-lib/README.md#efsmc)：基于事件驱动的有限状态机，通过巧妙设计，避免了命名冲突的问题。使用起来简单、方便、规范。
- [signals_slots](./kernel-framework-lib/README.md#signals_slots)：轻量级信号与槽框架，简化事件驱动编程。
- [UML State Machine in C](./kernel-framework-lib/README.md#uml-state-machine-in-c)：多平台、轻量级状态机框架，支持有限状态机和分层状态机，带有日志记录功能。

### [动态加载](./kernel-framework-lib/README.md#动态加载)

- [dynamic_loader](./kernel-framework-lib/README.md#dynamic_loader)：动态加载函数库，裁剪自 RT-Thread 的 libdl 源码，不与原本 OS 耦合，可在裸机使用。

### [RPC](./kernel-framework-lib/README.md#rpc)

- [ERPC](./kernel-framework-lib/README.md#erpc)：一个简单的、易用的、高效的远程调用框架。
- [EmbedXrpc](./kernel-framework-lib/README.md#embedxrpc)：通过 RPC 通讯协议，可忽略协议本身进行业务逻辑的实现，附带代码生成工具。
- [erpc](./kernel-framework-lib/README.md#erpc)：是 NXP 开源的、用于多芯片嵌入式系统和异构多核 SoC 的开源远程过程调用（RPC）系统。

### [CGI](./kernel-framework-lib/README.md#cgi)

- [FastCGI](./kernel-framework-lib/README.md#fastcgi)：改进了传统 CGI 的性能，增加了分布式计算和多角色特性。

### [Web/HTTP服务器](./kernel-framework-lib/README.md#web/http服务器)

- [LightTPD](./kernel-framework-lib/README.md#lighttpd)：是一个轻量级、高性能的 开源 Web 服务器，专为高并发、低内存占用 的场景设计。相比 Apache 或 Nginx 更适合嵌入式设备。
- [Mongoose](./kernel-framework-lib/README.md#mongoose)：C / C++ 的事件驱动网络库，除了基本协议栈还了内置 HTTP、MQTT 等服务协议，可在裸机及 RTOS 上运行，带有 UI 构建器。商用有付费限制。
- [Boa](./kernel-framework-lib/README.md#boa)：开源的小型 Web 服务器，适用于嵌入式应用。于 2005 起不再更新维护，目前存在已知安全漏洞，不推荐使用。
- [libevent](./kernel-framework-lib/README.md#libevent)：专用于网络服务器的事件驱动库，旨在替换事件驱动网络服务器中的事件循环。
- [dyad](./kernel-framework-lib/README.md#dyad)：基于 Linux 的异步网络库，仅支持 TCP 网络通讯，用于创建小型独立设备服务器，并为现有项目提供网络支持。
- [libevhtp](./kernel-framework-lib/README.md#libevhtp)：适合嵌入式设备的低负载 HTTP 库。

---

## [异常快照与测试库](./exception-test-lib/README.md#异常快照与测试库)

### [Coredump](./exception-test-lib/README.md#coredump)

- [CmBacktrace](./exception-test-lib/README.md#CmBacktrace)：赫赫有名的错误追踪库，针对 ARM Cortex-M 系列的 MCU，基本上稍复杂一点的项目无脑加就完事了。

### [异常捕捉](./exception-test-lib/README.md#异常捕捉)

- ~~[try](./exception-test-lib/README.md#try)：用 C 语言方式实现的 try catch 异常捕获。~~（待发布）
- [CException](./exception-test-lib/README.md#cexception)：适用于 C 语言的简单异常处理，比标准库的更快，可以移植到任何支持 setjmp/longjmp 的平台上。
- [MLA](./exception-test-lib/README.md#mla)：通过记录内存分配计数，来进行内存泄漏分析的库，小巧易用。

### [测试](./exception-test-lib/README.md#测试)

- ~~[MTTEST](./exception-test-lib/README.md#mttest)：基于 RTOS 的简易测试框架，采用注册机制。~~（待发布）
- [MinUnit](./exception-test-lib/README.md#minunit)：C 的最小单元测试框架，不使用内存分配。
- [CuTest](./exception-test-lib/README.md#cutest)：极简的 C 单元测试框架，使用动态内存分配。
- [cmockery](./exception-test-lib/README.md#cmockery)：C 单元测试的轻量级框架，基于标准 C 库。
- [EEMBC](./exception-test-lib/README.md#eembc)：EEMBC 公司提供嵌入式领域众多测试库，主要测试芯片性能，属于业内标准，适合企业级项目部署。
- [Unity](./exception-test-lib/README.md#unity)：C 语言构建的单元测试框架，专注于使用嵌入式工具链。
- [greatest](./exception-test-lib/README.md#greatest)：小巧的 C 语言测试系统，使用插桩/覆盖测试，但可以与其他程序一起运行。
- [Catch2](./exception-test-lib/README.md#catch2)：一个流行的 C++ 单元测试框架，仅一个头文件，它的设计目标是轻量、易用且无依赖。

---

## [数据、算法与AI库](./data-algo-ai-lib/README.md#数据、算法与AI库)

### [算术](./data-algo-ai-lib/README.md#算术)

- ~~[float_converter](./data-algo-ai-lib/README.md#float_converter)：浮点数据四舍五入、取整处理库。~~（待发布）
- [LibBF](./data-algo-ai-lib/README.md#libbf)：高精度浮点运算的库，提供比标准浮点数（如 float 和 double）精度更高的数值，并且可以灵活地控制精度和舍入模式。

### [数据结构](./data-algo-ai-lib/README.md#数据结构)

- [CBUF](./data-algo-ai-lib/README.md#cbuf)：极优雅的宏实现环形缓冲区，功能简单易用。
- [sys/queue](./data-algo-ai-lib/README.md#sys/queue)：Linux、FreeBSD 中使用的队列、链表头文件，全部用宏来实现的，且能够链接任意类型，如结构体等。
- [byte_queue](./data-algo-ai-lib/README.md#byte_queue)：C 语言编写的支持任意类型的环形队列，带宏包装，使用简单。
- [queue](./data-algo-ai-lib/README.md#queue-project1)：C 语言通用队列，支持任意数据类型，使用简单高效。
- [Ring-Buffer](./data-algo-ai-lib/README.md#ring-buffer)：简单高效的环形缓冲库，适合没有指定存储大小的程序。
- [wl_queue](./data-algo-ai-lib/README.md#wl_queue)：支持任意数据类型的环形队列，运用了 C 重载的技巧，注重纤程安全。
- [RingBuffer](./data-algo-ai-lib/README.md#ringbuffer)：实用的环形缓冲库，功能完整，使用的是堆内存分配。
- [queue](./data-algo-ai-lib/README.md#queue-project2)：简单的队列功能库，扩展性强，同时支持零拷贝读写队列（适用于大内存的单个元素，可以有效减少函数耗时）。
- [QueueForMcu](./data-algo-ai-lib/README.md#queueformcu)：普通队列功能模块，仅限非 RTOS 系统，适用于个人小型程序。
- [ConcurrentQueue](./data-algo-ai-lib/README.md#concurrentqueue)：基于 C++ 的工业级无锁队列，无需锁也极其注重线程安全。
- [uthash](./data-algo-ai-lib/README.md#uthash)：提供哈希、列表、环形等数据结构库，只用包含头文件即可使用。
- [LwRB](./data-algo-ai-lib/README.md#lwrb)：专业的 FIFO 环形缓冲库，无动态内存分配，适用于 MDA 传输，注重线程和中断安全。
- [fifofast](./data-algo-ai-lib/README.md#fifofast)：针对 MCU 优化的 FIFO 库，旨在尽可能减少 CPU 和 SRAM 的消耗。

### [基础算法](./data-algo-ai-lib/README.md#基础算法)

- [FXT](./data-algo-ai-lib/README.md#fxt)：C 语言的算法库集合，专注于位运算、组合数学、快速变换等。
- [xxHash](./data-algo-ai-lib/README.md#xxhash)：是一种速度极快的非加密哈希算法，可在 RAM 、速度限制下工作，适合更专业的使用场景。
- [Terathon Math Library](./data-algo-ai-lib/README.md#terathon-math-library)：一个用 C++ 写成的数学库，包含向量、矩阵、四元数和射影几何代数元素的类。可用于图形、AI、游戏等领域。

### [AI框架](./data-algo-ai-lib/README.md#AI框架)

- [TinyMaix](./data-algo-ai-lib/README.md#tinymaix)：专为低资源的单片机设计的 AI 神经网络推理框架。
- [miniMNIST-c](./data-algo-ai-lib/README.md#minimnist-c)：C 语言实现了一个迷你神经网络（两层），可用于学习和基础嵌入式领域。
- [Genann](./data-algo-ai-lib/README.md#genann)：极简的神经网络库，经过充分测试，用于在 C 中训练和使用前馈人工神经网络（ANN）。
- [uTensor](./data-algo-ai-lib/README.md#utensor)：基于 Tensorflow 构建的极其轻量级的机器学习推理框架，并将训练模型生成 C++ 文件导入使用。
- [NNoM](./data-algo-ai-lib/README.md#nnom)：专门为了神经网络在 MCU 上运行的框架，使用起来和 TinyMaix 很像，但功能更多。
- [Paddle Lite](./data-algo-ai-lib/README.md#paddle-lite)：高性能、轻量级、灵活性强且易于扩展的深度学习推理框架，定位于支持包括移动端、嵌入式以及边缘端在内的多种硬件平台。
- [TVM](./data-algo-ai-lib/README.md#tvm)：内置深度学习编译器，适用于 CPU、GPU、ARM 等多种硬件架构，提供一条龙服务。
- [tflite-micro](./data-algo-ai-lib/README.md#tflite-micro)：适用于微控制器的 TensorFlow Lite，也就是在单片机上部署机器学习框架。
- [ncnn](./data-algo-ai-lib/README.md#ncnn)：是一个为移动端极致优化的高性能神经网络前向计算框架，支持大部分常用的 CNN 网络，可部署在部分嵌入式芯片上。
- [MNN](./data-algo-ai-lib/README.md#mnn)：轻量级的深度神经网络引擎，支持深度学习的推理与训练，支持具有 POSIX 接口的嵌入式设备。
- [TensorFlow Lite](./data-algo-ai-lib/README.md#tensorflow-lite)：极有名的机器学习库，可用于在移动设备、微控制器和其他边缘设备上部署模型，以便实现设备端机器学习。
- [Mediapipe](./data-algo-ai-lib/README.md#mediapipe)：谷歌开源的跨平台机器学习框架。它是一个能够轻松部署到移动端、Web、PC 和物联网设备的机器学习工具库，包含了物体检测、图像分类、人脸识别、手势识别、文本分类、语言检测、音频分类等模型。
- [Edge Impulse](./data-algo-ai-lib/README.md#edge-impulse)：流行的嵌入式机器学习开发平台，可以完成数据处理和分析、模型训练、部署模型等工作。
- [YMCV](./data-algo-ai-lib/README.md#ymcv)：纯 C 写的迷你计算机视觉库，无依赖、跨平台，可方便裁剪所需功能。
- [NeuralNetwork](./data-algo-ai-lib/README.md#neuralnetwork)：专用于单片机的神经网络库，仅需极少的资源即可运行RNN、GRU和LSTM等架构，支持裸机和部分操作系统。

### [AI 模型＆算法](./data-algo-ai-lib/README.md#AI-模型＆算法)

- ~~[Knn](./data-algo-ai-lib/README.md#knn)：用 C 语言编写的 Knn 算法，十分基础，没有什么优化，不太推荐使用。~~（待发布）
- [NanoDet-Plus](./data-algo-ai-lib/README.md#nanodet-plus)：超快速、高精度的轻量级无锚物体检测模型，基于移动端 AI 框架实现。
- [pico](./data-algo-ai-lib/README.md#pico)：轻量级的人脸识别算法，基于像素强度比较的目标检测，适合单一、流量较小的场景。

---

## [系统与线程库](./sys-thread-lib/README.md#系统与线程库)

### [时间片调度系统](./sys-thread-lib/README.md#时间片调度系统)

- [ztask](./sys-thread-lib/README.md#ztask)：极简的基于时间片调度器，仅 5 个 api，属于那种随手就可以写出来的框架。
- [ETP](./sys-thread-lib/README.md#etp)：时间片轮询框架，最基本的时间片框架来分离不同的时间片任务，适合简单功能的裸机。
- [cotTask](./sys-thread-lib/README.md#cottask)：时间片轮询框架，初始化、启动和任务调度管理，可以设置任务优先级。
- [CodeBrick](./sys-thread-lib/README.md#codebrick)：时间片轮询框架，包含了很多实用模块，不含驱动层，简单易用。符合现在项目的开发理念，是我很喜欢的一个裸机框架，可以说是普通项目的首选。
- [vkern](./sys-thread-lib/README.md#vkern)：仿照 RTOS 架构编写的任务调度内核，其原理还是使用定时器创建前后台系统。
- [cola_os](./sys-thread-lib/README.md#cola_os)：前后台系统，适合对功耗有要求且 CPU 性能不强的，有稍复杂功能的裸机。
- [JxOS](./sys-thread-lib/README.md#jxos)：前后台系统，没有过多复杂花哨的结构，但重要的功能一应俱全。各个模块也方便单独移植，是复杂裸机项目的首选。
- [EventOS](./sys-thread-lib/README.md#eventos)：事件驱动型的嵌入式系统，提供内核等功能。
- [BabyOS](./sys-thread-lib/README.md#babyos)：简易版的 RTT 裸机系统，带有 PC 模拟，所有外设注册型服务且类文件形式调用，适合于企业级项目开发，能够很好的维护和管理项目。

### [类实时系统](./sys-thread-lib/README.md#类实时系统)

- [cotOs](./sys-thread-lib/README.md#cotos)：简单的查询式协作多任务系统，无需使用定时器进行任务切换，就和 RTOS 创建任务一样，但没有提供其他功能，我很喜欢，感觉酷毙了。
- [BasicOS](./sys-thread-lib/README.md#basicos)：极简的协作式系统，所有的任务共享一个任务栈，包含简单的内核功能组件等。协作式系统适合实时性要求更高的项目。
- [TaskScheduler](./sys-thread-lib/README.md#taskscheduler)：协同多任务处理框架，抢占式编程，但不需要担心并发处理的安全问题。能够对任务的执行参数进行多种配置。
- [QuarkTS](./sys-thread-lib/README.md#quarkts)：事件驱动型多任务调度系统，是它无需考虑并发的陷阱（资源共享、竞争条件、死锁等...），并提供完整内核功能，符合多种行业标准，适合基础企业项目。
- [VSF](./sys-thread-lib/README.md#vsf)：是一个基于事件驱动的抢占式多任务框架，包含内核和常用的组件，适用于企业级项目。

### [RTOS](./sys-thread-lib/README.md#rtos)

- [KLite](./sys-thread-lib/README.md#klite)：最简洁易用的 RTOS，附带最基本实用的内核功能。适合需要快速部署的简单 RTOS 项目。
- [FreeRTOS](./sys-thread-lib/README.md#freertos)：很多小厂商会使用的 OS，网上资料比较多，属于中规中矩那种，适合有一个基础项目，准备上 RTOS 的那种。
- [uC/OS](./sys-thread-lib/README.md#uc/os)：早期比较流行的 OS，和 FreeRTOS 特征一样，功能比它强一些。
- [RT-Thread](./sys-thread-lib/README.md#rt-thread)：国产里耀眼的星星，非常好且实用的 RTOS，附带多个组件和附加功能，文档详细，非常适合一个空白期的 OS 项目。
- [RTX](./sys-thread-lib/README.md#rtx)：ARM 公司的 RTOS，和 Keil 适配性较强。
- [NuttX](./sys-thread-lib/README.md#nuttx)：强调标准兼容和小型封装的操作系统，遵循 POSIX 标准和 ANSI 标准。
- [embOS](./sys-thread-lib/README.md#embos)：SEGGER 公司的 RTOS，可免费用于非商业用途。
- [Azure RTOS](./sys-thread-lib/README.md#azure-rtos)：微软公司的 RTOS。
- [Zephyr](./sys-thread-lib/README.md#zephyr)：Linux 维护的一个 RTOS，很适合学习 Linux 的开发思想。
- [At-RTOS](./sys-thread-lib/README.md#at-rtos)：一个用户友好的嵌入式控制器实时操作系统，仅提供基本的内核功能。
- [Embox](./sys-thread-lib/README.md#embox)：多任务操作系统，其特点是支持使用 Linux 开源组件而不使用 Linux 系统，该开源系统旨在任何地方都能够使用 Linux 软件。
- [YiYiYa OS](./sys-thread-lib/README.md#yiyiya-os)：功能全面的 OS 系统，架构从上而下分层设计，几乎可以将其视为简易版的安卓系统，适合手机那种类型的产品。
- [LK](./sys-thread-lib/README.md#lk)：全称 Little Kernel，是一个微型嵌入式系统，其引导加载程序（BootLoader）最为出名，被作用于原生 Android 系统上。
- [SKRTOS_sparrow](./sys-thread-lib/README.md#skrtos_sparrow)：仅几百行的超微小系统，实现了基本调度和 IPC 机制，有人称之为儿童版 FreeRTOS。
- [CosyOS](./sys-thread-lib/README.md#cosyos)：零中断延迟的操作系统，可实现全局不关总中断而保持实时性，包含很多创新实用的内核功能。
- [scmRTOS](./sys-thread-lib/README.md#scmrtos)：C++ 编写的轻量级的 RTOS，仅提供调度和消息等最基本的内核功能。
- [MuditaOS](./sys-thread-lib/README.md#muditaos)：基于 FreeRTOS 构建，专为 E-Ink 显示屏优化的移动操作系统。

### [IoT-RTOS](./sys-thread-lib/README.md#iot-rtos)

- [Contiki-NG](./sys-thread-lib/README.md#contiki-ng)：uIP 和 LwIP 的作者维护的多任务物联网操作系统，它专注于可靠（安全可靠）的低功耗通信和标准互联网协议。
- [Mbed OS](./sys-thread-lib/README.md#mbed-os)：arm 旗下的易于使用的物联网操作系统。
- [Huawei LiteOS](./sys-thread-lib/README.md#huawei-liteos)：华为旗下针对物联网领域推出的轻量级物联网操作系统。
- [Xiaomi Vela](./sys-thread-lib/README.md#xiaomi-vela)：小米旗下的物联网操作系统，底层基于 NuttX 内核打造。
- [AliOS Things](./sys-thread-lib/README.md#alios-things)：阿里旗下面向 IoT 领域的、高可伸缩的物联网操作系统。
- [TencentOS Tiny](./sys-thread-lib/README.md#tencentos-tiny)：是腾讯面向物联网领域开发的实时操作系统。
- [OneOS](./sys-thread-lib/README.md#oneos)：是中国移动针对物联网领域推出的轻量级操作系统，具有可裁剪、跨平台、低功耗、高安全等特点，支持 - ARM Cortex-M/A、MIPS、RISC-V 等主流芯片架构，兼容 POSIX、CMSIS 等标准接口，支持 Javascript、Micropython 语言开发。
- [LuatOS](./sys-thread-lib/README.md#luatos)：一款针对嵌入式的 Lua 脚本运行框架，包含了一个系统的功能体量。
- [Lua-RTOS-ESP32](./sys-thread-lib/README.md#lua-rtos-esp32)：是一种支持 Lua 解释器的实时操作系统，提供了 Lua 所需所有资源和基本模块、中间件，可以移植到其他 32 位平台。
- [Apache Mynewt OS](./sys-thread-lib/README.md#apache-mynewt-os)：Apache 旗下专为低功耗无线设备所设计的 OS，自带蓝牙协议栈和 IEEE 通信协议，开箱即用。
- [Mongoose OS](./sys-thread-lib/README.md#mongoose-os)：物联网固件开发框架，支持 C/JavaScript 语言开发，对远程管理及升级有较好支持。开源版功能受限。
- [MicroPythonOS](./sys-thread-lib/README.md#micropythonos)：MicroPython 构建的轻量级多功能作系统，专为 ESP32 和桌面系统等微控制器而设计，提供类似Android的现代触屏界面、应用商店、OTA等功能。

### [ROS](./sys-thread-lib/README.md#ros)

- [ROS](./sys-thread-lib/README.md#ros)：业界有名的开源机器人操作系统，它实现了一整套的软件库和工具集。
- [AimRT](./sys-thread-lib/README.md#aimrt)：是一个基于 Modern C++ 开发，面向现代机器人领域的运行时开发框架。提供了全面的插件开发接口，具有高度可扩展性，与其他 ROS 生态兼容。

---

## [模块集合包](./module-pack/README.md#模块集合包)

- [ToolKit](./module-pack/README.md#toolkit)：一个小功能的嵌入式工具包，提供循环队列、软件定时器、事件集三个功能，文档写的很清楚。
- [lwUTIL](./module-pack/README.md#lwutil)：实用工具包，包含值运算、大小端存储、位运算、ascii 转化等。
- [sc](./module-pack/README.md#sc)：高性能且小内存占用的独立工具包，主要提供数据结构的相关功能。
- [cotUtils](./module-pack/README.md#cotutils)：C 语言的通用扩展库，包括多种容器（队列、栈、双向链表、动态数组），序列化/反序列化的结构体，PP 库（多功能宏）等功能。
- [mr-library](./module-pack/README.md#mr-library)：嵌入式轻量级框架，提供标准化的驱动接口和简单的内核功能组件等，是普通厂商级项目的首选。
- [Zorb Framework](./module-pack/README.md#zorb-framework)：轻量级的嵌入式框架，包含基本的内核功能，都是单独集成，方便裁剪使用。
- [Gear-Lib](./module-pack/README.md#gear-lib)：一组通用的 Ｃ 基础库，全部用 POSIX C 实现，旨在兼容 linux, windows, android, ios 等跨平台，包括数据结构、异步、I/O、状态机、动态加载等功能。
- [c-algorithms](./module-pack/README.md#c-algorithms)：提供常用算法和数据结构的集合来弥补标准库的缺失，并且比 C 标准库编译出来的小得多。
- [klib](./module-pack/README.md#klib)：一个独立的轻量级 C 库，提供多种基础算法、数据结构和解析器等功能。
- [AMetal](./module-pack/README.md#ametal)：是 ZLG 旗下的软件包，涵盖了各类型的外设，并统一编写了抽象层接口。代码比较冗余，但类型比较全面。
- [eLab](./module-pack/README.md#elab)：综合开发平台，包含嵌入式所需大部分功能包，尤其注重跨平台开发和 PC 仿真，特别适合对开发流程规范的项目。
- [TheAlgorithms](./module-pack/README.md#thealgorithms)：开源组织 TheAlgorithms 维护的各种基础算法、数据结构、机器学习等库，内容十分丰富，且包含各个流行语言的版本。
- [simpostOS](./module-pack/README.md#simpostos)：是一套设计方法，以及多个软件组件、服务的集合。其理念是将所有功能模块化，并极大地增加功能复用性。使用的是纯 C++ 语言，库写的十分现代化，对新手使用不友好。
- [PetiteDrv](./module-pack/README.md#petitedrv)：通用的 SDK 库，其思想是层层抽象，在不使用复杂的代码完成解耦功能，适合小公司小项目的开发。
- [varch](./module-pack/README.md#varch)：是嵌入式 C 语言常用代码模块库，包含了嵌入式中常用的算法库、数据结构（容器）库,、解析器库、独立 C 语言 std 库、工具库等等，每个库独立使用，简单高效。
- [ctool](./module-pack/README.md#ctool)：常用但一般库里并不包含的工具，包括不定参数、日期、内存测试等。
- [Generic_MCU_Software_Infrastructure](./module-pack/README.md#generic_mcu_software_infrastructure)：提供必要的软件基础设施、服务、宏来支持一些高级的抽象概念和范式。
- [appkit](./module-pack/README.md#appkit)：基于 C++ 的 Linux 应用开发库，包括开发中常用的模块功能（线程管理、定时器、文件 IO、串口通信等）。

---

## [芯片和工具链适配库](./chip-toolchain-lib/README.md#芯片和工具链适配库)

### [51](./chip-toolchain-lib/README.md#51)

- [8051-ELL](./chip-toolchain-lib/README.md#8051-ell)：51 芯片扩展库，适合项目级或稍复杂的工程。
- [ECBM](./chip-toolchain-lib/README.md#ecbm)：51 芯片外设函数库，需要哪个模块就取用哪个模块。

### [AVR](./chip-toolchain-lib/README.md#avr)

### [ST](./chip-toolchain-lib/README.md#st)

- [STM32F4 Discovery](./chip-toolchain-lib/README.md#stm32f4-discovery)：面向 STM32F4 系列微控制器的驱动库集合，包含多个外设、接口的实现教学及配套示例。

### [ESP](./chip-toolchain-lib/README.md#esp)

- [LwESP](./chip-toolchain-lib/README.md#lwesp)：专业的 AT 解析器库，旨在其他设备通过 AT 命令与 ESP 设备进行通信。
- [ESPUI](./chip-toolchain-lib/README.md#espui)：为 ESP32 和 ESP8266 设备设计的简单的网络用户界面库。它使用户能够轻松地创建和管理设备的 Web 界面，无需任何 HTML、CSS 或 JavaScript 前端开发知识。
- [FluidNC](./chip-toolchain-lib/README.md#fluidnc)：针对 ESP32 控制器优化的 CNC 固件库。
- [Rabbit GRBL](./chip-toolchain-lib/README.md#rabbit-grbl)：运行在 ESP32 处理器上的 CNC 固件库，经过高度优化，能够保持高达 120khZ 的稳定、无抖动的控制脉冲。

### [SIMCom](./chip-toolchain-lib/README.md#simcom)

- [LwCELL](./chip-toolchain-lib/README.md#lwcell)：专业的 AT 解析器库，旨在其他设备通过 AT 命令与 SIMCom 设备进行通信。

### [MDK](./chip-toolchain-lib/README.md#mdk)

- [flash_blob](./chip-toolchain-lib/README.md#flash_blob)：利用 MDK 的 FLM 文件快速生成通用 flash 驱动。

### [Driver](./chip-toolchain-lib/README.md#driver)

- [LibDriver](./chip-toolchain-lib/README.md#libdriver)：一个开源的驱动开发组织，包含了所有常用的外设模块驱动库（140+）。

---

## [引擎（仿真）库](./engine-sim-lib/README.md#引擎（仿真）库)

### [SoftFP](./engine-sim-lib/README.md#softfp)

- [SoftFP](./engine-sim-lib/README.md#softfp-project)：用于没有硬件浮点单元（FPU）的情况下，作为软件浮点运算的实现方式。

### [C++](./engine-sim-lib/README.md#c++)

- [sds](./engine-sim-lib/README.md#sds)：简单动态字符串库，使用堆内存，其作用就是在 C 语言中仿照 C++ 的 string 类型。
- [STR](./engine-sim-lib/README.md#str)：更高级的字符串处理库，拥有字符串分割/修剪/搜索/查错等功能。
- [etl](./engine-sim-lib/README.md#etl)：适用于嵌入式的 C++ 模板库。
- [LW_OOPC](./engine-sim-lib/README.md#lw_oopc)：适合嵌入式的面向对象的编程扩展，在源码的基础上进行了多个版本的更新优化，简单易用。
- [PLOOC](./engine-sim-lib/README.md#plooc)：在 C 语言中提供面向对象的编程扩展，可以实现私有成员、继承、重载等功能。
- [vlib](./engine-sim-lib/README.md#vlib)：C 语言模板库，提供了类似 C++ STL 的功能，包含了常用的容器，且可以使用任意数据类型。

### [Lua](./engine-sim-lib/README.md#lua)

- [MicroLua](./engine-sim-lib/README.md#microlua)：适用于树莓派 Pico 的 LUA 开发软件包，通过移植修改应该可以用于其他微控制器设备。
- [eLua](./engine-sim-lib/README.md#elua)：适用于嵌入式的 Lua 引擎。可在嵌入式平台使用 lua 脚本语言。

### [Python](./engine-sim-lib/README.md#python)

- [PikaPython](./engine-sim-lib/README.md#pikapython)：超轻量级 python 引擎，零依赖，零配置，使用 Python 代替 C 开发。具有大量的中文文档和视频资料。

### [Rust](./engine-sim-lib/README.md#rust)

- [Rust Embedded](./engine-sim-lib/README.md#rust-embedded)：专注于改善在资源受限的环境和非传统平台中使用 Rust 的端到端体验。

### [JavaScript](./engine-sim-lib/README.md#javascript)

- [mJS](./engine-sim-lib/README.md#mjs)：专用于微控制器的 JavaScript 引擎，空间占用量小(RAM:1k,ROM:50k)，基于 ES6 标准。

### [Arduino](./engine-sim-lib/README.md#arduino)

- [ArduinoCore-API](./engine-sim-lib/README.md#arduinocore-api)：Arduino 内核的硬件独立层，使用基于 Arduino 相关的库时需要包含对应的 API 文件。、

### [Android](./engine-sim-lib/README.md#android)

- [rawdrawandroid](./engine-sim-lib/README.md#rawdrawandroid)：使用 C 语言开发 Android 应用的开发框架，轻量且跨平台。

### [虚拟机（沙盒）](./engine-sim-lib/README.md#虚拟机沙盒)

- [EVM](./engine-sim-lib/README.md#evm)：针对物联网的超轻量虚拟机，由语法解析前端框架和字节码运行后端构成，可运行在资源受限制的单片机上。支持自行开发 app 运行在此虚拟机引擎上。
- [uvm32](./engine-sim-lib/README.md#uvm32)：一款极简、无依赖的虚拟机（RISC-V）沙箱，专为微控制器及其他资源受限设备设计。单C文件，无动态内存分配，采用异步架构设计。可作为LUA、MicroPython等脚本引擎的替代品。

### [游戏框架](./engine-sim-lib/README.md#游戏框架)

- [Arduboy](./engine-sim-lib/README.md#arduboy)：提供游戏制作所需的编程接口，使其允许游戏玩家轻松制作 C/C++ 游戏，运行在该平台上，并通过社区共享。
- [raylib](./engine-sim-lib/README.md#raylib)：纯 C 编写的游戏库，简易的视频、游戏编程库。

---

## ✨额外

### 库分类细则

由于开源库是多种多样的，有些同样功能的代码用在不同地方就有了不同名字，而有些库里包含了多个子功能，每个子功能都能作为一个领域进行划分，因此开源代码库分类就变得不太容易。
鉴于其特性，我将开源库分为三类：单功能，集功能和其他。

- 单功能：针对单一功能或单一领域的开源代码库，分类原则是按照 `领域-功能` 进行划分；
- 集功能：集成多个功能的软件包或框架系统等，分类原则是按照 `领域` 进行划分；
- 其他：只适配特定类型的芯片或引擎库；

**注意：该开源库不记录仅适配 POSIX 接口的库，若需要请到[其他相关开源库汇总](#其他相关开源库汇总)中查找；*

### 其他相关开源库汇总

- [EmbedSummary: 嵌入式大杂烩资源汇总](https://gitee.com/zhengnianli/EmbedSummary)
- [nhivp/Awesome-Embedded: A curated list of awesome embedded programming.](https://github.com/nhivp/Awesome-Embedded)
- [fffaraz/awesome-cpp: A curated list of awesome C++ (or C) frameworks, libraries, resources, and shiny things. Inspired by awesome-... stuff.](https://github.com/fffaraz/awesome-cpp)

除此之外，Arduino 社区包含极多库，可在 Arduino IDE 应用内搜索，也可以在 [Arduino Library List - Arduino Libraries](https://www.arduinolibraries.info/) 中搜索，其他厂商芯片在使用时需要移植[Arduino内核](./engine-sim-lib/README.md#arduinocore-api)。
