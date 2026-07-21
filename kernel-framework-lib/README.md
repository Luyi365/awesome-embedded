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

[![GitHub Repo stars](https://img.shields.io/github/stars/NevermindZZT/cpost)](https://github.com/NevermindZZT/cpost/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/NevermindZZT/cpost)](https://github.com/NevermindZZT/cpost/commits) | [![GitHub License](https://img.shields.io/github/license/NevermindZZT/cpost)]()

**链接**：[NevermindZZT/cpost](https://github.com/NevermindZZT/cpost)  
**特征**：超轻量的上下文切换和任务解耦库，采用事件分发机制，适合于裸机系统。  

#### 要点

- 参考：[c 语言上下文的快速切换 | Letter](https://nevermindzzt.github.io/2020/12/27/c语言上下文的快速切换/)和 [C 语言模块化编程的完美解耦 | Letter](https://nevermindzzt.github.io/2020/12/20/C语言模块化编程的完美解耦/)；
- 这里的上下文切换作用相当于中断里置标志，轮询中执行相应任务；
- 库中参数 `delay` 不是指的时间，而是系统"tick"；
- 这里解耦库是使用事件广播的原理，但不太适用于事件广播的用途，而是用来解耦的；
- 解耦库依赖于编译器，这个要注意些；
- 要添加适当的头文件；

---

### LwEVT

[![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwevt)](https://github.com/MaJerle/lwevt/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwevt)](https://github.com/MaJerle/lwevt/commits) | [![GitHub License](https://img.shields.io/github/license/MaJerle/lwevt)]()

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

[![GitHub Repo stars](https://img.shields.io/github/stars/zeromq/czmq)](https://github.com/zeromq/czmq/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/zeromq/czmq)](https://github.com/zeromq/czmq/commits) | [![GitHub License](https://img.shields.io/github/license/zeromq/czmq)]()

**链接**：[ZeroMQ](https://zeromq.org/)  
**特征**：一个高性能异步消息传递库，旨在用于分布式或并发应用程序。  

#### 要点

- 支持通过各种传输（TCP、进程内、进程间、组播、WebSocket 等）的常见消息传递模式（发布/订阅、请求/回复、客户端/服务器等），使进程间消息传递像线程间消息传递一样简单；

---

### CDIPC

[![GitHub Repo stars](https://img.shields.io/github/stars/dukelec/cdipc)](https://github.com/dukelec/cdipc/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/dukelec/cdipc)](https://github.com/dukelec/cdipc/commits) | [![GitHub License](https://img.shields.io/github/license/dukelec/cdipc)]()

**链接**：[dukelec/cdipc: A Real-time Inter-Process Communication (IPC) mechanism and library](https://github.com/dukelec/cdipc)  
**特征**：一种进程间通信 （IPC） 机制和库，适合在实时系统中协调感知、控制驱动程序和算法。  

#### 要点

---

## 管道

### readerwriterqueue

[![GitHub Repo stars](https://img.shields.io/github/stars/cameron314/readerwriterqueue)](https://github.com/cameron314/readerwriterqueue/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/cameron314/readerwriterqueue)](https://github.com/cameron314/readerwriterqueue/commits) | [![GitHub License](https://img.shields.io/github/license/cameron314/readerwriterqueue)]()

**链接**：[cameron314/readerwriterqueue: A fast single-producer, single-consumer lock-free queue for C++](https://github.com/cameron314/readerwriterqueue)  
**特征**：基于C++的单生产者、单使用者无锁队列，意义同通管道框架，速度快且易用，无需锁也能注重线程安全。  

#### 要点

---

## 邮箱

### DataCenter

[![GitHub Repo stars](https://img.shields.io/github/stars/FASTSHIFT/X-TRACK)](https://github.com/FASTSHIFT/X-TRACK/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/FASTSHIFT/X-TRACK?path=Software/X-Track/USER/App/Utils/DataCenter)](https://github.com/FASTSHIFT/X-TRACK/commits) | [![GitHub License](https://img.shields.io/github/license/FASTSHIFT/X-TRACK)]()

**链接**：[X-TRACK/Software/X-Track/USER/App/Utils/DataCenter at main · FASTSHIFT/X-TRACK](https://github.com/FASTSHIFT/X-TRACK/tree/main/Software/X-Track/USER/App/Utils/DataCenter)  
**特征**：基于 C++ 的消息发布订阅框架，提供完整的邮箱服务，适合项目级工程。  

#### 要点

---

## 线程管理

### C Thread Pool

[![GitHub Repo stars](https://img.shields.io/github/stars/Pithikos/C-Thread-Pool)](https://github.com/Pithikos/C-Thread-Pool/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/Pithikos/C-Thread-Pool)](https://github.com/Pithikos/C-Thread-Pool/commits) | [![GitHub License](https://img.shields.io/github/license/Pithikos/C-Thread-Pool)]()

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

- ~~代码用内存段代替了链表功能：代替链表；~~（待发布）
- 其中 `__start_platform_init`、`__stop_platform_init` 分别在链接文件里定义在 `.platform_init` 左右两侧，`__start_device_init` 同理；
- 如果芯片不支持 initcall 机制，将其 section 的部分换成链表的形式也可以达到同样的效果；
- 配合这个食用更佳：[__attribute__之section详解-CSDN 博客](https://blog.csdn.net/seven_feifei/article/details/95947358)；
- 为什么 `PLATFORM_ITEM_REGISTER` 中 `general_ops` 可以代替所有操作：[关于 union 联合体](./Appendix.md#关于-union-联合体)；

---

### c-periphery

[![GitHub Repo stars](https://img.shields.io/github/stars/vsergeev/c-periphery)](https://github.com/vsergeev/c-periphery/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/vsergeev/c-periphery)](https://github.com/vsergeev/c-periphery/commits) | [![GitHub License](https://img.shields.io/github/license/vsergeev/c-periphery)]()

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

[![Gitee Repo stars](https://gitee.com/moluo-tech/ril/badge/star.svg?theme=gvp)](https://gitee.com/moluo-tech/ril/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/moluo-tech/ril&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/moluo-tech/ril&query=$.license&label=license)]()

**链接**：[ril: RIL 是一款专门为嵌入式平台开发的无线通信模块(GSM/GPRS/CatM1/NB)管理框架，适用于资源受限物联网终端设备（单片机 + 无线蜂窝模组的方案），并提供物联网通信所需的基本功能，包含网络注册、连接管理、短信收发及 Socket 通信。](https://gitee.com/moluo-tech/ril)  
**特征**：专门为嵌入式平台开发的无线通信模组(GSM/GPRS/CatM1/NB-Iot)管理软件。  

#### 要点

---

## 状态机

### EFSMC

[![Gitee Repo stars](https://gitee.com/simpost/EFSMC/badge/star.svg?theme=gvp)](https://gitee.com/simpost/EFSMC/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/simpost/EFSMC&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/simpost/EFSMC&query=$.license&label=license)]()

**链接**：[EFSMC: EFSM(event finite state machine，事件驱动型有限状态机)，是一个基于事件驱动的有限状态机。使用EFSM可实现上百个状态、上千种事件处理，且可实现多重状态机和层次状态机。可应用在云后台微服务和嵌入式软件等各种平台中。](https://gitee.com/simpost/EFSMC)  
**特征**：基于事件驱动的有限状态机，通过巧妙设计，避免了命名冲突的问题。使用起来简单、方便、规范。  

#### 要点

---

### signals\_slots

[![GitHub Repo stars](https://img.shields.io/github/stars/Aladdin-Wang/signals_slots)](https://github.com/Aladdin-Wang/signals_slots/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/Aladdin-Wang/signals_slots)](https://github.com/Aladdin-Wang/signals_slots/commits) | [![GitHub License](https://img.shields.io/github/license/Aladdin-Wang/signals_slots)]()

**链接**：[Aladdin-Wang/signals_slots: C语言实现的信号槽模块](https://github.com/Aladdin-Wang/signals_slots)  
**特征**：轻量级信号与槽框架，简化事件驱动编程。  

#### 要点

- 实现过程：[C语言模拟QT的信号与槽功能](https://mp.weixin.qq.com/s/3BcMHY71lH3WPgcPwxb2LQ)

---

### UML State Machine in C

[![GitHub Repo stars](https://img.shields.io/github/stars/kiishor/UML-State-Machine-in-C)](https://github.com/kiishor/UML-State-Machine-in-C/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/kiishor/UML-State-Machine-in-C)](https://github.com/kiishor/UML-State-Machine-in-C/commits) | [![GitHub License](https://img.shields.io/github/license/kiishor/UML-State-Machine-in-C)]()

**链接**：[kiishor/UML-State-Machine-in-C: A minimalist UML State machine framework for finite state machine and hierarchical state machine in C](https://github.com/kiishor/UML-State-Machine-in-C)  
**特征**：多平台、轻量级状态机框架，支持有限状态机和分层状态机，带有日志记录功能。  

#### 要点

---

## 动态加载

### dynamic_loader

[![Gitee Repo stars](https://gitee.com/wzh1845462801/dynamic_loader/badge/star.svg?theme=gvp)](https://gitee.com/wzh1845462801/dynamic_loader/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/wzh1845462801/dynamic_loader&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/wzh1845462801/dynamic_loader&query=$.license&label=license)]()

**链接**：[dynamic_loader: 本项目是一个在单片机（如：STM32）上实现动态加载功能的函数库，与 Windows 中的 dll，Linux 中的 so 类似，可以将代码动态地从其他的存储介质，动态加载到 RAM 中](https://gitee.com/wzh1845462801/dynamic_loader)  
**特征**：动态加载函数库，裁剪自 [RT-Thread](../sys-thread-lib/README.md#rt-thread) 的 libdl 源码，不与原本 OS 耦合，可在裸机使用。  

#### 要点

- 参考：[基于 STM32 动态加载实现原理 V1.0 - STM32H7 - 硬汉嵌入式论坛 - Powered by Discuz!](https://forum.anfulai.cn/forum.php?mod=viewthread&tid=112099&extra=page=1)
- 使用介绍：[在单片机上实现动态加载功能？！](https://mp.weixin.qq.com/s/7FzGQ9FjDma9_fiDPYam2g)

---
