# Kernel and Foundation Framework Library
<!-- i18n:language-selector:start -->
[中文](README.md) | **English**
<!-- i18n:language-selector:end -->

> This library was originally split into two parts, but I later realized that combining kernels and frameworks essentially creates a system or toolkit, so they are grouped together. Some frameworks that are not strongly related to kernels are not included here, such as the [menu framework](../ui-menu-lib/README.md#菜单框架).  
> Code libraries involving relatively low-level functionality are also included here.  
>
> The three concepts of <ins>events</ins>, <ins>messages</ins>, and <ins>data</ins> are easy to confuse; their focuses are as follows:
>
> - **Events** - Focus on the occurrence of specific actions and callback response mechanisms;
> - **Messages** - Emphasize communication and data transfer between components;
> - **Data** - Involves how data is transferred within a program, without being limited to the context of messages or events.

## Events

### cpost

[![GitHub Repo stars](https://img.shields.io/github/stars/NevermindZZT/cpost)](https://github.com/NevermindZZT/cpost/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/NevermindZZT/cpost)](https://github.com/NevermindZZT/cpost/commits) | [![GitHub License](https://img.shields.io/github/license/NevermindZZT/cpost)]()

**Link** - [NevermindZZT/cpost](https://github.com/NevermindZZT/cpost)  
**Features** - An ultra-lightweight context-switching and task-decoupling library that uses event dispatching and is suitable for bare-metal systems.  

#### Key Points

- References: [Fast Context Switching in C | Letter](https://nevermindzzt.github.io/2020/12/27/c语言上下文的快速切换/) and [Perfect Decoupling for Modular Programming in C | Letter](https://nevermindzzt.github.io/2020/12/20/C语言模块化编程的完美解耦/)；
- The context switching here is equivalent to setting a flag in an interrupt and executing the corresponding task during polling;
- The library parameter `delay` refers not to time, but to the system "tick";
- This decoupling library uses event broadcasting, but it is not well suited to event-broadcasting purposes; it is intended for decoupling;
- The decoupling library depends on the compiler, which requires attention;
- Add the appropriate header files;

---

### LwEVT

[![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwevt)](https://github.com/MaJerle/lwevt/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwevt)](https://github.com/MaJerle/lwevt/commits) | [![GitHub License](https://img.shields.io/github/license/MaJerle/lwevt)]()

**Link** - [LwEVT latest-develop documentation — LwEVT documentation](https://docs.majerle.eu/projects/lwevt/en/latest/)  
**Features** - A professional event-module library with optional custom data types and attached specified functions; it can be understood as a combination of events and messages, handling event dispatching and callbacks.  

#### Key Points

- Introduction: [Recommended Lightweight Embedded Event Management Library!](https://mp.weixin.qq.com/s/KkV0pxVfb56Ig8HDMuwFaQ)
- Event enumerations are loaded using `LWEVT_TYPE_BASIC` and `LWEVT_TYPE_EXT` and placed separately in a header file.

---

## Messages

### YAMI4

**Link** - [Inspirel - YAMI4](http://www.inspirel.com/yami4/index.html)  
**Features** - A messaging library designed for distributed systems, with particular attention to control and monitoring systems.  

#### Key Points

- It is somewhat like a network protocol, also corresponding to clients and servers for sending and receiving data. Refer to the official introduction for the specific differences;
- The API has two parts: core and general. The core manages the most basic communication functions, including connection pools, message queues, and a frame assembly engine. Although this layer is highly simplified, it is fully sufficient for custom applications. The general layer, on the other hand, builds on the core services and adds thread management and higher-level interfaces, making it easier to use;
- Uses C++ and conforms to the POSIX interface;

---

### ZeroMQ

[![GitHub Repo stars](https://img.shields.io/github/stars/zeromq/czmq)](https://github.com/zeromq/czmq/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/zeromq/czmq)](https://github.com/zeromq/czmq/commits) | [![GitHub License](https://img.shields.io/github/license/zeromq/czmq)]()

**Link** - [ZeroMQ](https://zeromq.org/)  
**Features** - A high-performance asynchronous messaging library intended for distributed or concurrent applications.  

#### Key Points

- Supports common messaging patterns (publish/subscribe, request/reply, client/server, and so on) over a range of transports (TCP, in-process, inter-process, multicast, WebSocket, and so on), making inter-process messaging as simple as inter-thread messaging;

---

### CDIPC

[![GitHub Repo stars](https://img.shields.io/github/stars/dukelec/cdipc)](https://github.com/dukelec/cdipc/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/dukelec/cdipc)](https://github.com/dukelec/cdipc/commits) | [![GitHub License](https://img.shields.io/github/license/dukelec/cdipc)]()

**Link** - [dukelec/cdipc: A Real-time Inter-Process Communication (IPC) mechanism and library](https://github.com/dukelec/cdipc)  
**Features** - An inter-process communication (IPC) mechanism and library suitable for coordinating perception, control drivers, and algorithms in real-time systems.  

#### Key Points

---

## Pipes

### readerwriterqueue

[![GitHub Repo stars](https://img.shields.io/github/stars/cameron314/readerwriterqueue)](https://github.com/cameron314/readerwriterqueue/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/cameron314/readerwriterqueue)](https://github.com/cameron314/readerwriterqueue/commits) | [![GitHub License](https://img.shields.io/github/license/cameron314/readerwriterqueue)]()

**Link** - [cameron314/readerwriterqueue: A fast single-producer, single-consumer lock-free queue for C++](https://github.com/cameron314/readerwriterqueue)  
**Features** - A C++ single-producer, single-consumer lock-free queue. It serves the same purpose as a pipe framework, is fast and easy to use, and emphasizes thread safety without locks.  

#### Key Points

---

## Mailboxes

### DataCenter

[![GitHub Repo stars](https://img.shields.io/github/stars/FASTSHIFT/X-TRACK)](https://github.com/FASTSHIFT/X-TRACK/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/FASTSHIFT/X-TRACK?path=Software/X-Track/USER/App/Utils/DataCenter)](https://github.com/FASTSHIFT/X-TRACK/commits) | [![GitHub License](https://img.shields.io/github/license/FASTSHIFT/X-TRACK)]()

**Link** - [X-TRACK/Software/X-Track/USER/App/Utils/DataCenter at main · FASTSHIFT/X-TRACK](https://github.com/FASTSHIFT/X-TRACK/tree/main/Software/X-Track/USER/App/Utils/DataCenter)  
**Features** - A C++ message publish-subscribe framework that provides complete mailbox services and is suitable for project-level engineering.  

#### Key Points

---

## Thread Management

### C Thread Pool

[![GitHub Repo stars](https://img.shields.io/github/stars/Pithikos/C-Thread-Pool)](https://github.com/Pithikos/C-Thread-Pool/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/Pithikos/C-Thread-Pool)](https://github.com/Pithikos/C-Thread-Pool/commits) | [![GitHub License](https://img.shields.io/github/license/Pithikos/C-Thread-Pool)]()

**Link** - [Pithikos/C-Thread-Pool: A minimal but powerful thread pool in ANSI C](https://github.com/Pithikos/C-Thread-Pool)  
**Features** - A lightweight embedded thread-pool library for managing thread creation and lifecycles, solving the overhead caused by frequent thread creation and destruction.  

#### Key Points

- Introduction: [A Minimal Implementation of an Embedded Thread Pool!](https://mp.weixin.qq.com/s/0epRcDSvAU0GzQ6hlzg02w)

---

## Driver Frameworks

### initcall

**Link** - [Extracted RT-Thread initcall Framework - Code Snippet - Gitee.com](https://gitee.com/Luyi365/codes/x4co95d03hvrjtpaz2lkm52)  
**Features** - Extracts the RT-Thread initialization framework so initialization is completed in the kernel.  

#### Key Points

---

### platform_dev

**Link** - [Simplified Driver Framework - Code Snippet - Gitee.com](https://gitee.com/Luyi365/codes/r6n19xu2ikatw7cojy8he84)  
**Features** - A simplified driver framework modeled on Linux. Its design does not use dynamic memory allocation, making it suitable for chips with limited resources.  

#### Key Points

- ~~The code uses memory sections in place of linked-list functionality: replaces linked lists;~~ (pending release)
- `__start_platform_init` and `__stop_platform_init` are respectively defined in the linker file on the two sides of `.platform_init`; `__start_device_init` follows the same pattern;
- If a chip does not support the initcall mechanism, replacing its section portion with a linked-list form can achieve the same result;
- Best used with: [Detailed Explanation of __attribute__ section - CSDN Blog](https://blog.csdn.net/seven_feifei/article/details/95947358)；
- Why `general_ops` in `PLATFORM_ITEM_REGISTER` can replace all operations: [About the union Type](./appendix.en.md#about-the-union-type)；

---

### c-periphery

[![GitHub Repo stars](https://img.shields.io/github/stars/vsergeev/c-periphery)](https://github.com/vsergeev/c-periphery/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/vsergeev/c-periphery)](https://github.com/vsergeev/c-periphery/commits) | [![GitHub License](https://img.shields.io/github/license/vsergeev/c-periphery)]()

**Link** - [vsergeev/c-periphery: A C library for peripheral I/O (GPIO, LED, PWM, SPI, I2C, MMIO, Serial) in Linux.](https://github.com/vsergeev/c-periphery)  
**Features** - A Linux-based hardware peripheral abstraction-layer template.  

#### Key Points

- Introduction: [A Practical Hardware Peripheral Access Library!](https://mp.weixin.qq.com/s/tt4VzyIU-Nin8p8Ox-kGJA)

---

## Sensor Frameworks

### senser_algorithm

**Link** - [Sensor + Algorithm Processing Framework: A sensor-data processing framework for RTOS.](https://gitee.com/Luyi365/senser_algorithm)  
**Features** - A sensor-data processing framework for RTOS.  

#### Key Points

---

## Module Frameworks

### RIL

[![Gitee Repo stars](https://gitee.com/moluo-tech/ril/badge/star.svg?theme=gvp)](https://gitee.com/moluo-tech/ril/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/moluo-tech/ril&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/moluo-tech/ril&query=$.license&label=license)]()

**Link** - [ril: RIL is a wireless communication module (GSM/GPRS/CatM1/NB) management framework developed specifically for embedded platforms. It is suitable for resource-constrained IoT terminal devices (microcontroller + wireless cellular module solutions) and provides essential IoT communication functions, including network registration, connection management, SMS messaging, and Socket communication.](https://gitee.com/moluo-tech/ril)  
**Features** - Wireless communication module (GSM/GPRS/CatM1/NB-Iot) management software developed specifically for embedded platforms.  

#### Key Points

---

## State Machines

### EFSMC

[![Gitee Repo stars](https://gitee.com/simpost/EFSMC/badge/star.svg?theme=gvp)](https://gitee.com/simpost/EFSMC/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/simpost/EFSMC&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/simpost/EFSMC&query=$.license&label=license)]()

**Link** - [EFSMC: EFSM (event finite state machine) is an event-driven finite state machine. EFSM can implement hundreds of states and thousands of event handlers, as well as multiple state machines and hierarchical state machines. It can be applied to platforms such as cloud-backend microservices and embedded software.](https://gitee.com/simpost/EFSMC)  
**Features** - An event-driven finite state machine that avoids naming conflicts through careful design. It is simple, convenient, and standardized to use.  

#### Key Points

---

### signals\_slots

[![GitHub Repo stars](https://img.shields.io/github/stars/Aladdin-Wang/signals_slots)](https://github.com/Aladdin-Wang/signals_slots/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/Aladdin-Wang/signals_slots)](https://github.com/Aladdin-Wang/signals_slots/commits) | [![GitHub License](https://img.shields.io/github/license/Aladdin-Wang/signals_slots)]()

**Link** - [Aladdin-Wang/signals_slots: Signal-and-slot module implemented in C](https://github.com/Aladdin-Wang/signals_slots)  
**Features** - A lightweight signal-and-slot framework that simplifies event-driven programming.  

#### Key Points

- Implementation process: [Simulating Qt Signal-and-Slot Functionality in C](https://mp.weixin.qq.com/s/3BcMHY71lH3WPgcPwxb2LQ)

---

### UML State Machine in C

[![GitHub Repo stars](https://img.shields.io/github/stars/kiishor/UML-State-Machine-in-C)](https://github.com/kiishor/UML-State-Machine-in-C/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/kiishor/UML-State-Machine-in-C)](https://github.com/kiishor/UML-State-Machine-in-C/commits) | [![GitHub License](https://img.shields.io/github/license/kiishor/UML-State-Machine-in-C)]()

**Link** - [kiishor/UML-State-Machine-in-C: A minimalist UML State machine framework for finite state machine and hierarchical state machine in C](https://github.com/kiishor/UML-State-Machine-in-C)  
**Features** - A multi-platform, lightweight state-machine framework supporting finite state machines and hierarchical state machines, with logging functionality.  

#### Key Points

---

## Dynamic Loading

### dynamic_loader

[![Gitee Repo stars](https://gitee.com/wzh1845462801/dynamic_loader/badge/star.svg?theme=gvp)](https://gitee.com/wzh1845462801/dynamic_loader/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/wzh1845462801/dynamic_loader&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/wzh1845462801/dynamic_loader&query=$.license&label=license)]()

**Link** - [dynamic_loader: This project is a function library that implements dynamic loading on microcontrollers (such as STM32). Similar to DLLs on Windows and SOs on Linux, it can dynamically load code from other storage media into RAM.](https://gitee.com/wzh1845462801/dynamic_loader)  
**Features** - A dynamic-loading function library trimmed from the libdl source code of [RT-Thread](../sys-thread-lib/README.md#rt-thread). It is not coupled to the original OS and can be used on bare metal.  

#### Key Points

- Reference: [Principles of Dynamic Loading on STM32 V1.0 - STM32H7 - Anfulai Embedded Forum - Powered by Discuz!](https://forum.anfulai.cn/forum.php?mod=viewthread&tid=112099&extra=page=1)
- Introduction: [Implement Dynamic Loading on a Microcontroller?!](https://mp.weixin.qq.com/s/7FzGQ9FjDma9_fiDPYam2g)

---
