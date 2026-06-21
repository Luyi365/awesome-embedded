# 内核与基层框架库

> 原来这个库分为二个部分，但后来发觉其实内核和框架结合一下就是系统或者工具集了，所以将它们归为一类，但某些与内核相关性不是很强的框架就没放在这里，例如[菜单框架](../ui-menu-lib/README.md#菜单框架)。  
> 同时会把涉及到比较底层的代码库也放进来。  
>
> <ins>事件</ins>、<ins>消息</ins>和<ins>数据</ins>这三个概念容易弄混淆，它们的关注点如下：
>
> - **事件**：关注于特定动作的发生和回调响应机制；
> - **消息**：侧重于组件间的通信和数据传递；
> - **数据**：涉及数据在程序中的传递方式，不限于消息或事件的上下文。

## 事件

### cpost

![GitHub Repo stars](https://img.shields.io/github/stars/NevermindZZT/cpost) | ![GitHub last commit](https://img.shields.io/github/last-commit/NevermindZZT/cpost) | ![GitHub License](https://img.shields.io/github/license/NevermindZZT/cpost)

**链接**：[NevermindZZT/cpost](https://github.com/NevermindZZT/cpost)  
**特征**：超轻量的上下文切换和任务解耦库，采用事件分发机制，适合于裸机系统。  

#### 要点

- 参考：[c 语言上下文的快速切换 | Letter](https://nevermindzzt.github.io/2020/12/27/c%E8%AF%AD%E8%A8%80%E4%B8%8A%E4%B8%8B%E6%96%87%E7%9A%84%E5%BF%AB%E9%80%9F%E5%88%87%E6%8D%A2/)和 [C 语言模块化编程的完美解耦 | Letter](https://nevermindzzt.github.io/2020/12/20/C%E8%AF%AD%E8%A8%80%E6%A8%A1%E5%9D%97%E5%8C%96%E7%BC%96%E7%A8%8B%E7%9A%84%E5%AE%8C%E7%BE%8E%E8%A7%A3%E8%80%A6/)；
- 这里的上下文切换作用相当于中断里置标志，轮询中执行相应任务；
- 库中参数 `delay` 不是指的时间，而是系统"tick"；
- 这里解耦库是使用事件广播的原理，但不太适用于事件广播的用途，而是用来解耦的；
- 解耦库依赖于编译器，这个要注意些；
- 要添加适当的头文件；

---

### LwEVT

![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwevt) | ![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwevt) | ![GitHub License](https://img.shields.io/github/license/MaJerle/lwevt)

**链接**：[LwEVT latest-develop documentation — LwEVT documentation](https://docs.majerle.eu/projects/lwevt/en/latest/)  
**特征**：专业的事件模块库，可选数据结构的自定义类型，且挂载指定函数，可理解为事件和消息的结合。  

#### 要点

- 使用介绍：[推荐一个嵌入式轻量级事件管理库！](https://mp.weixin.qq.com/s/KkV0pxVfb56Ig8HDMuwFaQ)
- 事件的枚举都使用 `LWEVT_TYPE_BASIC` 和 `LWEVT_TYPE_EXT` 来载入，并单独放在一个头文件中。

---

## 消息

### YAMI4

**链接**：[Inspirel - YAMI4](http://www.inspirel.com/yami4/index.html)  
**特征**：专为分布式系统设计的消息传递库，特别关注控制和监控系统。  

#### 要点

- 和网络协议有点像，也是对应客户端与服务器，然后进行数据的收发，具体差别可参考官网介绍；
- API 分为两部分：核心和通用。核心部分管理最基本的通信功能，包括连接池、消息队列和帧组装引擎。该层虽然非常简化，但完全足以用于自定义应用程序。另一方面，通用层建立在核心服务之上，并添加了线程管理和更高级别的接口，使其更易于使用；
- 使用 C++ 语言，符合 POSIX 接口；

---

### ZeroMQ

![GitHub Repo stars](https://img.shields.io/github/stars/zeromq/czmq) | ![GitHub last commit](https://img.shields.io/github/last-commit/zeromq/czmq) | ![GitHub License](https://img.shields.io/github/license/zeromq/czmq)

**链接**：[ZeroMQ](https://zeromq.org/)  
**特征**：一个高性能异步消息传递库，旨在用于分布式或并发应用程序。  

#### 要点

- 支持通过各种传输（TCP、进程内、进程间、组播、WebSocket 等）的常见消息传递模式（发布/订阅、请求/回复、客户端/服务器等），使进程间消息传递像线程间消息传递一样简单；

---

### CDIPC

![GitHub Repo stars](https://img.shields.io/github/stars/dukelec/cdipc) | ![GitHub last commit](https://img.shields.io/github/last-commit/dukelec/cdipc) | ![GitHub License](https://img.shields.io/github/license/dukelec/cdipc)

**链接**：[dukelec/cdipc: A Real-time Inter-Process Communication (IPC) mechanism and library](https://github.com/dukelec/cdipc)  
**特征**：一种进程间通信 （IPC） 机制和库，适合在实时系统中协调感知、控制驱动程序和算法。  

#### 要点

---

## 管道

### readerwriterqueue

![GitHub Repo stars](https://img.shields.io/github/stars/cameron314/readerwriterqueue) | ![GitHub last commit](https://img.shields.io/github/last-commit/cameron314/readerwriterqueue) | ![GitHub License](https://img.shields.io/github/license/cameron314/readerwriterqueue)

**链接**：[cameron314/readerwriterqueue: A fast single-producer, single-consumer lock-free queue for C++](https://github.com/cameron314/readerwriterqueue)  
**特征**：基于C++的单生产者、单使用者无锁队列，意义同通管道框架，速度快且易用，无需锁也能注重线程安全。  

#### 要点

---

## 邮箱

### DataCenter

![GitHub Repo stars](https://img.shields.io/github/stars/FASTSHIFT/X-TRACK) | ![GitHub last commit](https://img.shields.io/github/last-commit/FASTSHIFT/X-TRACK?path=Software%2FX-Track%2FUSER%2FApp%2FUtils%2FDataCenter) | ![GitHub License](https://img.shields.io/github/license/FASTSHIFT/X-TRACK)

**链接**：[X-TRACK/Software/X-Track/USER/App/Utils/DataCenter at main · FASTSHIFT/X-TRACK](https://github.com/FASTSHIFT/X-TRACK/tree/main/Software/X-Track/USER/App/Utils/DataCenter)  
**特征**：基于 C++ 的消息发布订阅框架，提供完整的邮箱服务，适合项目级工程。  

#### 要点

---

## 线程管理

### C Thread Pool

![GitHub Repo stars](https://img.shields.io/github/stars/Pithikos/C-Thread-Pool) | ![GitHub last commit](https://img.shields.io/github/last-commit/Pithikos/C-Thread-Pool) | ![GitHub License](https://img.shields.io/github/license/Pithikos/C-Thread-Pool)

**链接**：[Pithikos/C-Thread-Pool: A minimal but powerful thread pool in ANSI C](https://github.com/Pithikos/C-Thread-Pool)  
**特征**：轻量级的嵌入式线程池库，用于管理线程的创建和生命周期，解决频繁地创建和销毁线程所带来较大开销的问题。  

#### 要点

- 使用介绍：[一个嵌入式线程池的极简实现！](https://mp.weixin.qq.com/s/0epRcDSvAU0GzQ6hlzg02w)

---

## 驱动框架

### initcall

**链接**：[提取 RT-Thread 的 initcall 框架 - 代码片段 - Gitee.com](https://gitee.com/Luyi365/codes/x4co95d03hvrjtpaz2lkm52)  
**特征**：提取 RT-Thread 的初始化框架，使初始化工作在内核中完成。  

#### 要点

---

### platform_dev

**链接**：[简化版驱动框架 - 代码片段 - Gitee.com](https://gitee.com/Luyi365/codes/r6n19xu2ikatw7cojy8he84)  
**特征**：模仿 Linux 的简化版驱动框架，设计中不使用动态内存分配，适合低资源的芯片使用。  

#### 要点

- ~~代码用内存段代替了链表功能：((20240116165930-cu53x1o '用 attribute((section))代替链表'))；~~（待发布）
- 其中 `__start_platform_init`、`__stop_platform_init` 分别在链接文件里定义在 `.platform_init` 左右两侧，`__start_device_init` 同理；
- 如果芯片不支持 initcall 机制，将其 section 的部分换成链表的形式也可以达到同样的效果；
- 配合这个食用更佳：[__attribute__之 section 详解___attribute__ section-CSDN 博客](https://blog.csdn.net/seven_feifei/article/details/95947358)；
- 为什么 `PLATFORM_ITEM_REGISTER` 中 `general_ops` 可以代替所有操作：[关于 union 联合体](./Appendix.md#关于-union-联合体)；

---

### c-periphery

![GitHub Repo stars](https://img.shields.io/github/stars/vsergeev/c-periphery) | ![GitHub last commit](https://img.shields.io/github/last-commit/vsergeev/c-periphery) | ![GitHub License](https://img.shields.io/github/license/vsergeev/c-periphery)

**链接**：[vsergeev/c-periphery: A C library for peripheral I/O (GPIO, LED, PWM, SPI, I2C, MMIO, Serial) in Linux.](https://github.com/vsergeev/c-periphery)  
**特征**：基于 Linux 的硬件外设抽象层模板。  

#### 要点

- 使用介绍：[一个实用的硬件外设访问库！](https://mp.weixin.qq.com/s/tt4VzyIU-Nin8p8Ox-kGJA)

---

## 传感器框架

### senser_algorithm

**链接**：[传感器 + 算法处理框架: 适用于 RTOS 的传感器数据处理框架。](https://gitee.com/Luyi365/senser_algorithm)  
**特征**：适用于 RTOS 的传感器数据处理框架。  

#### 要点

---

## 模组框架

### RIL

![Gitee Repo stars](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/moluo-tech/ril&query=$.stargazers_count&style=social&logo=gitee&label=Stars) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/moluo-tech/ril&query=$.pushed_at&label=last%20commit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/moluo-tech/ril&query=$.license&label=license)

**链接**：[ril: RIL 是一款专门为嵌入式平台开发的无线通信模块(GSM/GPRS/CatM1/NB)管理框架，适用于资源受限物联网终端设备（单片机 + 无线蜂窝模组的方案），并提供物联网通信所需的基本功能，包含网络注册、连接管理、短信收发及 Socket 通信。](https://gitee.com/moluo-tech/ril)  
**特征**：专门为嵌入式平台开发的无线通信模组(GSM/GPRS/CatM1/NB-Iot)管理软件。  

#### 要点

---

## 状态机

### EFSMC

![Gitee Repo stars](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/simpost/EFSMC&query=$.stargazers_count&style=social&logo=gitee&label=Stars) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/simpost/EFSMC&query=$.pushed_at&label=last%20commit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/simpost/EFSMC&query=$.license&label=license)

**链接**：[EFSMC: EFSM(event finite state machine，事件驱动型有限状态机)，是一个基于事件驱动的有限状态机。使用EFSM可实现上百个状态、上千种事件处理，且可实现多重状态机和层次状态机。可应用在云后台微服务和嵌入式软件等各种平台中。](https://gitee.com/simpost/EFSMC)  
**特征**：基于事件驱动的有限状态机，通过巧妙设计，避免了命名冲突的问题。使用起来简单、方便、规范。  

#### 要点

---

### signals\_slots

![GitHub Repo stars](https://img.shields.io/github/stars/Aladdin-Wang/signals_slots) | ![GitHub last commit](https://img.shields.io/github/last-commit/Aladdin-Wang/signals_slots) | ![GitHub License](https://img.shields.io/github/license/Aladdin-Wang/signals_slots)

**链接**：[Aladdin-Wang/signals_slots: C语言实现的信号槽模块](https://github.com/Aladdin-Wang/signals_slots)  
**特征**：轻量级信号与槽框架，简化事件驱动编程。  

#### 要点

- 实现过程：[C语言模拟QT的信号与槽功能](https://mp.weixin.qq.com/s/3BcMHY71lH3WPgcPwxb2LQ)

---

### UML State Machine in C

![GitHub Repo stars](https://img.shields.io/github/stars/kiishor/UML-State-Machine-in-C) | ![GitHub last commit](https://img.shields.io/github/last-commit/kiishor/UML-State-Machine-in-C) | ![GitHub License](https://img.shields.io/github/license/kiishor/UML-State-Machine-in-C)

**链接**：[kiishor/UML-State-Machine-in-C: A minimalist UML State machine framework for finite state machine and hierarchical state machine in C](https://github.com/kiishor/UML-State-Machine-in-C)  
**特征**：多平台、轻量级状态机框架，支持有限状态机和分层状态机，带有日志记录功能。  

#### 要点

---

## 动态加载

### dynamic_loader

![Gitee Repo stars](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/wzh1845462801/dynamic_loader&query=$.stargazers_count&style=social&logo=gitee&label=Stars) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/wzh1845462801/dynamic_loader&query=$.pushed_at&label=last%20commit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/wzh1845462801/dynamic_loader&query=$.license&label=license)

**链接**：[dynamic_loader: 本项目是一个在单片机（如：STM32）上实现动态加载功能的函数库，与 Windows 中的 dll，Linux 中的 so 类似，可以将代码动态地从其他的存储介质，动态加载到 RAM 中](https://gitee.com/wzh1845462801/dynamic_loader)  
**特征**：动态加载函数库，裁剪自 [RT-Thread](../sys-thread-lib/README.md#rt-thread) 的 libdl 源码，不与原本 OS 耦合，可在裸机使用。  

#### 要点

- 参考：[基于 STM32 动态加载实现原理 V1.0 - STM32H7 - 硬汉嵌入式论坛 - Powered by Discuz!](https://forum.anfulai.cn/forum.php?mod=viewthread&tid=112099&extra=page=1)
- 使用介绍：[在单片机上实现动态加载功能？！](https://mp.weixin.qq.com/s/7FzGQ9FjDma9_fiDPYam2g)

---

## RPC

> 远程调用RPC（Remote Procedure Call）是一种让不同的计算机程序之间像本地调用函数一样通信的方式。例如服务器创建了一个服务，其他客户端通过端口访问服务。参考：[Writing an RPC From Scratch · Caffeinspiration](https://alexanderell.is/posts/rpc-from-scratch/)

### ERPC

![Gitee Repo stars](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/simpost/ERPC-doc&query=$.stargazers_count&style=social&logo=gitee&label=Stars) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/simpost/ERPC-doc&query=$.pushed_at&label=last%20commit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/simpost/ERPC-doc&query=$.license&label=license)

**链接**：[ERPC-doc: ERPC（Embedded Remote Procedure Call）是一个简单的、易用的、高效的嵌入式远程调用框架。它不仅实现了远程调用，还实现了状态通知（观察者模式），同时还支持数据加密（用户可自定义加密算法）、异常监控和完备的日志管理方法。使用ERPC可简化系统的设计难度，降低模块之间的耦合度，降低开发人员之间的依赖性。](https://gitee.com/simpost/ERPC-doc)  
**特征**：一个简单的、易用的、高效的远程调用框架。  

---

### EmbedXrpc

![Gitee Repo stars](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/snikeguo/EmbedXrpc&query=$.stargazers_count&style=social&logo=gitee&label=Stars) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/snikeguo/EmbedXrpc&query=$.pushed_at&label=last%20commit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/snikeguo/EmbedXrpc&query=$.license&label=license)

**链接**：[EmbedXrpc: 这个东西类似于 Google 的 GRPC,但是应用场景是单片机。RPC 远程调用极大的方便了开发，使得不必关注于协议解析，数据的序列化和反序列化等繁琐的工作。可是目前还没有在单片机上实现好用的 RPC 框架，于是我就谋生了做这个 RPC 框架的想法，所用的技术是：C#做 IDL 语言 +csscript+ 自己实现序列化和反序列化 + 代码生成 QQ 群 134161401](https://gitee.com/snikeguo/EmbedXrpc)  
**特征**：通过RPC通讯协议，可忽略协议本身进行业务逻辑的实现，附带代码生成工具。  

#### 要点

---

### erpc

![GitHub Repo stars](https://img.shields.io/github/stars/EmbeddedRPC/erpc) | ![GitHub last commit](https://img.shields.io/github/last-commit/EmbeddedRPC/erpc) | ![GitHub License](https://img.shields.io/github/license/EmbeddedRPC/erpc)

**链接**：[EmbeddedRPC/erpc: Embedded RPC](https://github.com/EmbeddedRPC/erpc)  
**特征**：是NXP开源的、用于多芯片嵌入式系统和异构多核SoC的开源远程过程调用（RPC）系统。  

#### 要点

---

## CGI

> CGI（Common Gateway Interface）是一种 Web 服务器与外部程序进行交互的标准协议。参考：[CGI](./Appendix.md#cgi)

### FastCGI

![GitHub Repo stars](https://img.shields.io/github/stars/FastCGI-Archives/fcgi2) | ![GitHub last commit](https://img.shields.io/github/last-commit/FastCGI-Archives/fcgi2) | ![GitHub License](https://img.shields.io/github/license/FastCGI-Archives/fcgi2)

**链接**：[FastCGI.com Archives](https://fastcgi-archives.github.io/)  
**特征**：改进了传统CGI的性能，增加了分布式计算和多角色特性。  

#### 要点

---

## Web/HTTP服务器

### LightTPD

![GitHub Repo stars](https://img.shields.io/github/stars/lighttpd/lighttpd1.4) | ![GitHub last commit](https://img.shields.io/github/last-commit/lighttpd/lighttpd1.4) | ![GitHub License](https://img.shields.io/github/license/lighttpd/lighttpd1.4)

**链接**：[Home - Lighttpd - fly light](https://www.lighttpd.net/)  
**特征**：是一个轻量级、高性能的 开源 Web 服务器，专为高并发、低内存占用 的场景设计。相比Apache 或 Nginx更适合嵌入式设备。  

#### 要点

- 带有（CGI、FastCGI、Lua、PHP）等集成功能；

---

### Mongoose

![GitHub Repo stars](https://img.shields.io/github/stars/cesanta/mongoose) | ![GitHub last commit](https://img.shields.io/github/last-commit/cesanta/mongoose) | ![GitHub License](https://img.shields.io/github/license/cesanta/mongoose)

**链接**：[Mongoose - an embedded Web Server, MQTT and Websocket library with built-in TCP/IP and TLS1.3 stack](https://mongoose.ws/)  
**特征**：C / C++的事件驱动网络库，除了基本协议栈还了内置HTTP、MQTT等服务协议，可在裸机及RTOS上运行，带有UI构建器。商用有付费限制。  

#### 要点

---

### Boa

**链接**：[Boa Webserver](http://www.boa.org/)  
**特征**：开源的小型Web服务器，适用于嵌入式应用。于2005起不再更新维护，目前存在已知安全漏洞，不推荐使用。  

#### 要点

---

### libevent

![GitHub Repo stars](https://img.shields.io/github/stars/libevent/libevent) | ![GitHub last commit](https://img.shields.io/github/last-commit/libevent/libevent) | ![GitHub License](https://img.shields.io/github/license/libevent/libevent)

**链接**：[lib事件](https://libevent.org/)  
**特征**：专用于网络服务器的事件驱动库，旨在替换事件驱动网络服务器中的事件循环。  

#### 要点

- 使用介绍：[嵌入式开发必备：开源事件驱动库 libevent](https://mp.weixin.qq.com/s/3K4E6lOEu00EE4-CyhdIPg)

---

### dyad

![GitHub Repo stars](https://img.shields.io/github/stars/rxi/dyad) | ![GitHub last commit](https://img.shields.io/github/last-commit/rxi/dyad) | ![GitHub License](https://img.shields.io/github/license/rxi/dyad)

**链接**：[rxi/dyad: Asynchronous networking for C](https://github.com/rxi/dyad)  
**特征**：基于Linux的异步网络库，仅支持TCP 网络通讯，用于创建小型独立设备服务器，并为现有项目提供网络支持。  

#### 要点

- 可以看出来它是基于Linux系统的内核和POSIX接口实现的，如果要用在裸机或其他OS上则需要添加对应的支持才行；

---

### libevhtp

![GitHub Repo stars](https://img.shields.io/github/stars/Yellow-Camper/libevhtp) | ![GitHub last commit](https://img.shields.io/github/last-commit/Yellow-Camper/libevhtp) | ![GitHub License](https://img.shields.io/github/license/Yellow-Camper/libevhtp)

**链接**：[Yellow-Camper/libevhtp: Create extremely-fast and secure embedded HTTP servers with ease.](https://github.com/Yellow-Camper/libevhtp)   
**特征**：适合嵌入式设备的低负载HTTP库。  

#### 要点

- 使用介绍：[分享一款专为嵌入式系统设计的HTTP库](https://mp.weixin.qq.com/s/-d6r6Dbt888s6WozSDFTbQ)

---