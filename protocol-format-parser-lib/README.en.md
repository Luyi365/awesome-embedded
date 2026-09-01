# Communication Protocol and Format Parsing Library
<!-- i18n:language-selector:start -->
[中文](README.md) | **English**
<!-- i18n:language-selector:end -->

> Communication overlaps somewhat with the [Board-Level Bus Protocol Library](../board-bus-lib/README.en.md), as both involve data transmission and processing. This section is listed separately to distinguish multi-device communication protocols with a "client - server" model, such as network and Bluetooth protocols.

## Web Server

### LightTPD

[![GitHub Repo stars](https://img.shields.io/github/stars/lighttpd/lighttpd1.4)](https://github.com/lighttpd/lighttpd1.4/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/lighttpd/lighttpd1.4)](https://github.com/lighttpd/lighttpd1.4/commits) | [![GitHub License](https://img.shields.io/github/license/lighttpd/lighttpd1.4)]()

**Link** - [Home - Lighttpd - fly light](https://www.lighttpd.net/)  
**Features** - A lightweight, high-performance open-source Web server designed for high-concurrency, low-memory-use scenarios. It is more suitable for embedded devices than Apache or Nginx.  

#### Key Points

- Includes integrations such as CGI, FastCGI, Lua, and PHP;

---

### Mongoose

[![GitHub Repo stars](https://img.shields.io/github/stars/cesanta/mongoose)](https://github.com/cesanta/mongoose/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/cesanta/mongoose)](https://github.com/cesanta/mongoose/commits) | [![GitHub License](https://img.shields.io/github/license/cesanta/mongoose)]()

**Link** - [Embedded Web Server and Web UI Framework for Microcontrollers - Mongoose](https://mongoose.ws)  
**Features** - An event-driven networking library for C / C++. Besides the basic protocol stack, it includes HTTP and MQTT service protocols, runs on bare metal and RTOS, and includes a UI builder. Commercial use has paid restrictions.  

#### Key Points

---

### Boa

**Link** - [Boa Webserver](http://www.boa.org/)  
**Features** - A small open-source Web server for embedded applications. It has not been maintained since 2005 and has known security vulnerabilities, so it is not recommended.  

#### Key Points

---

## Web Plugin

### FastCGI

[![GitHub Repo stars](https://img.shields.io/github/stars/FastCGI-Archives/fcgi2)](https://github.com/FastCGI-Archives/fcgi2/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/FastCGI-Archives/fcgi2)](https://github.com/FastCGI-Archives/fcgi2/commits) | [![GitHub License](https://img.shields.io/github/license/FastCGI-Archives/fcgi2)]()

**Link** - [FastCGI.com Archives](https://fastcgi-archives.github.io/)  
**Features** - Improves traditional CGI performance and adds distributed-computing and multi-role features.  

#### Key Points

- CGI (Common Gateway Interface) is a standard protocol for interaction between a Web server and external programs. Reference: [CGI](./appendix.en.md#cgi)

---

### libevent

[![GitHub Repo stars](https://img.shields.io/github/stars/libevent/libevent)](https://github.com/libevent/libevent/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/libevent/libevent)](https://github.com/libevent/libevent/commits) | [![GitHub License](https://img.shields.io/github/license/libevent/libevent)]()

**Link** - [libevent](https://libevent.org)  
**Features** - An event-driven library for network servers, intended to replace event loops in event-driven network servers.  

#### Key Points

- Introduction: [Essential for Embedded Development: the Open-Source Event-Driven Library libevent](https://mp.weixin.qq.com/s/3K4E6lOEu00EE4-CyhdIPg)

---

### rtty

[![GitHub Repo stars](https://img.shields.io/github/stars/zhaojh329/rtty)](https://github.com/zhaojh329/rtty/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/zhaojh329/rtty)](https://github.com/zhaojh329/rtty/commits) | [![GitHub License](https://img.shields.io/github/license/zhaojh329/rtty)]()

**Link** - [zhaojh329/rtty: 🐛 Access your terminal from anywhere via the web.](https://github.com/zhaojh329/rtty)  
**Features** - Access a device terminal through the Web; suitable for embedded Linux and quite interesting.  

#### Key Points

---

### Nanomsg

[![GitHub Repo stars](https://img.shields.io/github/stars/nanomsg/nanomsg)](https://github.com/nanomsg/nanomsg/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/nanomsg/nanomsg)](https://github.com/nanomsg/nanomsg/commits) | [![GitHub License](https://img.shields.io/github/license/nanomsg/nanomsg)]()

**Link** - [About Nanomsg](https://nanomsg.org/)  
**Features** - A socket library for "scalability protocols" that provides several common communication patterns. Scalability protocols define how multiple application systems communicate to form a large distributed system.  

#### Key Points

---

### url

[![Gitee Repo stars](https://gitee.com/yikoulinux/url/badge/star.svg?theme=gvp)](https://gitee.com/yikoulinux/url/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/yikoulinux/url&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/yikoulinux/url&query=$.license&label=license)]()

**Link** - [url: A simple URL parsing algorithm implemented in C](https://gitee.com/yikoulinux/url)  
**Features** - A simple URL parsing module that can parse information from different segments.  

#### Key Points

- Introduction: [A Small Example of URL Parsing Implemented in C](https://mp.weixin.qq.com/s/gRErTrfOfx5RVwyGGXjrEQ)

---

### tiny-curl

[![License: GPL v3](https://img.shields.io/badge/license-GPL%20v3-orange.svg)](https://opensource.org/licenses/GPL-3.0)

**Link** - [tiny-curl](https://curl.se/tiny)
**Features** - A cURL library for embedded systems that supports only HTTP.

#### Key Points

- [What Is the cURL Command?](./appendix.en.md#what-is-the-curl-command)

---

## RPC

> RPC (Remote Procedure Call) is a way for programs on different computers to communicate as though they were calling local functions. For example, a server creates a service that other clients access through a port. Reference: [Writing an RPC From Scratch · Caffeinspiration](https://alexanderell.is/posts/rpc-from-scratch/)

### ERPC

[![Gitee Repo stars](https://gitee.com/simpost/ERPC-doc/badge/star.svg?theme=gvp)](https://gitee.com/simpost/ERPC-doc/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/simpost/ERPC-doc&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/simpost/ERPC-doc&query=$.license&label=license)]()

**Link** - [ERPC-doc: ERPC (Embedded Remote Procedure Call) is a simple, easy-to-use, efficient embedded remote-call framework. It implements remote calls and state notifications (the observer pattern), supports data encryption (with user-defined encryption algorithms), exception monitoring, and complete log-management methods. ERPC can simplify system design, reduce coupling between modules, and reduce dependencies between developers.](https://gitee.com/simpost/ERPC-doc)  
**Features** - A simple, easy-to-use, efficient remote-call framework.  

---

### EmbedXrpc

[![Gitee Repo stars](https://gitee.com/snikeguo/EmbedXrpc/badge/star.svg?theme=gvp)](https://gitee.com/snikeguo/EmbedXrpc/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/snikeguo/EmbedXrpc&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/snikeguo/EmbedXrpc&query=$.license&label=license)]()

**Link** - [EmbedXrpc: This is similar to Google's GRPC, but its application scenario is microcontrollers. RPC greatly simplifies development by removing the need to focus on protocol parsing and data serialization and deserialization. There has not yet been a practical RPC framework for microcontrollers, so the author decided to create one using C# for the IDL language, csscript, custom serialization and deserialization, and code generation. QQ group 134161401](https://gitee.com/snikeguo/EmbedXrpc)  
**Features** - An RPC communication protocol that enables business logic without focusing on the protocol itself and includes a code-generation tool.  

#### Key Points

---

### erpc

[![GitHub Repo stars](https://img.shields.io/github/stars/EmbeddedRPC/erpc)](https://github.com/EmbeddedRPC/erpc/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/EmbeddedRPC/erpc)](https://github.com/EmbeddedRPC/erpc/commits) | [![GitHub License](https://img.shields.io/github/license/EmbeddedRPC/erpc)]()

**Link** - [EmbeddedRPC/erpc: Embedded RPC](https://github.com/EmbeddedRPC/erpc)  
**Features** - An NXP open-source Remote Procedure Call (RPC) system for multi-chip embedded systems and heterogeneous multi-core SoCs.  

#### Key Points

---

## TCP/IP

### lwIP

[![License: BSD 2--Clause](https://img.shields.io/badge/license-BSD%202--Clause-blue.svg)](https://opensource.org/licenses/BSD-2-Clause)

**Link** - [lwIP - A Lightweight TCP/IP stack - Summary \[Savannah\]](http://savannah.nongnu.org/projects/lwip/)  
**Features** - A small open-source TCP/IP stack and one of the most widely used embedded network stacks, present in most IoT systems.  

#### Key Points

- Guide: [\[Wildfire\] LwIP Application Development Practical Guide - Based on STM32](https://doc.embedfire.com/net/lwip/zh/latest/index.html)
- Official documentation: [lwIP: Overview](https://www.nongnu.org/lwip)；
- The contrib package contains demos for porting and using LwIP;
- The test folder in the source tree is not a demo; it contains source code for testing LwIP kernel performance and can provide many kernel-performance metrics, so it is only needed by specialists;
- The application layer does not include an MQTT service protocol;
- Source files in the directory:  
  ```plaintext
  lwip
   ┣ contrib                # Demo routines, mostly contributed by the open-source community
   ┣ doc                    # Related documentation and guides.
   ┣ src                    # Source files
   ┃ ┣ api                  # Sources for the NETCONN API and Socket API; suitable only for OS environments
   ┃ ┣ apps                 # Application sources, including httpd, mqtt, tftp, sntp, snmp, and more
   ┃ ┣ core                 # Kernel source files
   ┃ ┃ ┣ ipv4               # IPv4 module sources
   ┃ ┃ ┣ ipv6               # IPv6 module sources
   ┃ ┃ ┣ altcp_xxx.c        # Layered TCP connection API used from the TCP/IP thread; an abstraction that can emulate an application's TCP callback API
   ┃ ┃ ┣ def.c              # Basic functions such as host/network byte-order conversion, string lookup and comparison, and integer-to-string conversion
   ┃ ┃ ┣ dns.c              # Implements domain-name resolution
   ┃ ┃ ┣ inet_chksum.c      # Provides checksum functionality
   ┃ ┃ ┣ init.c             # Initialization function that also checks user macro configuration
   ┃ ┃ ┣ ip.c               # IP protocol functions; encapsulates functions in the ipv4 and ipv6 folders
   ┃ ┃ ┣ mem.c              # Implements dynamic memory-pool management  
   ┃ ┃ ┣ memp.c             # Implements static memory-heap management
   ┃ ┃ ┣ netif.c            # Implements network-interface operations
   ┃ ┃ ┣ pbuf.c             # Network-packet operations; packets use the pbuf structure and are key to network development with the RAW/Callback API
   ┃ ┃ ┣ raw.c              # A transport-layer protocol framework that can be modified and extended for custom transport protocols; like UDP/TCP, it can interact directly with the IP layer.
   ┃ ┃ ┣ stats.c            # Provides kernel statistics to view LwIP processing of network packets in real time
   ┃ ┃ ┣ sys.c              # Provides critical-section-related operations
   ┃ ┃ ┣ tcp_xxx.c          # Implements the TCP protocol
   ┃ ┃ ┣ timeouts.c         # Defines the kernel timeout-handling mechanism
   ┃ ┃ ┗ udp.c              # Implements the UDP protocol
   ┃ ┣ include              # Header files for all modules
   ┃ ┗ netif                # Porting templates for different network interfaces
   ┣ test                   # Source for testing kernel performance, only needed by specialists
   ┗ other                  # Iteration log, licenses, introduction, and more
  ```

---

### CycloneTCP

[![License: GPL v2](https://img.shields.io/badge/license-GPL%20v2-orange.svg)](https://opensource.org/licenses/GPL-2.0)

**Link** - [CycloneTCP | Embedded TCP/IP Stack for STM32, PIC32, ARM Cortex-M](https://www.oryx-embedded.com/products/CycloneTCP)  
**Features** - A dual IPv4/IPv6 stack for embedded applications that simplifies Internet deployment.  

#### Key Points

- Commercial use requires a license;

---

### onps

[![Gitee Repo stars](https://gitee.com/Neo-T/open-npstack/badge/star.svg?theme=gvp)](https://gitee.com/Neo-T/open-npstack/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Neo-T/open-npstack&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Neo-T/open-npstack&query=$.license&label=license)]()

**Link** - [Open-NPStack: onps is an open-source, independently developed domestic network protocol stack. Its design goal is the same as LwIp, and it targets resource-constrained microcontroller systems. It provides a complete tcp/ip protocol-family implementation and network tools such as sntp, dns, and ping; supports dynamic dhcp IP address assignment in Ethernet environments as well as dynamic and static routing tables. The stack also encapsulates a Berkeley sockets layer and is developed in ANSI C.](https://gitee.com/Neo-T/open-npstack)  
**Features** - A domestic network protocol stack with the same design goal as Lwip, for resource-constrained microcontroller systems, providing a complete ethernet/ppp/tcp/ip protocol-family implementation.  

#### Key Points

---

### wolfIP

[![GitHub Repo stars](https://img.shields.io/github/stars/wolfssl/wolfIP)](https://github.com/wolfssl/wolfIP/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/wolfssl/wolfIP)](https://github.com/wolfssl/wolfIP/commits) | [![GitHub License](https://img.shields.io/github/license/wolfssl/wolfIP)]()

**Link** - [wolfIP TCP/IP stack - wolfSSL](https://www.wolfssl.com/products/wolfip)
**Features** - A tiny TCP/IP stack with no dynamic memory allocation, intended as a better alternative to [lwIP](#lwip) and designed to work seamlessly with the [wolfSSL](../secure-boot-update-lib/README.en.md#wolfssl) library.

#### Key Points

---

### dyad

[![GitHub Repo stars](https://img.shields.io/github/stars/rxi/dyad)](https://github.com/rxi/dyad/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/rxi/dyad)](https://github.com/rxi/dyad/commits) | [![GitHub License](https://img.shields.io/github/license/rxi/dyad)]()

**Link** - [rxi/dyad: Asynchronous networking for C](https://github.com/rxi/dyad)  
**Features** - An asynchronous networking library based on Linux. It supports only TCP communication, for creating small standalone device servers and adding network support to existing projects.  

#### Key Points

- It is implemented using the Linux kernel and POSIX interfaces, so corresponding support is required to use it on bare metal or another OS;

---

## SSH

### tinyssh

[![GitHub Repo stars](https://img.shields.io/github/stars/janmojzis/tinyssh)](https://github.com/janmojzis/tinyssh/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/janmojzis/tinyssh)](https://github.com/janmojzis/tinyssh/commits) | [![GitHub License](https://img.shields.io/github/license/janmojzis/tinyssh)]()

**Link** - [janmojzis/tinyssh: TinySSH is a small server (fewer than 100000 lines of code)](https://github.com/janmojzis/tinyssh)  
**Features** - A minimalist SSH server implementing only a subset of SSHv2 features, suitable for embedded use.  

#### Key Points

---

### wolfSSH

[![GitHub Repo stars](https://img.shields.io/github/stars/wolfSSL/wolfssh)](https://github.com/wolfSSL/wolfssh/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/wolfSSL/wolfssh)](https://github.com/wolfSSL/wolfssh/commits) | [![GitHub License](https://img.shields.io/github/license/wolfSSL/wolfssh)]()

**Link** - [wolfSSH Lightweight SSH Library | Products - wolfSSL](https://www.wolfssl.com/products/wolfssh)
**Features** - A lightweight SSHv2 client and server library written in ANSI C.

#### Key Points

- Encryption and decryption require porting the [wolfCrypt](../secure-boot-update-lib//README.en.md#wolfcrypt) library or using [hardware support](https://www.wolfssl.com/docs/hardware-crypto-support);

---

## HTTP

### libevhtp

[![GitHub Repo stars](https://img.shields.io/github/stars/Yellow-Camper/libevhtp)](https://github.com/Yellow-Camper/libevhtp/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/Yellow-Camper/libevhtp)](https://github.com/Yellow-Camper/libevhtp/commits) | [![GitHub License](https://img.shields.io/github/license/Yellow-Camper/libevhtp)]()

**Link** - [Yellow-Camper/libevhtp: Create extremely-fast and secure embedded HTTP servers with ease.](https://github.com/Yellow-Camper/libevhtp)  
**Features** - A low-overhead HTTP library for embedded devices.  

#### Key Points

- Introduction: [An HTTP Library Designed Specifically for Embedded Systems](https://mp.weixin.qq.com/s/-d6r6Dbt888s6WozSDFTbQ)

---

## MQTT

### Paho MQTT

[![GitHub Repo stars](https://img.shields.io/github/stars/eclipse-paho/paho.mqtt.embedded-c)](https://github.com/eclipse-paho/paho.mqtt.embedded-c/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/eclipse-paho/paho.mqtt.embedded-c)](https://github.com/eclipse-paho/paho.mqtt.embedded-c/commits) | [![GitHub License](https://img.shields.io/github/license/eclipse-paho/paho.mqtt.embedded-c)]()

**Link** - [eclipse/paho.mqtt.embedded-c: Paho MQTT C client library for embedded systems. Paho is an Eclipse IoT project](https://github.com/eclipse-paho/paho.mqtt.embedded-c)  
**Features** - An MQTT library for embedded platforms, containing three sublibraries: packet serialization, C clients, and C++ clients.

#### Key Points

---

### mqttclient

[![GitHub Repo stars](https://img.shields.io/github/stars/IoTSharp/mqttclient)](https://github.com/IoTSharp/mqttclient/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/IoTSharp/mqttclient)](https://github.com/IoTSharp/mqttclient/commits) | [![GitHub License](https://img.shields.io/github/license/IoTSharp/mqttclient)]()

**Link** - [jiejieTop/mqttclient: A high-performance, high-stability, cross-platform MQTT client, developed based on the socket API, can be used on embedded devices (FreeRTOS / LiteOS / RT-Thread / TencentOS tiny), Linux, Windows, Mac, with a very concise The API interface realizes the quality of service of QOS2 with very few resources, and seamlessly connects the mbedtls encryption library.](https://github.com/IoTSharp/mqttclient)  
**Features** - A high-performance, highly stable cross-platform MQTT client with a concise API, seamless integration with the [Mbed TLS](../secure-boot-update-lib/README.en.md#mbed-tls) library, and an online code-generation tool.  

#### Key Points

---

### Mosquitto

[![GitHub Repo stars](https://img.shields.io/github/stars/eclipse-mosquitto/mosquitto)](https://github.com/eclipse-mosquitto/mosquitto/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/eclipse-mosquitto/mosquitto)](https://github.com/eclipse-mosquitto/mosquitto/commits) | [![GitHub License](https://img.shields.io/github/license/eclipse-mosquitto/mosquitto)]()

**Link** - [Eclipse Mosquitto](https://mosquitto.org/)  
**Features** - An open-source message broker from Eclipse, mainly used to implement MQTT. Its lightweight design and low resource usage make it suitable for enterprise IoT projects.  

#### Key Points

---

### wolfMQTT

[![GitHub Repo stars](https://img.shields.io/github/stars/wolfSSL/wolfMQTT)](https://github.com/wolfSSL/wolfMQTT/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/wolfSSL/wolfMQTT)](https://github.com/wolfSSL/wolfMQTT/commits) | [![GitHub License](https://img.shields.io/github/license/wolfSSL/wolfMQTT)]()

**Link** - [wolfMQTT Client Library | Products - wolfSSL](https://www.wolfssl.com/products/wolfmqtt)
**Features** - A lightweight MQTT protocol client library supporting multiple platforms.

#### Key Points

- SSL/TLS support can be implemented through the [wolfSSL](../secure-boot-update-lib/README.en.md#wolfssl) library;

---

## Thread

### OpenThread

[![GitHub Repo stars](https://img.shields.io/github/stars/openthread/openthread)](https://github.com/openthread/openthread/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/openthread/openthread)](https://github.com/openthread/openthread/commits) | [![GitHub License](https://img.shields.io/github/license/openthread/openthread)]()

**Link** - [OpenThread](https://openthread.io/?hl=en)  
**Features** - Google's open-source implementation of Thread.  

#### Key Points

- Reference: [Thread - ESP32 - ESP-IDF Programming Guide latest documentation](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/api-reference/network/esp_openthread.html)  
  ESP wrapper layer: [esp-idf/components/openthread at be06a6f5ffe36f9554cfc91fe2036e0fc85fea60 · espressif/esp-idf](https://github.com/espressif/esp-idf/tree/be06a6f5ffe36f9554cfc91fe2036e0fc85fea60/components/openthread)；

---

## Bluetooth

### bluetooth\_stack

[![GitHub Repo stars](https://img.shields.io/github/stars/sj15712795029/bluetooth_stack)](https://github.com/sj15712795029/bluetooth_stack/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/sj15712795029/bluetooth_stack)](https://github.com/sj15712795029/bluetooth_stack/commits) | [![GitHub License](https://img.shields.io/github/license/sj15712795029/bluetooth_stack)]()

**Link** - [sj15712795029/bluetooth_stack: An open-source dual-mode Bluetooth protocol stack (bluetooth.stack)(btstack) that runs on STM32 and Linux. It includes HCI, L2CAP, SDP, RFCOMM, HFP, SPP, A2DP, AVRCP, AVDTP, AVCTP, OBEX, PBAP, and other protocols, and will continue to be maintained for commercial use.](https://github.com/sj15712795029/bluetooth_stack)  
**Features** - An open-source low-power dual-mode Bluetooth protocol stack for learning; its author provides many tutorials.  

#### Key Points

---

### BTstack

[![GitHub Repo stars](https://img.shields.io/github/stars/bluekitchen/btstack)](https://github.com/bluekitchen/btstack/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/bluekitchen/btstack)](https://github.com/bluekitchen/btstack/commits) | [![GitHub License](https://img.shields.io/github/license/bluekitchen/btstack)]()

**Link** - [BlueKitchen – BlueKitchen GmbH | Qualified Dual-mode Bluetooth Stack – Available in Source Code](https://bluekitchen-gmbh.com/)  
**Features** - A lightweight, open-source Bluetooth protocol stack designed for embedded systems and resource-constrained devices, suited to low-power and high-flexibility scenarios.  

#### Key Points

---

### NimBLE

[![GitHub Repo stars](https://img.shields.io/github/stars/apache/mynewt-nimble)](https://github.com/apache/mynewt-nimble/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/apache/mynewt-nimble)](https://github.com/apache/mynewt-nimble/commits) | [![GitHub License](https://img.shields.io/github/license/apache/mynewt-nimble)]()

**Link** - [apache/mynewt-nimble: Apache mynewt](https://github.com/apache/mynewt-nimble)  
**Features** - An open-source Bluetooth protocol stack (including host and controller) separated from Apache Mynewt; it completely replaces the proprietary SoftDevice on Nordic chipsets.  

#### Key Points

- Modified and ported by RT-Thread: [RT-Thread-packages/nimble: An Apache open-source Bluetooth 5.0 stack porting on RT-Thread](https://github.com/RT-Thread-packages/nimble)；

---

## GNSS

> [ESA's summary of related open-source projects](https://www.esa.int/Enabling_Support/Space_Engineering_Technology/Radio_Frequency_Systems/Open_Source_Software_Resources_for_Space_Downstream_Applications%20#Table1)

### LwGPS

[![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwgps)](https://github.com/MaJerle/lwgps/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwgps)](https://github.com/MaJerle/lwgps/commits) | [![GitHub License](https://img.shields.io/github/license/MaJerle/lwgps)]()

**Link** - [LwGPS latest-develop documentation — LwGPS documentation](https://docs.majerle.eu/projects/lwgps/en/latest/)  
**Features** - A simple NMEA message parsing library with built-in support for four GPS messages: GPGGA, GPGSA, GPGSV, and GPRMC; custom messages are also supported.  

#### Key Points

---

### RTKLIB

[![GitHub Repo stars](https://img.shields.io/github/stars/tomojitakasu/RTKLIB)](https://github.com/tomojitakasu/RTKLIB/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/tomojitakasu/RTKLIB)](https://github.com/tomojitakasu/RTKLIB/commits) | [![GitHub License](https://img.shields.io/github/license/tomojitakasu/RTKLIB)]()

**Link** - [GitHub - tomojitakasu/RTKLIB · GitHub](https://github.com/tomojitakasu/RTKLIB)  
**Version for low-cost GNSS receivers** - [GitHub - rtklibexplorer/RTKLIB: A version of RTKLIB optimized for low cost GNSS receivers, especially u-blox receivers. It is based on RTKLIB 2.4.3. This software is provided “AS IS” without any warranties of any kind so please be careful, especially if using it in any kind of real-time application. Click on the "Releases" label below to see the latest Windows pre-release. · GitHub](https://github.com/rtklibexplorer/RTKLIB)  
**Version optimized for smartphone GNSS chips** - [GitHub - salmoshu/MobileGNSS-SPP: An EKF-based SPP system optimized for smartphone · GitHub](https://github.com/salmoshu/MobileGNSS-SPP)  
**Features** - A benchmark library in the RTK field, widely used commercially and by the community, and also a textbook-style reference manual.  

#### Key Points

- Main functions of source files in the *src* directory:  
  ```plaintext
  src
  ├── rcv                # Parses proprietary binary formats of GNSS receivers from different vendors
  │   ├── binex.c        # Decodes BINEX (Binary Exchange) common-format data
  │   ├── crescent.c     # Decodes Crescent receiver data
  │   ├── javad.c        # Decodes JAVAD receiver data
  │   ├── novatel.c      # Decodes NovAtel receiver binary formats (such as OEM4/5/6/7)
  │   ├── nvs.c          # Decodes NVS receiver data
  │   ├── rt17.c         # Decodes Trimble RT17/RT27 format data
  │   ├── septentrio.c   # Decodes Septentrio receiver data
  │   ├── skytraq.c      # Decodes SkyTraq receiver data
  │   ├── ss2.c          # Decodes NovAtel Superstar II receiver data
  │   └── ublox.c        # Decodes u-blox receiver UBX binary data
  ├── convgpx.c          # Converts positioning results to GPX format
  ├── convkml.c          # Converts positioning results to KML (Google Earth) format
  ├── convrnx.c          # RINEX format conversion tool (such as compression and version conversion)
  ├── datum.c            # Geodetic datum conversion parameters and functions
  ├── download.c         # Automatically downloads precise ephemeris, ionosphere products, and other files from the Internet (FTP/HTTP)
  ├── ephemeris.c        # Calculates broadcast ephemerides (satellite position, velocity, and clock error)
  ├── geoid.c            # Calculates geoid models (such as EGM96) for elevation conversion
  ├── gis.c              # GIS helper functions (such as coordinate projection conversion)
  ├── ionex.c            # Reads and interpolates IONEX-format ionospheric TEC maps
  ├── lambda.c           # Implements the LAMBDA method for fast integer-ambiguity search and fixing
  ├── options.c          # Parses and handles command-line and configuration-file parameters
  ├── pntpos.c           # Single-point positioning module; calculates approximate receiver position and clock error and supplies an initial value for high-precision positioning
  ├── postpos.c          # Main post-processing positioning program; coordinates data input, solving, and output
  ├── ppp.c              # Implements the precise point positioning (PPP) algorithm
  ├── ppp_ar.c           # PPP ambiguity-resolution (PPP-AR) algorithm
  ├── preceph.c          # Reads and interpolates precise ephemerides (SP3 format)
  ├── rcvraw.c           # Raw observation-data input and interface management; invokes decoders in rcv/
  ├── rinex.c            # Reads and generates RINEX-format observations/navigation messages
  ├── rtcm.c             # RTCM common functions and version-compatible interfaces
  ├── rtcm2.c            # RTCM SC-104 version 2.x differential-data encoder/decoder
  ├── rtcm3.c            # RTCM SC-104 version 3.x differential-data encoder/decoder (basic)
  ├── rtcm3e.c           # Extended RTCM 3.x message support (such as MSM)
  ├── rtkcmn.c           # Common function library
  ├── rtklib.h           # Main header (defines all structures, constants, and function prototypes)
  ├── rtkpos.c           # RTK positioning core; invokes pntpos, relpos, and others for real-time/post-processing position solutions
  ├── rtksvr.c           # RTK server core; handles multi-base-station input, generates differential corrections, and broadcasts them
  ├── sbas.c             # SBAS data parsing and correction application
  ├── solution.c         # Position-solution management, filtering, and output formatting
  ├── stream.c           # Data-stream handling (serial ports, TCP/IP, NTRIP, and file I/O)
  ├── streamsvr.c        # Stream-server features, including multi-client connections and data forwarding
  ├── tides.c            # Earth-tide corrections (solid Earth tides, ocean tides, and pole tides)
  └── tle.c              # Parses TLE two-line orbital elements for low-precision satellite-position calculation (mainly GLONASS)
  ```
- RTKLIB-derived projects and learning resources: [rtkexplorer – Exploring low cost solutions for high precision GPS/GNSS](https://rtkexplorer.com/)
- Chinese translation and usage guide for this library: [Winchell](https://salmoshu.github.io/)

---

### Ntrip

[![GitHub Repo stars](https://img.shields.io/github/stars/ybzwyrcld/ntrip)](https://github.com/ybzwyrcld/ntrip/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/ybzwyrcld/ntrip)](https://github.com/ybzwyrcld/ntrip/commits) | [![GitHub License](https://img.shields.io/github/license/ybzwyrcld/ntrip)]()

**Link** - [GitHub - ybzwyrcld/ntrip: Simple ntrip caster/client/server example programs, using the NTRIP2.0 protocol](https://github.com/ybzwyrcld/ntrip)  
**Features** - A simple Ntrip protocol library written in C++, including a rover (Client)<sup>(Rover)</sup>, central server (Caster), and reference station (CORS)<sup>(Server)</sup>.  

#### Key Points

---

## AT

### AT Command

[![Gitee Repo stars](https://gitee.com/moluo-tech/AT-Command/badge/star.svg?theme=gvp)](https://gitee.com/moluo-tech/AT-Command/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/moluo-tech/AT-Command&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/moluo-tech/AT-Command&query=$.license&label=license)]()

**Link** - [AT Command: A component for managing AT command communication interactions, suitable for Modem, WIFI modules, Bluetooth, and other scenarios that use AT commands or ASCII command-line communication.](https://gitee.com/moluo-tech/AT-Command)  
**Features** - An AT command communication parsing module for Modem, WIFI modules, Bluetooth, and other scenarios using AT commands or ASCII command-line communication.  

#### Key Points

- Available as OS and bare-metal modules;
- Introduction: [An AT Command Communication Parsing Module!](https://mp.weixin.qq.com/s/XFrq6t5kjOOQUqhaZfmNGA)

---

### Xradio\_atcmd

[![GitHub Repo stars](https://img.shields.io/github/stars/XradioTech/xradio-skylark-sdk)](https://github.com/XradioTech/xradio-skylark-sdk/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/XradioTech/xradio-skylark-sdk?path=src/atcmd)](https://github.com/XradioTech/xradio-skylark-sdk/commits/master/src/atcmd) | [![GitHub License](https://img.shields.io/github/license/XradioTech/xradio-skylark-sdk)]()

**Link** - [xradio-skylark-sdk/src/atcmd at master · XradioTech/xradio-skylark-sdk](https://github.com/XradioTech/xradio-skylark-sdk/tree/master/src/atcmd), [xradio-skylark-sdk/include/atcmd at master · XradioTech/xradio-skylark-sdk](https://github.com/XradioTech/xradio-skylark-sdk/tree/master/include/atcmd)  
**Features** - An AT command parsing library extracted from the Xradio SDK, with abundant command examples and based on RTOS.  

#### Key Points

- Demo: [xradio-skylark-sdk/project/demo/at_demo at master · XradioTech/xradio-skylark-sdk](https://github.com/XradioTech/xradio-skylark-sdk/tree/master/project/demo/at_demo)；
- Some dependent libraries are based on other SDK files;

---

## Base64

> Reference: [Embedded Miscellany Weekly | Issue 14](https://mp.weixin.qq.com/s/iF2GuG1hDBeNJyxBCfqn8A)  
>
> base64 is arguably the simplest encoding and decoding method. It can act as an intermediate layer for device-side transmission to hide transport differences.  
>
> There are also many base64 source libraries online; choose one as needed.  

### base64

[![Gitee Repo stars](https://gitee.com/ylguo/base64/badge/star.svg?theme=gvp)](https://gitee.com/ylguo/base64/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/ylguo/base64&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/ylguo/base64&query=$.license&label=license)]()

**Link** - [base64: A base64 encoding and decoding algorithm implemented in C](https://gitee.com/ylguo/base64)  
**Features** - An extremely simple base64 encoding and decoding library.  

#### Key Points

---

### base64

[![GitHub Repo stars](https://img.shields.io/github/stars/aklomp/base64)](https://github.com/aklomp/base64/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/aklomp/base64)](https://github.com/aklomp/base64/commits) | [![GitHub License](https://img.shields.io/github/license/aklomp/base64)]()

**Link** - [aklomp/base64: Fast Base64 stream encoder/decoder in C99, with SIMD acceleration](https://github.com/aklomp/base64)  
**Features** - A base64 encoding and decoding library with SIMD and OpenMP acceleration, no dynamic memory use, and attention to thread safety.  

#### Key Points

---

## CSV

### MiniCSV

[![GitHub Repo stars](https://img.shields.io/github/stars/jedisct1/minicsv)](https://github.com/jedisct1/minicsv/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/jedisct1/minicsv)](https://github.com/jedisct1/minicsv/commits) | [![GitHub License](https://img.shields.io/github/license/jedisct1/minicsv)]()

**Link** - [jedisct1/minicsv: A tiny, fast, simple, single-file, BSD-licensed CSV parsing library in C.](https://github.com/jedisct1/minicsv)  
**Features** - A minimalist CSV parser that handles multiple lines, escaped characters in escaped rows and columns, blank lines, rows with a variable number of columns, and Windows or Unix-style line endings.  

#### Key Points

- Introduction: [Open-Source CSV Parsing Library in C: MiniCSV Usage Example](https://blog.csdn.net/whik1194/article/details/131490767)
- Does not use dynamic memory;
- Decodes and reads all content at once;

---

### CRStrLib

[![GitHub Repo stars](https://img.shields.io/github/stars/mushroom-x/CRStrLib)](https://github.com/mushroom-x/CRStrLib/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/mushroom-x/CRStrLib)](https://github.com/mushroom-x/CRStrLib/commits) | [![GitHub License](https://img.shields.io/github/license/mushroom-x/CRStrLib)]()

**Link** - [mushroom-x/CRStrLib: This project parses strings in csv and other formats in C, extracts values, and validates frame headers and trailers. It can be added to a microcontroller project or Arduino library functions.](https://github.com/mushroom-x/CRStrLib)  
**Features** - Parses strings in csv and other formats, extracts values, and validates frame headers and trailers.  

#### Key Points

---

### fast-cpp-csv-parser

[![GitHub Repo stars](https://img.shields.io/github/stars/ben-strasser/fast-cpp-csv-parser)](https://github.com/ben-strasser/fast-cpp-csv-parser/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/ben-strasser/fast-cpp-csv-parser)](https://github.com/ben-strasser/fast-cpp-csv-parser/commits) | [![GitHub License](https://img.shields.io/github/license/ben-strasser/fast-cpp-csv-parser)]()

**Link** - [ben-strasser/fast-cpp-csv-parser: fast-cpp-csv-parser](https://github.com/ben-strasser/fast-cpp-csv-parser)  
**Features** - A small, easy-to-use, fast, header-only CSV parser based on C++.  

#### Key Points

---

## INI

> `.ini` file format: [INI](./appendix.en.md#ini).

### libinimini

[![GitHub Repo stars](https://img.shields.io/github/stars/lovemengx/libinimini)](https://github.com/lovemengx/libinimini/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/lovemengx/libinimini)](https://github.com/lovemengx/libinimini/commits) | [![GitHub License](https://img.shields.io/github/license/lovemengx/libinimini)]()

**Link** - [lovemengx/libinimini: A minimalist ini parsing library for Android, Linux, Rtos, and microcontrollers](https://github.com/lovemengx/libinimini)  
**Features** - A minimalist ini parsing library for microcontrollers with controllable memory use. It supports the simplest key-value-pair file format.  

#### Key Points

---

### inih

[![GitHub Repo stars](https://img.shields.io/github/stars/benhoyt/inih)](https://github.com/benhoyt/inih/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/benhoyt/inih)](https://github.com/benhoyt/inih/commits) | [![GitHub License](https://img.shields.io/github/license/benhoyt/inih)]()

**Link** - [benhoyt/inih: Simple .INI file parser in C, good for embedded systems](https://github.com/benhoyt/inih)  
**Features** - An ini parsing library written in C and suitable for embedded systems, with syntax and parsing options.  

#### Key Points

- Introduction: [Embedded Miscellany Weekly | Issue 10](https://mp.weixin.qq.com/s/QAElgMjgHqEmO_V_TvuppA)

---

### iniparser

[![GitHub Repo stars](https://img.shields.io/github/stars/ndevilla/iniparser)](https://github.com/ndevilla/iniparser/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/ndevilla/iniparser)](https://github.com/ndevilla/iniparser/commits) | [![GitHub License](https://img.shields.io/github/license/ndevilla/iniparser)]()

**Link** - [ndevilla/iniparser: ini file parser](https://github.com/ndevilla/iniparser)  
**Features** - An ini parsing library written in C, portable to embedded systems and focused on thread safety.  

#### Key Points

- Introduction: [A Useful C Language .ini File Parsing Library - Alibaba Cloud Developer Community](https://developer.aliyun.com/article/1325467)

---

## TLV

> Protocol introduction: [TLV](./appendix.en.md#tlv).

### ITLV

**Link** - [ITLV: An optimized TLV (Tag, Length, Value) data format that is extremely simple and lightweight. Custom data formats can be built on it, and it includes CRC validation.](https://gitee.com/Luyi365/itlv)  
**Features** - An optimized TLV (Tag, Length, Value) data format that is extremely simple and lightweight. Custom data formats can be built on it, and it includes CRC validation.  

#### Key Points

- Introduction: [A Highly Flexible Protocol Format (with Code Examples)](https://mp.weixin.qq.com/s/z0Qr2D5yCpEiBPenYWrdOw)；

---

### tlv

[![GitHub Repo stars](https://img.shields.io/github/stars/skullboyer/TLV)](https://github.com/skullboyer/TLV/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/skullboyer/TLV)](https://github.com/skullboyer/TLV/commits) | [![GitHub License](https://img.shields.io/github/license/skullboyer/TLV)]()

**Link** - [skullboyer/TLV](https://github.com/skullboyer/TLV)  
**Features** - A TLV format encoding implementation.  

#### Key Points

- Introduction: [【TLV】 A TLV Encoding Implementation - Blog Garden](https://www.cnblogs.com/skullboyer/p/17982042)

---

## JSON

> ~~JSON file format: ((20230121192127-ajlkxif 'JSON'))~~ (pending release)

### cJSON

[![GitHub Repo stars](https://img.shields.io/github/stars/DaveGamble/cJSON)](https://github.com/DaveGamble/cJSON/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/DaveGamble/cJSON)](https://github.com/DaveGamble/cJSON/commits) | [![GitHub License](https://img.shields.io/github/license/DaveGamble/cJSON)]()

**Link** - [DaveGamble/cJSON: Ultralightweight JSON parser in ANSI C](https://github.com/DaveGamble/cJSON)  
**Features** - An ultralightweight JSON parser in ANSI C and also the most native JSON parsing library. It is somewhat cumbersome to use and not recommended for direct use.  

#### Key Points

- Introduction:
  [A Simple Introduction to JSON and Using the cJSON Library (Part 1)](https://www.jianshu.com/p/59eb2bd1aeea)  
  [Parsing cJSON and Generating JSON Files | Personal Blog](https://www.yanbinghu.com/2019/08/04/21364.html)  
- A json object can be json, a string, an array, and more.

---

### struct2json

![Gitee Repo stars](https://gitee.com/Armink/struct2json/badge/star.svg?theme=gvp) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Armink/struct2json&query=$.pushed_at&label=lastcommit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Armink/struct2json&query=$.license&label=license)

**Link** - [struct2json: A library for rapid conversion between C structures and JSON, quickly implementing serialization and deserialization of C structures](https://gitee.com/Armink/struct2json)  
**Features** - An extremely convenient library for rapid conversion between C structures and JSON, based on [cJSON](#cjson).  

#### Key Points

---

### cson

[![GitHub Repo stars](https://img.shields.io/github/stars/NevermindZZT/cson)](https://github.com/NevermindZZT/cson/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/NevermindZZT/cson)](https://github.com/NevermindZZT/cson/commits) | [![GitHub License](https://img.shields.io/github/license/NevermindZZT/cson)]()

**Link** - [NevermindZZT/cson: A json data mapping and parsing library based on C](https://github.com/NevermindZZT/cson)  
**Features** - A json-struct model parsing tool running on the C platform and based on [cJSON](#cjson). It makes JSON parsing more convenient.  

#### Key Points

---

### json

![Gitee Repo stars](https://gitee.com/Lamdonn/json/badge/star.svg?theme=gvp) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Lamdonn/json&query=$.pushed_at&label=lastcommit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Lamdonn/json&query=$.license&label=license)

**Link** - [json: A concise, efficient, flexible, and secure json interpreter in C](https://gitee.com/Lamdonn/json)  
**Features** - A simple and efficient C library for generating and parsing json, suitable for simple projects.  

#### Key Points

---

### JSMN

[![GitHub Repo stars](https://img.shields.io/github/stars/zserge/jsmn)](https://github.com/zserge/jsmn/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/zserge/jsmn)](https://github.com/zserge/jsmn/commits) | [![GitHub License](https://img.shields.io/github/license/zserge/jsmn)]()

**Link** - [zserge/jsmn: Jsmn is a world fastest JSON parser/tokenizer. This is the official repo replacing the old one at Bitbucket](https://github.com/zserge/jsmn)  
**Features** - An extremely compact and fast JSON parser with no dynamic memory allocation and no parsing correction.  

#### Key Points

- Note that parsing is one-way only, from JSON to C;
- It records the key-value location of each json and does not create copies for parsing, so it is very space-efficient;

---

### lwjson

[![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwjson)](https://github.com/MaJerle/lwjson/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwjson)](https://github.com/MaJerle/lwjson/commits) | [![GitHub License](https://img.shields.io/github/license/MaJerle/lwjson)]()

**Link** - [LwJSON latest-develop documentation — LwJSON documentation](https://docs.majerle.eu/projects/lwjson/en/latest/)  
**Features** - A general JSON parser library optimized for embedded systems.  

#### Key Points

- Note that parsing is one-way only, from JSON to C;

---

### MojoJson

[![GitHub Repo stars](https://img.shields.io/github/stars/scottcgi/MojoJson)](https://github.com/scottcgi/MojoJson/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/scottcgi/MojoJson)](https://github.com/scottcgi/MojoJson/commits) | [![GitHub License](https://img.shields.io/github/license/scottcgi/MojoJson)]()

**Link** - [scottcgi/MojoJson: A simple and fast JSON parser.](https://github.com/scottcgi/MojoJson)  
**Features** - A general JSON parser library implemented with object-oriented ideas and providing a C version.  

#### Key Points

- Note that parsing is one-way only, from JSON to C;

---

### LJSON

![Gitee Repo stars](https://gitee.com/lengjingzju/json/badge/star.svg?theme=gvp) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/lengjingzju/json&query=$.pushed_at&label=lastcommit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/lengjingzju/json&query=$.license&label=license)

**Link** - [json: LJSON is a JSON library implemented in C that is much faster than cJSON (up to 20 times faster) and RapidJSON (up to 1 time faster), and is currently the fastest general JSON library. LJSON supports JSON parsing, printing, and editing; provides DOM and SAX interfaces; supports strings and files for I/O; and fully supports nativejson-benchmark test cases.](https://gitee.com/lengjingzju/json)  
**Features** - Claimed to be the fastest JSON parser library, with extremely powerful features covering nearly all JSON parsing needs.  

#### Key Points

---

### json-parser

[![GitHub Repo stars](https://img.shields.io/github/stars/Barenboim/json-parser)](https://github.com/Barenboim/json-parser/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/Barenboim/json-parser)](https://github.com/Barenboim/json-parser/commits) | [![GitHub License](https://img.shields.io/github/license/Barenboim/json-parser)]()

**Link** - [Barenboim/json-parser: JSON parser in standard C](https://github.com/Barenboim/json-parser)  
**C++ version** - [wfrest/Json: c++ Json library](https://github.com/wfrest/Json)  
**Features** - A simple, standard, practical JSON library for parsing and generation.  

#### Key Points

---

### Frozen

[![GitHub Repo stars](https://img.shields.io/github/stars/cesanta/frozen)](https://github.com/cesanta/frozen/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/cesanta/frozen)](https://github.com/cesanta/frozen/commits) | [![GitHub License](https://img.shields.io/github/license/cesanta/frozen)]()

**Link** - [cesanta/frozen: JSON parser and generator for C/C++ with scanf/printf like interface. Targeting embedded systems.](https://github.com/cesanta/frozen)  
**Features** - A JSON parsing and generation library with a scanf/printf-like interface, including a base64 encoder and binary data decoder.  

#### Key Points

---

### sj.h

[![GitHub Repo stars](https://img.shields.io/github/stars/rxi/sj.h)](https://github.com/rxi/sj.h/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/rxi/sj.h)](https://github.com/rxi/sj.h/commits) | [![GitHub License](https://img.shields.io/github/license/rxi/sj.h)]()

**Link** - [GitHub - rxi/sj.h: A tiny little JSON parsing library](https://github.com/rxi/sj.h)  
**Features** - A minimalist JSON parsing library in C using a zero-copy strategy that parses the original data directly.  

#### Key Points

---

## XML

### simple\_xml

![Gitee Repo stars](https://gitee.com/xfwangqiang/simple_xml/badge/star.svg?theme=gvp) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/xfwangqiang/simple_xml&query=$.pushed_at&label=lastcommit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/xfwangqiang/simple_xml&query=$.license&label=license)

**Link** - [simple_xml: An XML parser in C. Existing open-source parsers are tied to operating systems, making XML files difficult to use on less common and embedded operating systems. This project aims to develop code that can be used on multiple platforms.](https://gitee.com/xfwangqiang/simple_xml)  
**Features** - An XML parsing library with complete functionality and bidirectional parsing support.  

#### Key Points

---

### TinyXML-2

[![GitHub Repo stars](https://img.shields.io/github/stars/leethomason/tinyxml2)](https://github.com/leethomason/tinyxml2/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/leethomason/tinyxml2)](https://github.com/leethomason/tinyxml2/commits) | [![GitHub License](https://img.shields.io/github/license/leethomason/tinyxml2)]()

**Link** - [leethomason/tinyxml2: TinyXML2 is a simple, small, efficient, C++ XML parser that can be easily integrated into other programs.](https://github.com/leethomason/tinyxml2)  
**Features** - An XML parsing library based on C++. It uses a document object model (DOM) and can conveniently convert between XML and C++ objects.  

#### Key Points

---

## TOML

### toml

**Link** - [TOML: Tom's Obvious, Minimal Language](https://toml.io/en/)  
**Features** - A data markup format that is more extensible than INI and lacks the deeply nested JSON and YAML indentation syntax; it is not widely known.  

#### Key Points

---

## Other Formats

### LwPKT

[![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwpkt)](https://github.com/MaJerle/lwpkt/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwpkt)](https://github.com/MaJerle/lwpkt/commits) | [![GitHub License](https://img.shields.io/github/license/MaJerle/lwpkt)]()

**Link** - [LwPKT latest-develop documentation — LwPKT documentation](https://docs.majerle.eu/projects/lwpkt/en/latest/)  
**Features** - A general packet protocol library with variable data lengths and theoretically unlimited packet length. It allows multiple annotations using sender and receiver addresses on a network and includes CRC validation.  

#### Key Points

- Introduction: [A Lightweight Communication Protocol Tool for Embedded Systems!](https://mp.weixin.qq.com/s/e_yvMNMILzvpLtvmDw3iCw)
- Use the [LwRB](../algo-ai-lib/README.en.md) library for data read/write operations;

---

### xpack

[![GitHub Repo stars](https://img.shields.io/github/stars/xyz347/xpack)](https://github.com/xyz347/xpack/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/xyz347/xpack)](https://github.com/xyz347/xpack/commits) | [![GitHub License](https://img.shields.io/github/license/xyz347/xpack)]()

**Link** - [xyz347/xpack: convert json/xml/bson to c++ struct](https://github.com/xyz347/xpack)  
**Features** - Converts between C++ structures and JSON/XML/YAML/BSON/MySQL/SQLite; header-only.

#### Key Points

---

### Uart\_Transfer\_BIN\_to\_exFlash

[![GitHub Repo stars](https://img.shields.io/github/stars/firestaradmin/Uart_Transfer_BIN_to_exFlash)](https://github.com/firestaradmin/Uart_Transfer_BIN_to_exFlash/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/firestaradmin/Uart_Transfer_BIN_to_exFlash)](https://github.com/firestaradmin/Uart_Transfer_BIN_to_exFlash/commits) | [![GitHub License](https://img.shields.io/github/license/firestaradmin/Uart_Transfer_BIN_to_exFlash)]()

**Link** - [firestaradmin/Uart_Transfer_BIN_to_exFlash: STM32 serial-port programming of BIN files and font files \[QT host application\]](https://github.com/firestaradmin/Uart_Transfer_BIN_to_exFlash)  
**Features** - Adds frame attributes to serial communication, enabling convenient and reliable data transfer to Flash.  

#### Key Points

---
