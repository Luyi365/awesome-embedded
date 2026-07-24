# 通信协议与端侧库

> 通信的概念与[板级总线协议库](../board-bus-lib/README.md)及[格式解析与数据库](../db-format-parser-lib/README.md)存在一定的交集，都会涉及到数据传输及处理。但我们这里单独再列出来，主要是区分带有「客户端 - 服务端」这样的多端侧设备通信协议，比较典型像网络协议、蓝牙协议等。

## Web-Server

### LightTPD

[![GitHub Repo stars](https://img.shields.io/github/stars/lighttpd/lighttpd1.4)](https://github.com/lighttpd/lighttpd1.4/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/lighttpd/lighttpd1.4)](https://github.com/lighttpd/lighttpd1.4/commits) | [![GitHub License](https://img.shields.io/github/license/lighttpd/lighttpd1.4)]()

**链接**：[Home - Lighttpd - fly light](https://www.lighttpd.net/)  
**特征**：是一个轻量级、高性能的 开源 Web 服务器，专为高并发、低内存占用 的场景设计。相比Apache 或 Nginx更适合嵌入式设备。  

#### 要点

- 带有（CGI、FastCGI、Lua、PHP）等集成功能；

---

### Mongoose

[![GitHub Repo stars](https://img.shields.io/github/stars/cesanta/mongoose)](https://github.com/cesanta/mongoose/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/cesanta/mongoose)](https://github.com/cesanta/mongoose/commits) | [![GitHub License](https://img.shields.io/github/license/cesanta/mongoose)]()

**链接**：[Embedded Web Server and Web UI Framework for Microcontrollers - Mongoose](https://mongoose.ws)  
**特征**：C / C++的事件驱动网络库，除了基本协议栈还了内置HTTP、MQTT等服务协议，可在裸机及RTOS上运行，带有UI构建器。商用有付费限制。  

#### 要点

---

### Boa

**链接**：[Boa Webserver](http://www.boa.org/)  
**特征**：开源的小型Web服务器，适用于嵌入式应用。于2005起不再更新维护，目前存在已知安全漏洞，不推荐使用。  

#### 要点

---

## Web-Plugin

### FastCGI

[![GitHub Repo stars](https://img.shields.io/github/stars/FastCGI-Archives/fcgi2)](https://github.com/FastCGI-Archives/fcgi2/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/FastCGI-Archives/fcgi2)](https://github.com/FastCGI-Archives/fcgi2/commits) | [![GitHub License](https://img.shields.io/github/license/FastCGI-Archives/fcgi2)]()

**链接**：[FastCGI.com Archives](https://fastcgi-archives.github.io/)  
**特征**：改进了传统CGI的性能，增加了分布式计算和多角色特性。  

#### 要点

- CGI（Common Gateway Interface）是一种 Web 服务器与外部程序进行交互的标准协议。参考：[CGI](./appendix.md#cgi)

---

### libevent

[![GitHub Repo stars](https://img.shields.io/github/stars/libevent/libevent)](https://github.com/libevent/libevent/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/libevent/libevent)](https://github.com/libevent/libevent/commits) | [![GitHub License](https://img.shields.io/github/license/libevent/libevent)]()

**链接**：[libevent](https://libevent.org)  
**特征**：专用于网络服务器的事件驱动库，旨在替换事件驱动网络服务器中的事件循环。  

#### 要点

- 使用介绍：[嵌入式开发必备：开源事件驱动库 libevent](https://mp.weixin.qq.com/s/3K4E6lOEu00EE4-CyhdIPg)

---

### rtty

[![GitHub Repo stars](https://img.shields.io/github/stars/zhaojh329/rtty)](https://github.com/zhaojh329/rtty/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/zhaojh329/rtty)](https://github.com/zhaojh329/rtty/commits) | [![GitHub License](https://img.shields.io/github/license/zhaojh329/rtty)]()

**链接**：[zhaojh329/rtty: 🐛 Access your terminal from anywhere via the web.](https://github.com/zhaojh329/rtty)  
**特征**：通过 Web 访问设备的终端，适合嵌入式 Linux，有点意思。  

#### 要点

---

### Nanomsg

[![GitHub Repo stars](https://img.shields.io/github/stars/nanomsg/nanomsg)](https://github.com/nanomsg/nanomsg/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/nanomsg/nanomsg)](https://github.com/nanomsg/nanomsg/commits) | [![GitHub License](https://img.shields.io/github/license/nanomsg/nanomsg)]()

**链接**：[About Nanomsg](https://nanomsg.org/)  
**特征**：是一个“可扩展协议”的套接字库，它提供了几种常见的通信模式。可扩展协议的任务是定义多个应用系统如何通信，从而组成一个大的分布式系统。  

#### 要点

---

### url

[![Gitee Repo stars](https://gitee.com/yikoulinux/url/badge/star.svg?theme=gvp)](https://gitee.com/yikoulinux/url/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/yikoulinux/url&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/yikoulinux/url&query=$.license&label=license)]()

**链接**：[url: 用 C 语言实现一个简单的解析 url 的算法](https://gitee.com/yikoulinux/url)  
**特征**：简单的解析 url 模块，可以解析不同段的信息。  

#### 要点

- 使用介绍：[分享一个 C 语言实现 url 解析的小实例](https://mp.weixin.qq.com/s/gRErTrfOfx5RVwyGGXjrEQ)

---

### tiny-curl

[![License: GPL v3](https://img.shields.io/badge/license-GPL%20v3-orange.svg)](https://opensource.org/licenses/GPL-3.0)

**链接**：[tiny-curl](https://curl.se/tiny)
**特征**：适用于嵌入式的 cURL 库，仅支持 HTTP 协议。

#### 要点

- [什么是 cURL 命令](./appendix.md#什么是-curl-命令)

---

## RPC

> 远程调用RPC（Remote Procedure Call）是一种让不同的计算机程序之间像本地调用函数一样通信的方式。例如服务器创建了一个服务，其他客户端通过端口访问服务。参考：[Writing an RPC From Scratch · Caffeinspiration](https://alexanderell.is/posts/rpc-from-scratch/)

### ERPC

[![Gitee Repo stars](https://gitee.com/simpost/ERPC-doc/badge/star.svg?theme=gvp)](https://gitee.com/simpost/ERPC-doc/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/simpost/ERPC-doc&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/simpost/ERPC-doc&query=$.license&label=license)]()

**链接**：[ERPC-doc: ERPC（Embedded Remote Procedure Call）是一个简单的、易用的、高效的嵌入式远程调用框架。它不仅实现了远程调用，还实现了状态通知（观察者模式），同时还支持数据加密（用户可自定义加密算法）、异常监控和完备的日志管理方法。使用ERPC可简化系统的设计难度，降低模块之间的耦合度，降低开发人员之间的依赖性。](https://gitee.com/simpost/ERPC-doc)  
**特征**：一个简单的、易用的、高效的远程调用框架。  

---

### EmbedXrpc

[![Gitee Repo stars](https://gitee.com/snikeguo/EmbedXrpc/badge/star.svg?theme=gvp)](https://gitee.com/snikeguo/EmbedXrpc/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/snikeguo/EmbedXrpc&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/snikeguo/EmbedXrpc&query=$.license&label=license)]()

**链接**：[EmbedXrpc: 这个东西类似于 Google 的 GRPC,但是应用场景是单片机。RPC 远程调用极大的方便了开发，使得不必关注于协议解析，数据的序列化和反序列化等繁琐的工作。可是目前还没有在单片机上实现好用的 RPC 框架，于是我就谋生了做这个 RPC 框架的想法，所用的技术是：C#做 IDL 语言 +csscript+ 自己实现序列化和反序列化 + 代码生成 QQ 群 134161401](https://gitee.com/snikeguo/EmbedXrpc)  
**特征**：通过RPC通讯协议，可忽略协议本身进行业务逻辑的实现，附带代码生成工具。  

#### 要点

---

### erpc

[![GitHub Repo stars](https://img.shields.io/github/stars/EmbeddedRPC/erpc)](https://github.com/EmbeddedRPC/erpc/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/EmbeddedRPC/erpc)](https://github.com/EmbeddedRPC/erpc/commits) | [![GitHub License](https://img.shields.io/github/license/EmbeddedRPC/erpc)]()

**链接**：[EmbeddedRPC/erpc: Embedded RPC](https://github.com/EmbeddedRPC/erpc)  
**特征**：是NXP开源的、用于多芯片嵌入式系统和异构多核SoC的开源远程过程调用（RPC）系统。  

#### 要点

---

## TCP/IP

### lwIP

[![License: BSD 2--Clause](https://img.shields.io/badge/license-BSD%202--Clause-blue.svg)](https://opensource.org/licenses/BSD-2-Clause)

**链接**：[lwIP - A Lightweight TCP/IP stack - Summary \[Savannah\]](http://savannah.nongnu.org/projects/lwip/)  
**特征**：小型开源的TCP/IP协议栈，使用最广泛的嵌入式网络协议栈，基本上物联网系统中都有它。  

#### 要点

- 指南：[\[野火\]LwIP应用开发实战指南—基于STM32 — \[野火\]LwIP应用开发实战指南—基于野火STM32 文档](https://doc.embedfire.com/net/lwip/zh/latest/index.html)
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

[![License: GPL v2](https://img.shields.io/badge/license-GPL%20v2-orange.svg)](https://opensource.org/licenses/GPL-2.0)

**链接**：[CycloneTCP | Embedded TCP/IP Stack for STM32, PIC32, ARM Cortex-M](https://www.oryx-embedded.com/products/CycloneTCP)  
**特征**：专用于嵌入式应用的双 IPv4/IPv6 栈，简化了互联网的部署。  

#### 要点

- 商用需授权；

---

### onps

[![Gitee Repo stars](https://gitee.com/Neo-T/open-npstack/badge/star.svg?theme=gvp)](https://gitee.com/Neo-T/open-npstack/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Neo-T/open-npstack&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Neo-T/open-npstack&query=$.license&label=license)]()

**链接**：[Open-NPStack: onps是一个开源且完全自主开发的国产网络协议栈。设计目标与LwIp相同，onps栈的目标系统同样是资源受限的单片机系统。提供完整的tcp/ip协议族实现，同时提供sntp、dns、ping等网络工具，支持以太网环境下dhcp动态ip地址申请，也支持动态及静态路由表。协议栈还封装实现了一个伯克利套接字（Berkeley sockets）层。协议栈使用ANSI C语言开发。](https://gitee.com/Neo-T/open-npstack)  
**特征**：国产网络协议栈，设计目标与Lwip相同，适用于资源受限的单片机系统，提供完整地ethernet/ppp/tcp/ip协议族实现。  

#### 要点

---

### wolfIP

[![GitHub Repo stars](https://img.shields.io/github/stars/wolfssl/wolfIP)](https://github.com/wolfssl/wolfIP/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/wolfssl/wolfIP)](https://github.com/wolfssl/wolfIP/commits) | [![GitHub License](https://img.shields.io/github/license/wolfssl/wolfIP)]()

**链接**：[wolfIP TCP/IP stack - wolfSSL](https://www.wolfssl.com/products/wolfip)
**特征**：无动态内存分配的微型 TCP/IP 协议栈，旨在提供比 [lwIP](#lwip) 更好的替代方案，并与 [wolfSSL](../secure-boot-update-lib/README.md#wolfssl) 库无缝配合。

#### 要点

---

### dyad

[![GitHub Repo stars](https://img.shields.io/github/stars/rxi/dyad)](https://github.com/rxi/dyad/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/rxi/dyad)](https://github.com/rxi/dyad/commits) | [![GitHub License](https://img.shields.io/github/license/rxi/dyad)]()

**链接**：[rxi/dyad: Asynchronous networking for C](https://github.com/rxi/dyad)  
**特征**：基于Linux的异步网络库，仅支持TCP 网络通讯，用于创建小型独立设备服务器，并为现有项目提供网络支持。  

#### 要点

- 可以看出来它是基于Linux系统的内核和POSIX接口实现的，如果要用在裸机或其他OS上则需要添加对应的支持才行；

---

## SSH

### tinyssh

[![GitHub Repo stars](https://img.shields.io/github/stars/janmojzis/tinyssh)](https://github.com/janmojzis/tinyssh/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/janmojzis/tinyssh)](https://github.com/janmojzis/tinyssh/commits) | [![GitHub License](https://img.shields.io/github/license/janmojzis/tinyssh)]()

**链接**：[janmojzis/tinyssh：TinySSH 是小型服务器（少于 100000 字代码）](https://github.com/janmojzis/tinyssh)  
**特征**：一个简约的 SSH 服务器，它只实现了 SSHv2 功能的子集，适合嵌入式使用。  

#### 要点

---

### wolfSSH

[![GitHub Repo stars](https://img.shields.io/github/stars/wolfSSL/wolfssh)](https://github.com/wolfSSL/wolfssh/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/wolfSSL/wolfssh)](https://github.com/wolfSSL/wolfssh/commits) | [![GitHub License](https://img.shields.io/github/license/wolfSSL/wolfssh)]()

**链接**：[wolfSSH Lightweight SSH Library | Products - wolfSSL](https://www.wolfssl.com/products/wolfssh)
**特征**：轻量级 SSHv2 客户端和服务器库，采用 ANSI C 编写。

#### 要点

- 加解密操作需要移植 [wolfCrypt](../secure-boot-update-lib//README.md#wolfcrypt) 库或[硬件支持](https://www.wolfssl.com/docs/hardware-crypto-support)来完成；

---

## HTTP

### libevhtp

[![GitHub Repo stars](https://img.shields.io/github/stars/Yellow-Camper/libevhtp)](https://github.com/Yellow-Camper/libevhtp/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/Yellow-Camper/libevhtp)](https://github.com/Yellow-Camper/libevhtp/commits) | [![GitHub License](https://img.shields.io/github/license/Yellow-Camper/libevhtp)]()

**链接**：[Yellow-Camper/libevhtp: Create extremely-fast and secure embedded HTTP servers with ease.](https://github.com/Yellow-Camper/libevhtp)  
**特征**：适合嵌入式设备的低负载HTTP库。  

#### 要点

- 使用介绍：[分享一款专为嵌入式系统设计的HTTP库](https://mp.weixin.qq.com/s/-d6r6Dbt888s6WozSDFTbQ)

---

## MQTT

### Paho MQTT

[![GitHub Repo stars](https://img.shields.io/github/stars/eclipse-paho/paho.mqtt.embedded-c)](https://github.com/eclipse-paho/paho.mqtt.embedded-c/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/eclipse-paho/paho.mqtt.embedded-c)](https://github.com/eclipse-paho/paho.mqtt.embedded-c/commits) | [![GitHub License](https://img.shields.io/github/license/eclipse-paho/paho.mqtt.embedded-c)]()

**链接**：[eclipse/paho.mqtt.embedded-c: Paho MQTT C client library for embedded systems. Paho is an Eclipse IoT project](https://github.com/eclipse-paho/paho.mqtt.embedded-c)  
**特征**：嵌入式平台的 MQTT 库，包含三个子库——数据包序列化、C及C++客户端。

#### 要点

---

### mqttclient

[![GitHub Repo stars](https://img.shields.io/github/stars/IoTSharp/mqttclient)](https://github.com/IoTSharp/mqttclient/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/IoTSharp/mqttclient)](https://github.com/IoTSharp/mqttclient/commits) | [![GitHub License](https://img.shields.io/github/license/IoTSharp/mqttclient)]()

**链接**：[jiejieTop/mqttclient: A high-performance, high-stability, cross-platform MQTT client, developed based on the socket API, can be used on embedded devices (FreeRTOS / LiteOS / RT-Thread / TencentOS tiny), Linux, Windows, Mac, with a very concise The API interface realizes the quality of service of QOS2 with very few resources, and seamlessly connects the mbedtls encryption library.](https://github.com/IoTSharp/mqttclient)  
**特征**：高性能、高稳定性的跨平台 MQTT 客户端，拥有简洁的 API，无缝衔接 [Mbed TLS](../secure-boot-update-lib/README.md#mbed-tls) 库，提供在线代码生成工具。  

#### 要点

---

### Mosquitto

[![GitHub Repo stars](https://img.shields.io/github/stars/eclipse-mosquitto/mosquitto)](https://github.com/eclipse-mosquitto/mosquitto/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/eclipse-mosquitto/mosquitto)](https://github.com/eclipse-mosquitto/mosquitto/commits) | [![GitHub License](https://img.shields.io/github/license/eclipse-mosquitto/mosquitto)]()

**链接**：[Eclipse Mosquitto](https://mosquitto.org/)  
**特征**：Eclipse 旗下的一个开源的消息代理（broker），主要用于实现 MQTT 协议。它设计轻巧，资源占用少，适合物联网领域的企业级项目。  

#### 要点

---

### wolfMQTT

[![GitHub Repo stars](https://img.shields.io/github/stars/wolfSSL/wolfMQTT)](https://github.com/wolfSSL/wolfMQTT/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/wolfSSL/wolfMQTT)](https://github.com/wolfSSL/wolfMQTT/commits) | [![GitHub License](https://img.shields.io/github/license/wolfSSL/wolfMQTT)]()

**链接**：[wolfMQTT Client Library | Products - wolfSSL](https://www.wolfssl.com/products/wolfmqtt)
**特征**：轻量化的 MQTT 协议客户端库，支持多个平台。

#### 要点

- 可以通过 [wolfSSL](../secure-boot-update-lib/README.md#wolfssl) 库实现 SSL/TLS 的支持；

---

## Thread

### OpenThread

[![GitHub Repo stars](https://img.shields.io/github/stars/openthread/openthread)](https://github.com/openthread/openthread/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/openthread/openthread)](https://github.com/openthread/openthread/commits) | [![GitHub License](https://img.shields.io/github/license/openthread/openthread)]()

**链接**：[OpenThread](https://openthread.io/?hl=zh-cn)  
**特征**：Google 旗下的产品，是Thread的开源实现。  

#### 要点

- 参考：[Thread - ESP32 - — ESP-IDF 编程指南 latest 文档](https://docs.espressif.com/projects/esp-idf/zh_CN/latest/esp32/api-reference/network/esp_openthread.html)  
  ESP的封装层：[esp-idf/components/openthread at be06a6f5ffe36f9554cfc91fe2036e0fc85fea60 · espressif/esp-idf](https://github.com/espressif/esp-idf/tree/be06a6f5ffe36f9554cfc91fe2036e0fc85fea60/components/openthread)；

---

## Bluetooth

### bluetooth\_stack

[![GitHub Repo stars](https://img.shields.io/github/stars/sj15712795029/bluetooth_stack)](https://github.com/sj15712795029/bluetooth_stack/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/sj15712795029/bluetooth_stack)](https://github.com/sj15712795029/bluetooth_stack/commits) | [![GitHub License](https://img.shields.io/github/license/sj15712795029/bluetooth_stack)]()

**链接**：[sj15712795029/bluetooth_stack: 这是一个开源的双模蓝牙协议栈(bluetooth.stack)(btstack),可以运行在STM32,Linux.，包含HCI,L2CAP,SDP,RFCOMM,HFP,SPP,A2DP,AVRCP,AVDTP,AVCTP,OBEX,PBAP等协议，后续会继续维护，以达到商用的目的](https://github.com/sj15712795029/bluetooth_stack)  
**特征**：一个开源的低功耗双模蓝牙协议栈，可以用于学习，作者有很多教程。  

#### 要点

---

### BTstack

[![GitHub Repo stars](https://img.shields.io/github/stars/bluekitchen/btstack)](https://github.com/bluekitchen/btstack/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/bluekitchen/btstack)](https://github.com/bluekitchen/btstack/commits) | [![GitHub License](https://img.shields.io/github/license/bluekitchen/btstack)]()

**链接**：[BlueKitchen – BlueKitchen GmbH | Qualified Dual-mode Bluetooth Stack – Available in Source Code](https://bluekitchen-gmbh.com/)  
**特征**：是一个轻量级、开源的 蓝牙协议栈，专为嵌入式系统和资源受限设备设计，适合需要低功耗、高灵活性的场景。  

#### 要点

---

### NimBLE

[![GitHub Repo stars](https://img.shields.io/github/stars/apache/mynewt-nimble)](https://github.com/apache/mynewt-nimble/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/apache/mynewt-nimble)](https://github.com/apache/mynewt-nimble/commits) | [![GitHub License](https://img.shields.io/github/license/apache/mynewt-nimble)]()

**链接**：[apache/mynewt-nimble： Apache mynewt](https://github.com/apache/mynewt-nimble)  
**特征**：从Apache Mynewt中分离出来的一个开源的蓝牙协议栈（包括主机和控制器） 完全取代了 Nordic 芯片组上的专有 SoftDevice。  

#### 要点

- RT-Thread将其进行了修改并移植：[RT-Thread-packages/nimble: An Apache open-source Bluetooth 5.0 stack porting on RT-Thread](https://github.com/RT-Thread-packages/nimble)；

---

## GNSS

> [ESA欧空局对相关开源项目的汇总](https://www.esa.int/Enabling_Support/Space_Engineering_Technology/Radio_Frequency_Systems/Open_Source_Software_Resources_for_Space_Downstream_Applications%20#Table1)

### LwGPS

[![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwgps)](https://github.com/MaJerle/lwgps/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwgps)](https://github.com/MaJerle/lwgps/commits) | [![GitHub License](https://img.shields.io/github/license/MaJerle/lwgps)]()

**链接**：[LwGPS latest-develop documentation — LwGPS documentation](https://docs.majerle.eu/projects/lwgps/en/latest/)  
**特征**：简易的 NMEA 报文解析库，内置支持 4 个 GPS 报文：GPGGA、GPGSA、GPGSV、GPRMC，以及允许自定义报文。  

#### 要点

---

### RTKLIB

[![GitHub Repo stars](https://img.shields.io/github/stars/tomojitakasu/RTKLIB)](https://github.com/tomojitakasu/RTKLIB/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/tomojitakasu/RTKLIB)](https://github.com/tomojitakasu/RTKLIB/commits) | [![GitHub License](https://img.shields.io/github/license/tomojitakasu/RTKLIB)]()

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

[![GitHub Repo stars](https://img.shields.io/github/stars/ybzwyrcld/ntrip)](https://github.com/ybzwyrcld/ntrip/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/ybzwyrcld/ntrip)](https://github.com/ybzwyrcld/ntrip/commits) | [![GitHub License](https://img.shields.io/github/license/ybzwyrcld/ntrip)]()

**链接**：[GitHub - ybzwyrcld/ntrip: Simple ntrip caster/client/server example programs, using the NTRIP2.0 protocol](https://github.com/ybzwyrcld/ntrip)  
**特征**：C++编写的简易Ntrip协议库，包含流动站（Client）<sup>(Rover)</sup>、中央服务器（Caster）、基准站（CORS）<sup>(Server)</sup>。  

#### 要点

---
