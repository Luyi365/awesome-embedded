# 数据库与格式解析（传输协议）库

> 这里的传输协议库与[总线协议与端侧库](../bus-protocol-lib/README.md)不一样，实际上<ins>传输协议</ins>（待发布）与格式解析意义相等，只不过在格式解析的基础上增加了端与端通讯的概念。

## 数据库

### cotParam

![Gitee Repo stars](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/cot_package/cot_param&query=$.stargazers_count&style=social&logo=gitee&label=Stars) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/cot_package/cot_param&query=$.pushed_at&label=last%20commit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/cot_package/cot_param&query=$.license&label=license)

**链接**：[cotParam: 轻量级参数管理框架(C 语言)](https://gitee.com/cot_package/cot_param)  
**特征**：采用表驱动方式进行参数管理，包括缺省值、最小值和最大值等。  

#### 要点

- 和普通变量赋值最大的区别目前来看有两点：
  - 可以键值配对；
  - 给参数定范围，一旦不符合范围即赋为规定的值；
- 使用介绍：[C 语言参数管理代码框架-重大更新](https://mp.weixin.qq.com/s/Q0ROGgkxjDGXyKAxnu-aHQ)

---

### EasyFlash

![Gitee Repo stars](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Armink/EasyFlash&query=$.stargazers_count&style=social&logo=gitee&label=Stars) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Armink/EasyFlash&query=$.pushed_at&label=last%20commit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Armink/EasyFlash&query=$.license&label=license)

**链接**：[EasyFlash: 轻量级物联网设备信息存储方案，让 Flash 成为小型 KV 数据库。 全新一代版本请移步至 https://gitee.com/armink/FlashDB](https://gitee.com/Armink/EasyFlash)  
**特征**：Key-Value 型简易数据库，主要提供：变量的 KV 配对，IAP 数据修改（可用于升级），log 存储等功能。  

#### 要点

- log 的存储需要用到旗下的：[EasyLogger](../log-term-lib/README.md#easylogger) ；

---

### FlashDB

![Gitee Repo stars](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Armink/FlashDB&query=$.stargazers_count&style=social&logo=gitee&label=Stars) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Armink/FlashDB&query=$.pushed_at&label=last%20commit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Armink/FlashDB&query=$.license&label=license)

**链接**：[FlashDB: 一款支持 KV 数据和时序数据的超轻量级数据库](https://gitee.com/Armink/FlashDB)  
**特征**：提供 KV 和 TS 两种数据库，比起 [EasyFlash](#easyflash) 更专注于数据库本身，而不提供过多的额外功能。  

#### 要点

- ~~介绍：((20230731152707-8yuheud 'FlashDB'))；~~（待发布）
- 使用该库可以用来解决 Flash 地址内数据在设备迭代升级时被移动的问题，因为使用的是键值映射；

---

### Nanopb

![GitHub Repo stars](https://img.shields.io/github/stars/nanopb/nanopb) | ![GitHub last commit](https://img.shields.io/github/last-commit/nanopb/nanopb) | ![GitHub License](https://img.shields.io/github/license/nanopb/nanopb)

**链接**：[Nanopb - protocol buffers with small code size](https://jpa.kapsi.fi/nanopb/)  
**特征**：轻量的、支持 C 语言的 Protobuf，Protobuf 是 Google 公司开发的一种数据格式。可用于数据存储、通信协议等方面，且不依赖于语言和平台，也就是说可以不同设备端进行数据通讯。  

#### 要点

- 协议文档：[Protocol Buffers Documentation](https://protobuf.dev/)
- 教程：
  - [protobuf 优缺点及编码原理 - 牛奔 - 博客园](https://www.cnblogs.com/niuben/p/14212711.html)
  - [Protobuf 使用手册 | 欢迎来到 linghutf 的博客!](https://linghutf.github.io/2016/06/08/protobuf/)
  - [Protobuf 学习 - 入门 - Aut - 博客园](https://www.cnblogs.com/autyinjing/p/6495103.html)
  - [嵌入式大杂烩周记 | 第 9 期](https://mp.weixin.qq.com/s/kS05PsqRAfw7GoxB8FeSvA)
  - [Nanopb 的使用方法_ECBG_2024 的博客-CSDN 博客](https://blog.csdn.net/weixin_56035008/category_10884684.html)
  - [Protocol Buffers_小猪快跑爱摄影的博客-CSDN 博客](https://blog.csdn.net/ymzhu385/category_11573002.html)
- 以前公司用该协议通过蓝牙在设备和手机端进行实时交互；
- 在编写 PB 文件时，要注意层次结构，因为 PB 文件是可以包含其他文件的，要有继承的思想，把类似于 `get`、`put`、`write`、`read` 这类通用操作放在操作的基层；不同种类的事件放在事件的基层；

---

### ITTIA DB

**链接**：[ITTIA | ITTIA DB Safe and Secure Embedded Edge Data Platform](https://www.ittia.com)  
**Lite 版链接**：[ITTIA DB Lite | ITTIA](https://www.ittia.com/ittia-db-lite)  
**特征**：功能强大的实时嵌入式数据库，主要用于嵌入式系统和物联网设备，用于在设备上本地监控，存储和分析时间序列数据，需要商业许可。  

#### 要点

---

### linq4c

![GitHub Repo stars](https://img.shields.io/github/stars/haifenghuang/linq4c) | ![GitHub last commit](https://img.shields.io/github/last-commit/haifenghuang/linq4c) | ![GitHub License](https://img.shields.io/github/license/haifenghuang/linq4c)

**链接**：[haifenghuang/linq4c: LINQ for C(GroupBy, GroupJoin, Join, Take, Where, Select, etc)](https://github.com/haifenghuang/linq4c)  
**特征**：在 C 语言里实现了 C# 的 linq 方法。  

#### 要点

- 什么是 LINQ？将代码中的数据集合成一个数据库，给定其标签，并用类似于 SQL 的查询语法来操作该集合，能够以一种更直观、更简洁的方式来查询和处理数据。

---

### SQLite

![License: SQLite](https://img.shields.io/badge/license-SQLite-blue.svg)

**链接**：[SQLite Home Page](https://www.sqlite.org/)  
**特征**：业界用的最多的嵌入式标准的数据库，使用 SQL 语法，可使用磁盘文件。  

#### 要点

- ~~详细解释可参见：((20240701142124-fkzyo5i 'SQLite（MySQL）'))；~~（待发布）

---

## 数据流

> 怎么做到真正的流控：（以 UART 向用户层传输为例）
> 1. UART+DMA 进行数据收发；
> 2. DMA 永远进行 UART 端的数据接收工作，触发指定条件后将其数据转移到 UART 流缓冲区；
> 3. 将流数据进行分包后再提交到 UART 队列缓存中；
> 4. 数据处理线程挂起，当发现 UART 队列缓存中有数据后启动接收处理（序列化）；
> 5. 反过来一样，用户数据先发送到用户队列缓存区，之后数据处理区进行接收处理（反序列化），再给到 DMA 由 UART 发生出去；
> 
> ![CMSIS-Stream-Graph](CMSIS-Stream-Graph.gif)
>

### uart_stream

**链接**：[UART 与用户数据流缓冲处理 - 代码片段 - Gitee.com](https://gitee.com/Luyi365/codes/jr7tzaiq6lupefkxh4com60)  
**特征**：数据流缓冲处理库，针对 UART 数据，但有一定的通用性。  

#### 要点

- 因为使用了 cJSON 解析库，不能拿来直接用，有些地方需要改改；

---

### xprintf

![License: xprintf](https://img.shields.io/badge/License-xprintf-blue.svg)

**链接**：[ELM - Embedded String Functions](http://elm-chan.org/fsw/strf/xprintf.html)  
**特征**：嵌入式字符串函数，代替不足以实现常规 printf 功能，可以动态的将字符串写入不同外设。  

#### 要点

---

### CMSIS-Stream

![GitHub Repo stars](https://img.shields.io/github/stars/ARM-software/CMSIS-Stream) | ![GitHub last commit](https://img.shields.io/github/last-commit/ARM-software/CMSIS-Stream) | ![GitHub License](https://img.shields.io/github/license/ARM-software/CMSIS-Stream)

**链接**：[ARM-software/CMSIS-Stream: CMSIS-Stream software component](https://github.com/ARM-software/CMSIS-Stream)  
**特征**：ARM 官方出品的数据流处理组件，提供图形表示，需要 Python 和 C++ 联合完成。  

#### 要点

- 由 Python 根据配置生成 C++ 代码；

---

## 压缩库

### lz4

![GitHub Repo stars](https://img.shields.io/github/stars/lz4/lz4) | ![GitHub last commit](https://img.shields.io/github/last-commit/lz4/lz4) | ![GitHub License](https://img.shields.io/github/license/lz4/lz4)

**链接**：[LZ4 - Extremely fast compression](https://lz4.org/)  
**特征**：极快的无损压缩算法库，适合通信时的数据压缩。  

#### 要点

---

### heatshrink

![GitHub Repo stars](https://img.shields.io/github/stars/atomicobject/heatshrink) | ![GitHub last commit](https://img.shields.io/github/last-commit/atomicobject/heatshrink) | ![GitHub License](https://img.shields.io/github/license/atomicobject/heatshrink)

**链接**：[atomicobject/heatshrink: data compression library for embedded/real-time systems](https://github.com/atomicobject/heatshrink)  
**特征**：超低资源消耗的嵌入式解压缩库。相关文档较少。  

#### 要点

- 目前还不清楚是否能和文件系统联动，能够解压 PC 上的压缩包；

---

### TJpgDec

![License: TJpgDec](https://img.shields.io/badge/License-TJpgDec-blue.svg)

**链接**：[TJpgDec - Tiny JPEG Decompressor](http://elm-chan.org/fsw/tjpgd/00index.html)  
**特征**：针对嵌入式系统优化的 JPEG 图像解压缩模块。  

#### 要点

- 支持像素格式：RGB888、RGB565 或灰度；

---

## URL

![Gitee Repo stars](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/yikoulinux/url&query=$.stargazers_count&style=social&logo=gitee&label=Stars) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/yikoulinux/url&query=$.pushed_at&label=last%20commit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/yikoulinux/url&query=$.license&label=license)

### <a name="url-project"></a>url

**链接**：[url: 用 C 语言实现一个简单的解析 url 的算法](https://gitee.com/yikoulinux/url)  
**特征**：简单的解析 url 模块，可以解析不同段的信息。  

#### 要点

- 使用介绍：[分享一个 C 语言实现 url 解析的小实例](https://mp.weixin.qq.com/s/gRErTrfOfx5RVwyGGXjrEQ)

---

## SSH

### tinyssh

![GitHub Repo stars](https://img.shields.io/github/stars/janmojzis/tinyssh) | ![GitHub last commit](https://img.shields.io/github/last-commit/janmojzis/tinyssh) | ![GitHub License](https://img.shields.io/github/license/janmojzis/tinyssh)

**链接**：[janmojzis/tinyssh：TinySSH 是小型服务器（少于 100000 字代码）](https://github.com/janmojzis/tinyssh)  
**特征**：一个简约的 SSH 服务器，它只实现了 SSHv2 功能的子集，适合嵌入式使用。  

#### 要点

---

## MQTT

### Paho MQTT

![GitHub Repo stars](https://img.shields.io/github/stars/eclipse-paho/paho.mqtt.embedded-c) | ![GitHub last commit](https://img.shields.io/github/last-commit/eclipse-paho/paho.mqtt.embedded-c) | ![GitHub License](https://img.shields.io/github/license/eclipse-paho/paho.mqtt.embedded-c)

**链接**：[eclipse/paho.mqtt.embedded-c: Paho MQTT C client library for embedded systems. Paho is an Eclipse IoT project](https://github.com/eclipse/paho.mqtt.embedded-c)  
**特征**：嵌入式平台的 MQTT 客户端库。  

#### 要点

---

### mqttclient

![GitHub Repo stars](https://img.shields.io/github/stars/IoTSharp/mqttclient) | ![GitHub last commit](https://img.shields.io/github/last-commit/IoTSharp/mqttclient) | ![GitHub License](https://img.shields.io/github/license/IoTSharp/mqttclient)

**链接**：[jiejieTop/mqttclient: A high-performance, high-stability, cross-platform MQTT client, developed based on the socket API, can be used on embedded devices (FreeRTOS / LiteOS / RT-Thread / TencentOS tiny), Linux, Windows, Mac, with a very concise The API interface realizes the quality of service of QOS2 with very few resources, and seamlessly connects the mbedtls encryption library.](https://github.com/IoTSharp/mqttclient)  
**特征**：高性能、高稳定性的跨平台 MQTT 客户端，拥有简洁的 API，无缝衔接 [Mbed TLS](../secure-boot-update-lib/README.md#mbed-tls) 库，提供在线代码生成工具。  

#### 要点

---

### Mosquitto

![GitHub Repo stars](https://img.shields.io/github/stars/eclipse-mosquitto/mosquitto) | ![GitHub last commit](https://img.shields.io/github/last-commit/eclipse-mosquitto/mosquitto) | ![GitHub License](https://img.shields.io/github/license/eclipse-mosquitto/mosquitto)

**链接**：[Eclipse Mosquitto](https://mosquitto.org/)  
**特征**：Eclipse 旗下的一个开源的消息代理（broker），主要用于实现 MQTT 协议。它设计轻巧，资源占用少，适合物联网领域的企业级项目。  

#### 要点

---

## AT

### AT Command

![Gitee Repo stars](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/moluo-tech/AT-Command&query=$.stargazers_count&style=social&logo=gitee&label=Stars) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/moluo-tech/AT-Command&query=$.pushed_at&label=last%20commit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/moluo-tech/AT-Command&query=$.license&label=license)

**链接**：[AT Command: 一款管理 AT 命令通信交互组件， 适用于 Modem、WIFI 模块、蓝牙等使用 AT 命令或者 ASCII 命令行通信的场景。](https://gitee.com/moluo-tech/AT-Command)  
**特征**：AT 命令通信解析模块，适用于 Modem、WIFI 模块、蓝牙等使用 AT 命令或者 ASCII 命令行通信的场景。  

#### 要点

- 分为 OS 和裸机两种模块；
- 使用介绍：[一个 AT 命令通信解析模块！](https://mp.weixin.qq.com/s/XFrq6t5kjOOQUqhaZfmNGA)

---

### Xradio\_atcmd

![GitHub Repo stars](https://img.shields.io/github/stars/XradioTech/xradio-skylark-sdk) | ![GitHub last commit](https://img.shields.io/github/last-commit/XradioTech/xradio-skylark-sdk?path=src%2Fatcmd) | ![GitHub License](https://img.shields.io/github/license/XradioTech/xradio-skylark-sdk)

**链接**：[xradio-skylark-sdk/src/atcmd at master · XradioTech/xradio-skylark-sdk](https://github.com/XradioTech/xradio-skylark-sdk/tree/master/src/atcmd)、[xradio-skylark-sdk/include/atcmd at master · XradioTech/xradio-skylark-sdk](https://github.com/XradioTech/xradio-skylark-sdk/tree/master/include/atcmd)  
**特征**：Xradio SDK 里提取的 AT 命令解析库，命令实例丰富，基于 RTOS。  

#### 要点

- Demo：[xradio-skylark-sdk/project/demo/at_demo at master · XradioTech/xradio-skylark-sdk](https://github.com/XradioTech/xradio-skylark-sdk/tree/master/project/demo/at_demo)；
- 还有一些依赖库基于 SDK 里的其他文件；

---

## Base64

> 参考：[嵌入式大杂烩周记 | 第 14 期](https://mp.weixin.qq.com/s/iF2GuG1hDBeNJyxBCfqn8A)  
>
> base64 可以说是最简单的编解码了，可作为设备端传输的中间层，其作用是屏蔽传输上的差异。  
>
> 另外，网上有极多 base64 源码库，可自行查找选择。  

### <a name="base64-project1"></a>base64

![Gitee Repo stars](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/ylguo/base64&query=$.stargazers_count&style=social&logo=gitee&label=Stars) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/ylguo/base64&query=$.pushed_at&label=last%20commit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/ylguo/base64&query=$.license&label=license)

**链接**：[base64: c 语言版 base64 编解码算法实现](https://gitee.com/ylguo/base64)  
**特征**：极简单的 base64 编解码库。  

#### 要点

---

### <a name="base64-project2"></a>base64

![GitHub Repo stars](https://img.shields.io/github/stars/aklomp/base64) | ![GitHub last commit](https://img.shields.io/github/last-commit/aklomp/base64) | ![GitHub License](https://img.shields.io/github/license/aklomp/base64)

**链接**：[aklomp/base64: Fast Base64 stream encoder/decoder in C99, with SIMD acceleration](https://github.com/aklomp/base64)  
**特征**：支持 SIMD 和 OpenMP 加速的 base64 编解码库，不使用动态内存，注重线程安全。  

#### 要点

---

## CSV

### MiniCSV

![GitHub Repo stars](https://img.shields.io/github/stars/jedisct1/minicsv) | ![GitHub last commit](https://img.shields.io/github/last-commit/jedisct1/minicsv) | ![GitHub License](https://img.shields.io/github/license/jedisct1/minicsv)

**链接**：[jedisct1/minicsv: A tiny, fast, simple, single-file, BSD-licensed CSV parsing library in C.](https://github.com/jedisct1/minicsv)  
**特征**：极简的 CSV 解析库，能够解决多行、转义行、转义列中的转义字符、空行、列数可变的行、Windows 或 Unix 风格的行结尾等问题。  

#### 要点

- 使用介绍：[基于 C 语言的开源 csv 解析库：MiniCSV 使用示例_whik1194 的博客-CSDN 博客](https://blog.csdn.net/whik1194/article/details/131490767)
- 不使用动态内存；
- 一次性全部解出和读入；

---

### CRStrLib

![GitHub Repo stars](https://img.shields.io/github/stars/mushroom-x/CRStrLib) | ![GitHub last commit](https://img.shields.io/github/last-commit/mushroom-x/CRStrLib) | ![GitHub License](https://img.shields.io/github/license/mushroom-x/CRStrLib)

**链接**：[mushroom-x/CRStrLib: 此工程主要用于 C 语言解析 csv 格式/其他格式的字符串， 提取数值，帧头帧尾校验。 可以加入到单片机工程或者添加到 Arduino 的库函数中。](https://github.com/mushroom-x/CRStrLib)  
**特征**：解析 csv 格式/其他格式的字符串， 提取数值，帧头帧尾校验。  

#### 要点

---

### fast-cpp-csv-parser

![GitHub Repo stars](https://img.shields.io/github/stars/ben-strasser/fast-cpp-csv-parser) | ![GitHub last commit](https://img.shields.io/github/last-commit/ben-strasser/fast-cpp-csv-parser) | ![GitHub License](https://img.shields.io/github/license/ben-strasser/fast-cpp-csv-parser)

**链接**：[ben-strasser/fast-cpp-csv-parser: fast-cpp-csv-parser](https://github.com/ben-strasser/fast-cpp-csv-parser)  
**特征**：基于 C++ 的 CSV 解析器，小型、易于使用且快速的仅标头库。  

#### 要点

---

## INI

> `.ini` 文件格式说明：[INI](./Appendix.md#ini)。

### libinimini

![GitHub Repo stars](https://img.shields.io/github/stars/lovemengx/libinimini) | ![GitHub last commit](https://img.shields.io/github/last-commit/lovemengx/libinimini) | ![GitHub License](https://img.shields.io/github/license/lovemengx/libinimini)

**链接**：[lovemengx/libinimini: ini 极简解析库，适用于 Android、Linux、Rtos 以及单片机](https://github.com/lovemengx/libinimini)  
**特征**：适用单片机的 ini 极简解析库，内存空间占用可控。最简单的键值配对文件格式。  

#### 要点

---

### inih

![GitHub Repo stars](https://img.shields.io/github/stars/benhoyt/inih) | ![GitHub last commit](https://img.shields.io/github/last-commit/benhoyt/inih) | ![GitHub License](https://img.shields.io/github/license/benhoyt/inih)

**链接**：[benhoyt/inih: Simple .INI file parser in C, good for embedded systems](https://github.com/benhoyt/inih)  
**特征**：基于 C 编写的 ini 解析库，适合嵌入式系统。带有语法与解析选项。  

#### 要点

- 使用介绍：[嵌入式大杂烩周记 | 第 10 期](https://mp.weixin.qq.com/s/QAElgMjgHqEmO_V_TvuppA)

---

### iniparser

![GitHub Repo stars](https://img.shields.io/github/stars/ndevilla/iniparser) | ![GitHub last commit](https://img.shields.io/github/last-commit/ndevilla/iniparser) | ![GitHub License](https://img.shields.io/github/license/ndevilla/iniparser)

**链接**：[ndevilla/iniparser: ini file parser](https://github.com/ndevilla/iniparser)  
**特征**：基于 C 编写的 ini 解析库，可移植嵌入式系统，注重线程安全。  

#### 要点

- 使用介绍：[分享一个好用的 C 语言.ini 文件的解析库-阿里云开发者社区](https://developer.aliyun.com/article/1325467)

---

## TLV

> 协议介绍：[TLV](./Appendix.md#tlv)。

### ITLV

**链接**：[ITLV: TLV（Tag、Length、Value）格式数据的优化版本，极简轻量的数据传输格式，可以以此为基础自定义数据格式，附带 CRC 检验。](https://gitee.com/Luyi365/itlv)  
**特征**：TLV（Tag、Length、Value）格式数据的优化版本，极简轻量的数据传输格式，可以以此为基础自定义数据格式，附带 CRC 检验。  

#### 要点

- 使用介绍：[分享一种灵活性很高的协议格式（附代码例子）](https://mp.weixin.qq.com/s/z0Qr2D5yCpEiBPenYWrdOw)；

---

### <a name="tlv-project"></a>tlv

![GitHub Repo stars](https://img.shields.io/github/stars/skullboyer/TLV) | ![GitHub last commit](https://img.shields.io/github/last-commit/skullboyer/TLV) | ![GitHub License](https://img.shields.io/github/license/skullboyer/TLV)

**链接**：[skullboyer/TLV](https://github.com/skullboyer/TLV)  
**特征**：TLV 格式编码实现。  

#### 要点

- 使用介绍：[【TLV】一种 TLV 编码实现 - 壹点灵异 - 博客园](https://www.cnblogs.com/skullboyer/p/17982042)

---

## JSON

> ~~JSON 文件格式说明：((20230121192127-ajlkxif 'JSON'))~~（待发布）

### cJSON

![GitHub Repo stars](https://img.shields.io/github/stars/DaveGamble/cJSON) | ![GitHub last commit](https://img.shields.io/github/last-commit/DaveGamble/cJSON) | ![GitHub License](https://img.shields.io/github/license/DaveGamble/cJSON)

**链接**：[DaveGamble/cJSON: Ultralightweight JSON parser in ANSI C](https://github.com/DaveGamble/cJSON)  
**特征**：ANSI C 中的超轻量级 JSON 解析器，也是最原生的 JSON 解析库，用起来会有点麻烦，不太推荐直接使用。  

#### 要点

- 使用介绍：
  [JSON 的简单介绍&cJSON 库使用（一）](https://www.jianshu.com/p/59eb2bd1aeea)  
  [cJSON 解析和生成 JSON 文件 | 守望的个人博客](https://www.yanbinghu.com/2019/08/04/21364.html)  
- json 对象可以是 json、字符串、数组等。

---

### struct2json

![Gitee Repo stars](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Armink/struct2json&query=$.stargazers_count&style=social&logo=gitee&label=Stars) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Armink/struct2json&query=$.pushed_at&label=last%20commit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Armink/struct2json&query=$.license&label=license)

**链接**：[struct2json: C 结构体与 JSON 快速互转库，快速实现 C 结构体的序列化及反序列化](https://gitee.com/Armink/struct2json)  
**特征**：基于 [cJSON](#cjson)，超简便的 C 结构体与 JSON 快速互转库。  

#### 要点

---

### cson

![GitHub Repo stars](https://img.shields.io/github/stars/NevermindZZT/cson) | ![GitHub last commit](https://img.shields.io/github/last-commit/NevermindZZT/cson) | ![GitHub License](https://img.shields.io/github/license/NevermindZZT/cson)

**链接**：[NevermindZZT/cson: 基于 C 语言的 json 数据映射解析库](https://github.com/NevermindZZT/cson)  
**特征**：基于 [cJSON](#cjson)，运行于 C 语言平台的 json-struct 模型解析工具。使 JSON 解析更加方便。  

#### 要点

---

### <a name="json-project"></a>json

![Gitee Repo stars](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Lamdonn/json&query=$.stargazers_count&style=social&logo=gitee&label=Stars) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Lamdonn/json&query=$.pushed_at&label=last%20commit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Lamdonn/json&query=$.license&label=license)

**链接**：[json: C 语言 json 解释器，简洁高效，灵活安全](https://gitee.com/Lamdonn/json)  
**特征**：简单高效的 C 语言 json 生成和解析库，适合简单项目的使用。  

#### 要点

---

### JSMN

![GitHub Repo stars](https://img.shields.io/github/stars/zserge/jsmn) | ![GitHub last commit](https://img.shields.io/github/last-commit/zserge/jsmn) | ![GitHub License](https://img.shields.io/github/license/zserge/jsmn)

**链接**：[zserge/jsmn: Jsmn is a world fastest JSON parser/tokenizer. This is the official repo replacing the old one at Bitbucket](https://github.com/zserge/jsmn)  
**特征**：超简约、极快的 JSON 解析器，无动态内存分配，无解析纠正。  

#### 要点

- 注意只能单向的从 JSON→C 解析；
- 原理是记录每个 json 的键值位置，不会创造副本来解析，因此非常节省空间；

---

### lwjson

![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwjson) | ![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwjson) | ![GitHub License](https://img.shields.io/github/license/MaJerle/lwjson)

**链接**：[LwJSON latest-develop documentation — LwJSON documentation](https://docs.majerle.eu/projects/lwjson/en/latest/)  
**特征**：针对嵌入式系统优化的通用 JSON 解析器库。  

#### 要点

- 注意只能单向的从 JSON→C 解析；

---

### MojoJson

![GitHub Repo stars](https://img.shields.io/github/stars/scottcgi/MojoJson) | ![GitHub last commit](https://img.shields.io/github/last-commit/scottcgi/MojoJson) | ![GitHub License](https://img.shields.io/github/license/scottcgi/MojoJson)

**链接**：[scottcgi/MojoJson: A simple and fast JSON parser.](https://github.com/scottcgi/MojoJson)  
**特征**：通用的 JSON 解析库，采用面向对象的思想实现，提供 C 语言版本。  

#### 要点

- 注意只能单向的从 JSON→C 解析；

---

### LJSON

![Gitee Repo stars](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/lengjingzju/json&query=$.stargazers_count&style=social&logo=gitee&label=Stars) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/lengjingzju/json&query=$.pushed_at&label=last%20commit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/lengjingzju/json&query=$.license&label=license)

**链接**：[json: LJSON 是一个远远快于 cJSON(最快可达 20 倍)、大幅度快于 RapidJSON (最快可达 1 倍)的 C 实现的 JSON 库，他是目前最快的通用 JSON 库。 LJSON 支持 JSON 的解析、打印、编辑，提供 DOM 和 SAX 接口，I/O 支持字符串和文件，且完全支持 nativejson-benchmark 的测试用例。](https://gitee.com/lengjingzju/json)  
**特征**：号称最快的 JSON 解析库，功能极为强大，几乎覆盖了 JSON 解析的所有需要。  

#### 要点

---

### json-parser

![GitHub Repo stars](https://img.shields.io/github/stars/Barenboim/json-parser) | ![GitHub last commit](https://img.shields.io/github/last-commit/Barenboim/json-parser) | ![GitHub License](https://img.shields.io/github/license/Barenboim/json-parser)

**链接**：[Barenboim/json-parser: JSON parser in standard C](https://github.com/Barenboim/json-parser)  
**C++ 版**：[wfrest/Json: c++ Json library](https://github.com/wfrest/Json)  
**特征**：简单、规范、实用的 JSON 库，包括解析和生成。  

#### 要点

---

### Frozen

![GitHub Repo stars](https://img.shields.io/github/stars/cesanta/frozen) | ![GitHub last commit](https://img.shields.io/github/last-commit/cesanta/frozen) | ![GitHub License](https://img.shields.io/github/license/cesanta/frozen)

**链接**：[cesanta/frozen: JSON parser and generator for C/C++ with scanf/printf like interface. Targeting embedded systems.](https://github.com/cesanta/frozen)  
**特征**：类似 scanf/printf 的 JSON 解析和生成库，内置 base64 编码器和二进制数据解码器。  

#### 要点

---

### sj.h

![GitHub Repo stars](https://img.shields.io/github/stars/rxi/sj.h) | ![GitHub last commit](https://img.shields.io/github/last-commit/rxi/sj.h) | ![GitHub License](https://img.shields.io/github/license/rxi/sj.h)

**链接**：[GitHub - rxi/sj.h: A tiny little JSON parsing library](https://github.com/rxi/sj.h)  
**特征**：极简的 C 语言 JSON 解析库，采用零拷贝策略，直接在原数据上解析。  

#### 要点

---

## XML

### simple\_xml

![Gitee Repo stars](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/xfwangqiang/simple_xml&query=$.stargazers_count&style=social&logo=gitee&label=Stars) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/xfwangqiang/simple_xml&query=$.pushed_at&label=last%20commit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/xfwangqiang/simple_xml&query=$.license&label=license)

**链接**：[simple_xml: 基于 C 语言的 XML 解析器，已有的一些开源解析器都与操作系统相关，对于一些并不主流的操作系统以及嵌入式操作系统，想应用 XML 文件，就显得比较困难。开发本项目的目的在于开发一个能在多平台应用的代码](https://gitee.com/xfwangqiang/simple_xml)  
**特征**：XML 解析库，具有完备的功能，支持双向解析。  

#### 要点

---

### TinyXML-2

![GitHub Repo stars](https://img.shields.io/github/stars/leethomason/tinyxml2) | ![GitHub last commit](https://img.shields.io/github/last-commit/leethomason/tinyxml2) | ![GitHub License](https://img.shields.io/github/license/leethomason/tinyxml2)

**链接**：[leethomason/tinyxml2: TinyXML2 is a simple, small, efficient, C++ XML parser that can be easily integrated into other programs.](https://github.com/leethomason/tinyxml2)  
**特征**：基于 C++ 的 XML 解析库，它使用文档对象模型（DOM），可以很方便的将 XML 和 C++ 对象互相加息转换。  

#### 要点

---

## TOML

### <a name="toml-project"></a>toml

**链接**：[TOML：Tom 的（语义）明显、（配置）最小化的语言](https://toml.io/cn/)  
**特征**：比 INI 的扩展性强、又没有层层嵌套的 JSON 和 YAML 的缩进语法，一种人们不常了解的数据标记格式。  

#### 要点

---

## 其他

### LwPKT

![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwpkt) | ![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwpkt) | ![GitHub License](https://img.shields.io/github/license/MaJerle/lwpkt)

**链接**：[LwPKT latest-develop documentation — LwPKT documentation](https://docs.majerle.eu/projects/lwpkt/en/latest/)  
**特征**：通用数据包协议库，可变数据长度，支持理论上无限的数据包长度，允许在网络中使用发件人地址和收件人地址进行多个注释，附带 CRC 检验。  

#### 要点

- 使用介绍：[嵌入式中轻量级通信协议利器！](https://mp.weixin.qq.com/s/e_yvMNMILzvpLtvmDw3iCw)
- 使用 [LwRB](../data-algo-ai-lib/README.md#lwrb) 库进行数据读/写操作；

---

### xpack

![GitHub Repo stars](https://img.shields.io/github/stars/xyz347/xpack) | ![GitHub last commit](https://img.shields.io/github/last-commit/xyz347/xpack) | ![GitHub License](https://img.shields.io/github/license/xyz347/xpack)

**链接**：[xyz347/xpack: convert json/xml/bson to c++ struct](https://github.com/xyz347/xpack)  
**特征**：用于在 C++ 结构体和 json/xml/yaml/bson/mysql/sqlite 之间互相转换，仅有头文件。  

#### 要点

---

### ESSL

![GitHub Repo stars](https://img.shields.io/github/stars/espressif/idf-extra-components) | ![GitHub last commit](https://img.shields.io/github/last-commit/espressif/idf-extra-components?path=esp_serial_slave_link) | ![GitHub License](https://img.shields.io/github/license/espressif/idf-extra-components)

**链接**：[idf-extra-components/esp_serial_slave_link at master · espressif/idf-extra-components](https://github.com/espressif/idf-extra-components/tree/master/esp_serial_slave_link)  
**特征**：ESP 旗下的串行从机链路，该组件能让主机通过总线驱动和相应的协议与从机进行通信。也可以说就是双 mcu 通讯，只是在上面套了一层壳。  

#### 要点

---

### Uart\_Transfer\_BIN\_to\_exFlash

![GitHub Repo stars](https://img.shields.io/github/stars/firestaradmin/Uart_Transfer_BIN_to_exFlash) | ![GitHub last commit](https://img.shields.io/github/last-commit/firestaradmin/Uart_Transfer_BIN_to_exFlash) | ![GitHub License](https://img.shields.io/github/license/firestaradmin/Uart_Transfer_BIN_to_exFlash)

**链接**：[firestaradmin/Uart_Transfer_BIN_to_exFlash: STM32 串口烧录 BIN 文件、字库文件【QT 上位机】](https://github.com/firestaradmin/Uart_Transfer_BIN_to_exFlash)  
**特征**：基于串口通讯，增加帧属性，从而方便、可靠的将数据传输到 Flash 中。  

#### 要点

---

### SACP

![GitHub Repo stars](https://img.shields.io/github/stars/Snapmaker/SnapmakerController-IDEX) | ![GitHub last commit](https://img.shields.io/github/last-commit/Snapmaker/SnapmakerController-IDEX?path=snapmaker%2Fprotocol) | ![GitHub License](https://img.shields.io/github/license/Snapmaker/SnapmakerController-IDEX)

**链接**：[SnapmakerController-IDEX/snapmaker/protocol at main · Snapmaker/SnapmakerController-IDEX](https://github.com/Snapmaker/SnapmakerController-IDEX/tree/main/snapmaker/protocol)  
**特征**：是 Snapmaker 设备的数据通信协议，基于 C++ 的专用于整机多设备的设备间通信。  

#### 要点

- 使用介绍：[一个可用于多设备间的 C/C++ 嵌入式通信协议的设计与实现-SACP 协议](https://mp.weixin.qq.com/s/Kj-9V5xJBlQQTgMj97O-Yw)
- 相关：[MVC 模式](./Appendix.md#mvc-模式)

---

### rtty

![GitHub Repo stars](https://img.shields.io/github/stars/zhaojh329/rtty) | ![GitHub last commit](https://img.shields.io/github/last-commit/zhaojh329/rtty) | ![GitHub License](https://img.shields.io/github/license/zhaojh329/rtty)

**链接**：[zhaojh329/rtty: 🐛 Access your terminal from anywhere via the web.](https://github.com/zhaojh329/rtty)  
**特征**：通过 Web 访问设备的终端，适合嵌入式 Linux，有点意思。  

#### 要点

---

### Nanomsg

![GitHub Repo stars](https://img.shields.io/github/stars/nanomsg/nanomsg) | ![GitHub last commit](https://img.shields.io/github/last-commit/nanomsg/nanomsg) | ![GitHub License](https://img.shields.io/github/license/nanomsg/nanomsg)

**链接**：[About Nanomsg](https://nanomsg.org/)  
**特征**：是一个“可扩展协议”的套接字库，它提供了几种常见的通信模式。可扩展协议的任务是定义多个应用系统如何通信，从而组成一个大的分布式系统。  

#### 要点

---