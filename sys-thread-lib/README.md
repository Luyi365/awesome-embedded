# 系统与线程库

> OS 一般分为两种，即裸机和 RTOS，但这里我分为五类：
>
> - [时间片调度系统](#时间片调度系统)：定时器或轮询控制任务运转；
> - [类实时系统](#类实时系统)：强调任务栈的硬实时性，但还没上升到 RTOS 级别；
> - [RTOS](#rtos)：有丰富的内核功能以及实时性；
> - [IoT-RTOS](#iot-rtos)：除了拥有 RTOS 特点外，注重物联网传输，基本都遵循 [POSIX](./appendix.md#什么是-posix) 标准，与 Linux 兼容；
> - [ROS](#ros)：机器人专用系统，一般采用分布式的通信框架，帮助程序进程之间更方便地通信，所以它并不是管控机器人所有部件的模组的，而是管理每个部件，部件自身可以用不同的 OS。

## 时间片调度系统

### ztask

[![GitHub Repo stars](https://img.shields.io/github/stars/tomzbj/ztask)](https://github.com/tomzbj/ztask/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/tomzbj/ztask)](https://github.com/tomzbj/ztask/commits) | [![GitHub License](https://img.shields.io/github/license/tomzbj/ztask)]()

**链接**：[GitHub - tomzbj/ztask: A simple timer-based scheduler](https://github.com/tomzbj/ztask)  
**特征**：极简的基于时间片调度器，仅 5 个 api，属于那种随手就可以写出来的框架。  

#### 要点

---

### ETP

[![Gitee Repo stars](https://gitee.com/ecbm/timeslice-polling/badge/star.svg?theme=gvp)](https://gitee.com/ecbm/timeslice-polling/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/ecbm/timeslice-polling&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/ecbm/timeslice-polling&query=$.license&label=license)]()

**链接**：[时间片轮询框架: 这是一个跨平台的 ETP（Ecbm-Timeslice-Polling）框架。本框架基于时间片轮询法，任务之间不具备有抢占性，优先级由安装任务的顺序决定。](https://gitee.com/ecbm/timeslice-polling)  
**特征**：时间片轮询框架，旨在解耦主轮询中各个不同时间片的任务，属于最基础的轮询框架。  

#### 要点

---

### cotTask

[![Gitee Repo stars](https://gitee.com/cot_package/cot_task/badge/star.svg?theme=gvp)](https://gitee.com/cot_package/cot_task/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/cot_package/cot_task&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/cot_package/cot_task&query=$.license&label=license)]()

**链接**：[cotTask: 嵌入式设备中使用定时器实现任务调度的模块组件代码](https://gitee.com/cot_package/cot_task)  
**特征**：时间片轮询框架，初始化、启动和任务调度管理。  

#### 要点

- 上面这个链接和 [cTask](https://gitee.com/const-zpc/cTask) 的内容是一样的，选其中一个使用就行；
- 和 [ETP](#etp) 的区别是可以设置任务的优先级；
- 使用介绍：[任务调度开源代码](https://mp.weixin.qq.com/s/7rf_9xq63wi0muo63bqkSw)

---

### CodeBrick

[![Gitee Repo stars](https://gitee.com/moluo-tech/CodeBrick/badge/star.svg?theme=gvp)](https://gitee.com/moluo-tech/CodeBrick/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/moluo-tech/CodeBrick&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/moluo-tech/CodeBrick&query=$.license&label=license)]()

**链接**：[CodeBrick: 一种无 OS 的 MCU 实用软件管理系统，包括任务轮询框架，命令管理器、低功耗管理、环形缓冲区等实用模块。](https://gitee.com/moluo-tech/CodeBrick)  
**特征**：时间片轮询框架，包括任务轮询管理，命令管理器、低功耗管理、环形缓冲区等实用模块，不带有驱动层。  

#### 要点

- 模块的初始化、任务的载入、cli 命令的载入都是以注册到一个内存段的方式进行。
- 使用介绍：[一个实用的单片机软件框架](https://mp.weixin.qq.com/s/hCmV3kJTC_TFXSzuklmUVA)

---

### vkern

[![Gitee Repo stars](https://gitee.com/Lamdonn/vkern/badge/star.svg?theme=gvp)](https://gitee.com/Lamdonn/vkern/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Lamdonn/vkern&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Lamdonn/vkern&query=$.license&label=license)]()

**链接**：[vkern: 简单的周期任务调度内核](https://gitee.com/Lamdonn/vkern)  
**特征**：仿照 RTOS 架构编写的任务调度内核，其原理还是使用定时器创建前后台系统。  

#### 要点

---

### cola_os

[![Gitee Repo stars](https://gitee.com/schuck/cola_os/badge/star.svg?theme=gvp)](https://gitee.com/schuck/cola_os/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/schuck/cola_os&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/schuck/cola_os&query=$.license&label=license)]()

**链接**：[cola_os: 300 行代码实现多任务管理的 OS，在很多 MCU 开发中，功能很简单，实时性要求不强，如果使用 RTOS 显得太浪费，任务多了管理不当又很乱，所以才会想起做一个轮询的任务管理。简单好用！CSDN:https://blog.csdn.net/ziqi5543/article/details/101512722](https://gitee.com/schuck/cola_os)  
**特征**：前后台系统，包含（initcall 初始化机制、类 rt_thread 硬件抽象层、任务池和 Timer 池）。  

#### 要点

- 核心就是在裸机的基础上增加了链表对进程进行管理，将大循环解耦成多个互不干扰的任务；
- 除了代码量外，没有其他资源的消耗，因此上了这个 os 后并不影响功耗和性能，很适合稍复杂的裸机系统；
- 使用 AC6 编译 `cola_init` 组件会报错，具体可看：[使用 ARM Compiler 6 编译器时有问题，需要修复 · Issue #I6TF6K · schuck/cola_os - Gitee.com](https://gitee.com/schuck/cola_os/issues/I6TF6K)
- 使用介绍：[嵌入式大杂烩周记 | 第 4 期](https://mp.weixin.qq.com/s/7seVk1q5SOa3Lq_yU3_XOQ)

---

### JxOS

[![Gitee Repo stars](https://gitee.com/jeremyceng/JxOS/badge/star.svg?theme=gvp)](https://gitee.com/jeremyceng/JxOS/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/jeremyceng/JxOS&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/jeremyceng/JxOS&query=$.license&label=license)]()

**链接**：[JxOS: 面向 MCU 的小型前后台系统。此项目的设计思想是：功能模块与硬件高度解耦，提高代码模块的可复用性；不使用复杂的数据结构和语法以提高不同硬件平台和编译器之间的兼容性，实现工程在不同 MCU 之间的快速移植；提供实用稳定常用的功能模块，实现项目的快速开发；定义标准应用开发框架，减轻应用开发的工作量和难度。](https://gitee.com/jeremyceng/JxOS)  
**特征**：前后台系统，没有复杂的注册与函数指针结构，提供系统内核功能：任务、事件、消息、公告板、邮箱、管道、注册、内存分配……  

#### 要点

- 里面的小功能很多，解耦的也比较清晰，可以根据需要逐个进行移植。
- 使用介绍：[一个面向 MCU 的小型前后台系统](https://mp.weixin.qq.com/s/Qlir_JqmOJtdNkuAeygoQQ)

---

### EventOS

[![Gitee Repo stars](https://gitee.com/event-os/eventos/badge/star.svg?theme=gvp)](https://gitee.com/event-os/eventos/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/event-os/eventos&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/event-os/eventos&query=$.license&label=license)]()

**链接**：[eventos: 嵌入式开发框架，事件驱动，超级轻量。最低占用 ROM 1.5KB，RAM 172 字节。核心技术是事件总线，支持 Reactor 和状态机两种模式，协作式内核，极度可靠。可深度裁剪，移植方便。](https://gitee.com/event-os/eventos)  
**特征**：事件驱动型的嵌入式系统，提供内核等功能。  

#### 要点

---

### BabyOS

[![Gitee Repo stars](https://gitee.com/notrynohigh/BabyOS/badge/star.svg?theme=gvp)](https://gitee.com/notrynohigh/BabyOS/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/notrynohigh/BabyOS&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/notrynohigh/BabyOS&query=$.license&label=license)]()

**链接**：[BabyOS: 专为 MCU 项目开发提速的代码框架](https://gitee.com/notrynohigh/BabyOS)  
**特征**：注册服务型框架，适用于裸机 MCU 项目，是一套管理功能模块和外设驱动的框架，拥有极明确的代码分层和代码规范，类 RTT 的“MenuConfig”终端配置，带有 PC 模拟。  

#### 要点

- 由于是货架结构，该 OS 旨在为裸机 MCU 提供方便的可替换、可验证和可存储的代码结构。因此很适合中小公司的项目开发。
- 由于带有终端配置功能，新的代码需要严格按照该 OS 提供的规则编写。
- 使用介绍：[分享一个管理功能模块和外设驱动的框架](https://mp.weixin.qq.com/s/3yeVTiNWkLj1yevq3lSb9Q)

---

## 类实时系统

### cotOs

[![Gitee Repo stars](https://gitee.com/cot_package/cot_os/badge/star.svg?theme=gvp)](https://gitee.com/cot_package/cot_os/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/cot_package/cot_os&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/cot_package/cot_os&query=$.license&label=license)]()

**链接**：[cotOs: 嵌入式设备中利用 setjmp/longjmp 实现一个简单的查询式协作多任务调度系统](https://gitee.com/cot_package/cot_os)  
**特征**：简单的查询式协作多任务系统，无需使用定时器进行任务切换，就和 RTOS 创建任务一样，但没有提供其他功能。  

#### 要点

- 与其他裸机 OS 及 RTOS 的对比在链接里都有写；
- 使用介绍：[查询式协作多任务系统](https://mp.weixin.qq.com/s/qouyA6IApyktT9XxSFTuYA)

---

### BasicOS

[![Gitee Repo stars](https://gitee.com/event-os/basic-os/badge/star.svg?theme=gvp)](https://gitee.com/event-os/basic-os/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/event-os/basic-os&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/event-os/basic-os&query=$.license&label=license)]()

**链接**：[basic-os: 支持共享任务栈的协作式内核，专门定位小 RAM 的 MCU，目前提供了共享栈任务调度和软定时器等基本功能。极度适合非硬实时且 RAM 资源紧张的小型单片机项目。](https://gitee.com/event-os/basic-os)  
**特征**：极简的协作式系统，所有的任务共享一个任务栈，包含简单的内核功能组件等。  

#### 要点

---

### TaskScheduler

[![GitHub Repo stars](https://img.shields.io/github/stars/arkhipenko/TaskScheduler)](https://github.com/arkhipenko/TaskScheduler/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/arkhipenko/TaskScheduler)](https://github.com/arkhipenko/TaskScheduler/commits) | [![GitHub License](https://img.shields.io/github/license/arkhipenko/TaskScheduler)]()

**链接**：[arkhipenko/TaskScheduler: Cooperative multitasking for Arduino, ESPx, STM32, nRF and other microcontrollers](https://github.com/arkhipenko/TaskScheduler)  
**特征**：协同多任务处理框架，抢占式编程，但不需要担心并发处理的安全问题。能够对任务的执行参数进行多种配置。  

#### 要点

- 使用介绍：[分享一个强大的协同多任务处理库](https://mp.weixin.qq.com/s/lhapcjI4JVzqI-VL3lnasg)

---

### QuarkTS

[![GitHub Repo stars](https://img.shields.io/github/stars/kmilo17pet/QuarkTS)](https://github.com/kmilo17pet/QuarkTS/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/kmilo17pet/QuarkTS)](https://github.com/kmilo17pet/QuarkTS/commits) | [![GitHub License](https://img.shields.io/github/license/kmilo17pet/QuarkTS)]()

**链接**：[kmilo17pet/QuarkTS: An open-source OS for embedded applications that supports prioritized cooperative scheduling, time control, inter-task communications primitives, hierarchical state machines and CoRoutines.](https://github.com/kmilo17pet/QuarkTS)  
**C++ 版链接**：[kmilo17pet/QuarkTS-cpp: The QuarkTS port for C++. An open-source OS for embedded applications that supports prioritized cooperative scheduling, time control, inter-task communications primitives, hierarchical state machines and CoRoutines.](https://github.com/kmilo17pet/QuarkTS-cpp)  
**特征**：事件驱动型多任务调度系统，是它无需考虑并发的陷阱（资源共享、竞争条件、死锁等...），并提供完整内核功能，符合多种行业标准，适合基础企业项目。  

#### 要点

---

### VSF

[![GitHub Repo stars](https://img.shields.io/github/stars/vsfteam/vsf)](https://github.com/vsfteam/vsf/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/vsfteam/vsf)](https://github.com/vsfteam/vsf/commits) | [![GitHub License](https://img.shields.io/github/license/vsfteam/vsf)]()

**链接**：[vsfteam/vsf: Versaloon Software Framework -- a tiny preemptive-capable event-driven incremental software framework for embedded systems](https://github.com/vsfteam/vsf)  
**特征**：是一个基于事件驱动的抢占式多任务框架，包含内核和常用的组件，适用于企业级项目。  

#### 要点

- 引入“皮肤”的概念，可以把任务伪装成其他系统的接口；

---

## RTOS

> 实时操作系统通常有两种模式——协同式和抢占式。它们的主要区别是任务移交方式，协同式 RTOS 需要任务主动让出 CPU 控制权，而抢占式 RTOS 则由内核调度器来决定执行哪个任务。伪代码如下 👇：
> ```c
> /* 协同式RTOS */
> void task_yield() {
>     save_context(current_task);    // 保存当前
>     current_task = next_task;      // 选择下一个
>     restore_context(current_task); // 恢复执行
> }
>
> // 任务说"换人"
> while(1) {
>     do_work();
>     task_yield();  // ← 不调用就卡死！
> }
> ```
>
> ```c
> /* 抢占式RTOS */
> void systick_isr() {
>     save_context(current_task);    // 保存当前
>     if (higher_priority_ready()) { // 检查优先级
>         current_task = highest_task(); // 选择最高
>     }
>     restore_context(current_task); // 恢复执行
> }
>
> // 系统说"换人"
> while(1) {
>     do_work();  // ← 不yield也能被切换
> }
> ```

### KLite

[![Gitee Repo stars](https://gitee.com/kerndev/klite/badge/star.svg?theme=gvp)](https://gitee.com/kerndev/klite/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/kerndev/klite&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/kerndev/klite&query=$.license&label=license)]()

**链接**：[KLite: 简洁易用的嵌入式操作系统内核。交流 QQ 群:317930646](https://gitee.com/kerndev/klite)  
**特征**：最简洁易用的 RTOS，附带最基本实用的内核功能。  

#### 要点

- 使用介绍：[分享一个简洁易用的嵌入式操作系统内核](https://mp.weixin.qq.com/s/uAMewkX7Ax_w3aQi7KUKhg)

---

### FreeRTOS

[![GitHub Repo stars](https://img.shields.io/github/stars/FreeRTOS/FreeRTOS)](https://github.com/FreeRTOS/FreeRTOS/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/FreeRTOS/FreeRTOS)](https://github.com/FreeRTOS/FreeRTOS/commits) | [![GitHub License](https://img.shields.io/github/license/FreeRTOS/FreeRTOS)]()

**链接**：[FreeRTOS™ - FreeRTOS™](https://www.freertos.org)  
**可单独使用的组件**：[FreeRTOS Core - FreeRTOS](https://www.freertos.org/zh-cn-cmn-s/freertos-core/overview.html)  
**依赖于 OS 内核的组件**：[FreeRTOS+ Feature libraries designed to work with FreeRTOS](https://www.freertos.org/zh-cn-cmn-s/FreeRTOS-Plus/index.html)  
**特征**：很多小厂商会使用的 OS，网上资料比较多，属于中规中矩那种，适合有一个基础项目，准备上 RTOS 的那种。  

#### 要点

- ~~参考：FreeRTOS~~（待发布）

---

### uC/OS

[![GitHub Repo stars](https://img.shields.io/github/stars/weston-embedded/uC-OS3)](https://github.com/weston-embedded/uC-OS3/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/weston-embedded/uC-OS3)](https://github.com/weston-embedded/uC-OS3/commits) | [![GitHub License](https://img.shields.io/github/license/weston-embedded/uC-OS3)]()

**链接**：[Overview - Weston Embedded Solutions](https://weston-embedded.com/micrium/overview)  
**特征**：早期比较流行的 OS，和 [FreeRTOS](#freertos) 特征差不多，功能比它强一些。  

#### 要点

- ~~参考：μC/OS~~（待发布）

---

### RT-Thread

[![GitHub Repo stars](https://img.shields.io/github/stars/RT-Thread/rt-thread)](https://github.com/RT-Thread/rt-thread/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/RT-Thread/rt-thread)](https://github.com/RT-Thread/rt-thread/commits) | [![GitHub License](https://img.shields.io/github/license/RT-Thread/rt-thread)]()

**链接**：[rt-thread.org](https://www.rt-thread.org)  
**Nano 版本，精简内核，不附带软件包或附加功能**：[Nano 简介与下载](https://www.rt-thread.org/document/site/#/rt-thread-version/rt-thread-nano/an0038-nano-introduction)  
**Smart 版本**：[smart 简介](https://www.rt-thread.org/document/site/#/rt-thread-version/rt-thread-smart/introduction/rt-smart-intro/rt-smart-intro)  
**特征**：国产里耀眼的星星，非常好且实用的 RTOS，附带多个组件和附加功能，文档详细，非常适合一个空白期的 OS 项目。  

#### 要点

- 通过 FinSH 组件进行控制台交互；
- 初始化使用 initcall 方式；
- 通过 Env 工具修改项目的 config 宏参数；
- ~~`xxx_EXPORT` 功能参考：段区注册及调用机制；~~（待发布）

---

### RTX

[![GitHub Repo stars](https://img.shields.io/github/stars/ARM-software/CMSIS-FreeRTOS)](https://github.com/ARM-software/CMSIS-FreeRTOS/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/ARM-software/CMSIS-FreeRTOS)](https://github.com/ARM-software/CMSIS-FreeRTOS/commits) | [![GitHub License](https://img.shields.io/github/license/ARM-software/CMSIS-FreeRTOS)]()

**链接**：[Main Page](https://arm-software.github.io/CMSIS_5/RTOS2/html/index.html)  
**特征**：ARM 公司的 RTOS，和 Keil 适配性较强。  

#### 要点

- 这个系统有好几代，而且很多都是附带在 ARM 的 MDK 包里。

---

### NuttX

[![GitHub Repo stars](https://img.shields.io/github/stars/apache/nuttx)](https://github.com/apache/nuttx/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/apache/nuttx)](https://github.com/apache/nuttx/commits) | [![GitHub License](https://img.shields.io/github/license/apache/nuttx)]()

**链接**：[apache/nuttx: Apache NuttX is a mature, real-time embedded operating system (RTOS)](https://github.com/apache/nuttx)  
**特征**：强调标准兼容和小型封装的操作系统，遵循 [POSIX](./appendix.md#什么是-posix) 标准和 ANSI 标准。  

#### 要点

---

### embOS

[![License: embOS](https://img.shields.io/badge/License-embOS-blue.svg)]()

**链接**：[embOS - RTOS](https://www.segger.com/products/rtos/embos/)  
**特征**：SEGGER 公司的 RTOS，可免费用于非商业用途。  

#### 要点

---

### Azure RTOS

[![GitHub Repo stars](https://img.shields.io/github/stars/eclipse-threadx/rtos-docs)](https://github.com/eclipse-threadx/rtos-docs/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/eclipse-threadx/rtos-docs)](https://github.com/eclipse-threadx/rtos-docs/commits) | [![GitHub License](https://img.shields.io/github/license/eclipse-threadx/rtos-docs)]()

**链接**：[Microsoft Azure RTOS 文档中心 | Microsoft Learn](https://learn.microsoft.com/zh-cn/azure/rtos/)  
**特征**：微软公司的 RTOS，具有丰富的组件。  

#### 要点

- 除了官网，硬汉论讨教程也十分丰富；
- 组件：ThreadX、NetX、FileX、GUIX、USBX、TraceX 等...

---

### Zephyr

[![GitHub Repo stars](https://img.shields.io/github/stars/zephyrproject-rtos/zephyr)](https://github.com/zephyrproject-rtos/zephyr/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/zephyrproject-rtos/zephyr)](https://github.com/zephyrproject-rtos/zephyr/commits) | [![GitHub License](https://img.shields.io/github/license/zephyrproject-rtos/zephyr)]()

**链接**：[The Zephyr Project – A proven RTOS ecosystem, by developers, for developers.](https://zephyrproject.org/)  
**特征**：Linux 维护的一个 RTOS，很适合学习 Linux 的开发思想。  

#### 要点

- 介绍：[Zephyr 会成为物联网时代 RTOS 的佼佼者？](https://mp.weixin.qq.com/s/TiFY68XX3x6trfffo5hvKQ)

---

### At-RTOS

[![GitHub Repo stars](https://img.shields.io/github/stars/At-EC/At-RTOS)](https://github.com/At-EC/At-RTOS/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/At-EC/At-RTOS)](https://github.com/At-EC/At-RTOS/commits) | [![GitHub License](https://img.shields.io/github/license/At-EC/At-RTOS)]()

**链接**：[At-EC/At-RTOS: At-RTOS is an open and user-friendly real-time operating system (RTOS) for embedded controller (EC).](https://github.com/At-EC/At-RTOS)  
**特征**：一个用户友好的嵌入式控制器实时操作系统，仅提供基本的内核功能。  

#### 要点

---

### Embox

[![GitHub Repo stars](https://img.shields.io/github/stars/embox/embox)](https://github.com/embox/embox/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/embox/embox)](https://github.com/embox/embox/commits) | [![GitHub License](https://img.shields.io/github/license/embox/embox)]()

**链接**：[Embox | Real-time operating system](https://embox.github.io/)  
**特征**：多任务操作系统，其特点是支持使用 Linux 开源组件而不使用 Linux 系统，该开源系统旨在任何地方都能够使用 Linux 软件。  

#### 要点

- 有时候想把 Linux 的一些功能裁剪出来自己用，此库就提供了非常好的借鉴方案；

---

### YiYiYa OS

[![GitHub Repo stars](https://img.shields.io/github/stars/evilbinary/YiYiYa)](https://github.com/evilbinary/YiYiYa/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/evilbinary/YiYiYa)](https://github.com/evilbinary/YiYiYa/commits) | [![GitHub License](https://img.shields.io/github/license/evilbinary/YiYiYa)]()

**链接**：[evilbinary/YiYiYa: YiYiYa 一个 os](https://github.com/evilbinary/YiYiYa)  
**特征**：功能全面的 OS 系统，架构从上而下分层设计，几乎可以将其视为简易版的安卓系统，适合手机那种类型的产品。  

#### 要点

---

### LK

[![GitHub Repo stars](https://img.shields.io/github/stars/littlekernel/lk)](https://github.com/littlekernel/lk/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/littlekernel/lk)](https://github.com/littlekernel/lk/commits) | [![GitHub License](https://img.shields.io/github/license/littlekernel/lk)]()

**链接**：[littlekernel/lk: LK embedded kernel](https://github.com/littlekernel/lk)  
**特征**：全称 Little Kernel，是一个微型嵌入式系统，其引导加载程序（BootLoader）最为出名，被作用于原生 Android 系统上。  

#### 要点

- 使用介绍：[一个被严重低估的嵌入式系统微内核！](https://mp.weixin.qq.com/s/M0v1vEp63zeqJE0wrGFU-g?color_scheme=light)

---

### SKRTOS\_sparrow

[![GitHub Repo stars](https://img.shields.io/github/stars/skaiui2/SKRTOS_sparrow)](https://github.com/skaiui2/SKRTOS_sparrow/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/skaiui2/SKRTOS_sparrow)](https://github.com/skaiui2/SKRTOS_sparrow/commits) | [![GitHub License](https://img.shields.io/github/license/skaiui2/SKRTOS_sparrow)]()

**链接**：[skaiui2/SKRTOS_sparrow: Lightweight rtos inspired by SKRTOS](https://github.com/skaiui2/SKRTOS_sparrow)  
**特征**：仅几百行的超微小系统，实现了基本调度和 IPC 机制，有人称之为儿童版 FreeRTOS。  

#### 要点

---

### CosyOS

[![Gitee Repo stars](https://gitee.com/cosyos/cosyos/badge/star.svg?theme=gvp)](https://gitee.com/cosyos/cosyos/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/cosyos/cosyos&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/cosyos/cosyos&query=$.license&label=license)]()

**链接**：[CosyOS: CosyOS 是一款来自中国的开源实时操作系统，从经典的 8051 内核，到流行的 Arm Cortex-M 内核，均可实现全局不关总中断、零中断延迟，适用于对系统实时性及中断响应速度有较高要求的场合。QQ 交流群：303421780.](https://gitee.com/cosyos/cosyos)  
**特征**：零中断延迟的操作系统，可实现全局不关总中断而保持实时性，包含很多创新实用的内核功能。  

#### 要点

---

### scmRTOS

[![GitHub Repo stars](https://img.shields.io/github/stars/scmrtos/scmrtos)](https://github.com/scmrtos/scmrtos/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/scmrtos/scmrtos)](https://github.com/scmrtos/scmrtos/commits) | [![GitHub License](https://img.shields.io/github/license/scmrtos/scmrtos)]()

**链接**：[scmrtos/scmrtos: scmRTOS embedded operating system](https://github.com/scmrtos/scmrtos)  
**特征**：C++ 编写的轻量级的 RTOS，仅提供调度和消息等最基本的内核功能。  

#### 要点

---

### MuditaOS

[![GitHub Repo stars](https://img.shields.io/github/stars/mudita/MuditaOS)](https://github.com/mudita/MuditaOS/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/mudita/MuditaOS)](https://github.com/mudita/MuditaOS/commits) | [![GitHub License](https://img.shields.io/github/license/mudita/MuditaOS)]()

**链接**：[MuditaOS - Open Source E Ink mobile operating system | Mudita](https://mudita.com/products/phones/mudita-pure/muditaos/)  
**特征**：基于 [FreeRTOS](#freertos) 构建，专为 E-Ink 显示屏优化的移动操作系统。  

#### 要点

---

## IoT-RTOS

### Contiki-NG

[![GitHub Repo stars](https://img.shields.io/github/stars/contiki-ng/contiki-ng)](https://github.com/contiki-ng/contiki-ng/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/contiki-ng/contiki-ng)](https://github.com/contiki-ng/contiki-ng/commits) | [![GitHub License](https://img.shields.io/github/license/contiki-ng/contiki-ng)]()

**链接**：[contiki-ng/contiki-ng: Contiki-NG: The OS for Next Generation IoT Devices](https://github.com/contiki-ng/contiki-ng)  
**特征**：uIP 和 LwIP 的作者维护的多任务物联网操作系统，它专注于可靠（安全可靠）的低功耗通信和标准互联网协议。  

#### 要点

---

### Mbed OS

[![GitHub Repo stars](https://img.shields.io/github/stars/ARMmbed/mbed-os)](https://github.com/ARMmbed/mbed-os/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/ARMmbed/mbed-os)](https://github.com/ARMmbed/mbed-os/commits) | [![GitHub License](https://img.shields.io/github/license/ARMmbed/mbed-os)]()

**链接**：[Mbed OS | Mbed](https://os.mbed.com/mbed-os/)  
**特征**：arm 旗下的易于使用的物联网操作系统。  

#### 要点

---

### Huawei LiteOS

[![Gitee Repo stars](https://gitee.com/LiteOS/LiteOS/badge/star.svg?theme=gvp)](https://gitee.com/LiteOS/LiteOS/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/LiteOS/LiteOS&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/LiteOS/LiteOS&query=$.license&label=license)]()

**链接**：[Huawei LiteOS: 轻量级操作系统，驱动万物感知 互联 智能](https://gitee.com/LiteOS)  
**特征**：华为旗下针对物联网领域推出的轻量级物联网操作系统。  

#### 要点

---

### Xiaomi Vela

**链接**：[iot.mi.com/vela](https://iot.mi.com/vela)  
**特征**：小米旗下的物联网操作系统，底层基于 [NuttX](#nuttx) 构建。内核打造。  

#### 要点

---

### AliOS Things

[![Gitee Repo stars](https://gitee.com/alios-things-admin/AliOS-Things/badge/star.svg?theme=gvp)](https://gitee.com/alios-things-admin/AliOS-Things/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/alios-things-admin/AliOS-Things&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/alios-things-admin/AliOS-Things&query=$.license&label=license)]()

**链接**：[AliOS Things: AliOS Things 是由开放原子开源基金会（OpenAtom Foundation）孵化及运营的开源项目，是面向开发者的新一代物联网操作系统。](https://gitee.com/alios-things)  
**特征**：阿里旗下面向 IoT 领域的、高可伸缩的物联网操作系统。  

#### 要点

---

### TencentOS Tiny

[![Gitee Repo stars](https://gitee.com/Tencent/TencentOS-tiny/badge/star.svg?theme=gvp)](https://gitee.com/Tencent/TencentOS-tiny/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Tencent/TencentOS-tiny&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Tencent/TencentOS-tiny&query=$.license&label=license)]()

**链接**：[TencentOS-tiny: TencentOS tiny 是腾讯面向物联网领域开发的实时操作系统，具有低功耗，低资源占用，模块化，安全可靠等特点，可有效提升物联网终端产品开发效率](https://gitee.com/Tencent/TencentOS-tiny)  
**特征**：是腾讯面向物联网领域开发的实时操作系统。  

#### 要点

---

### OneOS

**链接**：[OneOS - 中国移动物联网操作系统](https://os.iot.10086.cn/)  
**特征**：是中国移动针对物联网领域推出的轻量级操作系统，具有可裁剪、跨平台、低功耗、高安全等特点，支持 ARM Cortex-M/A、MIPS、RISC-V 等主流芯片架构，兼容 POSIX、CMSIS 等标准接口，支持 JavaScript、Micropython 语言开发。  

#### 要点

---

### LuatOS

[![Gitee Repo stars](https://gitee.com/openLuat/LuatOS/badge/star.svg?theme=gvp)](https://gitee.com/openLuat/LuatOS/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/openLuat/LuatOS&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/openLuat/LuatOS&query=$.license&label=license)]()

**链接**：[LuatOS 文档](https://wiki-zh.luatos.org)  
**特征**：一款针对嵌入式的 Lua 脚本运行框架，包含了一个系统的功能体量。  

#### 要点

- 目前支持的 MCU 比较单一；

---

### Lua-RTOS-ESP32

[![GitHub Repo stars](https://img.shields.io/github/stars/whitecatboard/Lua-RTOS-ESP32)](https://github.com/whitecatboard/Lua-RTOS-ESP32/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/whitecatboard/Lua-RTOS-ESP32)](https://github.com/whitecatboard/Lua-RTOS-ESP32/commits) | [![GitHub License](https://img.shields.io/github/license/whitecatboard/Lua-RTOS-ESP32)]()

**链接**：[whitecatboard/Lua-RTOS-ESP32: Lua RTOS for ESP32](https://github.com/whitecatboard/Lua-RTOS-ESP32)  
**特征**：是一种支持 Lua 解释器的实时操作系统，提供了 Lua 所需所有资源和基本模块、中间件，可以移植到其他 32 位平台。  

#### 要点

---

### Apache Mynewt OS

[![GitHub Repo stars](https://img.shields.io/github/stars/apache/mynewt-core)](https://github.com/apache/mynewt-core/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/apache/mynewt-core)](https://github.com/apache/mynewt-core/commits) | [![GitHub License](https://img.shields.io/github/license/apache/mynewt-core)]()

**链接**：[apache/mynewt-core: An OS to build, deploy and securely manage billions of devices](https://github.com/apache/mynewt-core)  
**特征**：Apache 旗下专为低功耗无线设备所设计的 OS，自带蓝牙协议栈和 IEEE 通信协议，开箱即用。  

#### 要点

---

### Mongoose OS

[![GitHub Repo stars](https://img.shields.io/github/stars/cesanta/mongoose-os)](https://github.com/cesanta/mongoose-os/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/cesanta/mongoose-os)](https://github.com/cesanta/mongoose-os/commits) | [![GitHub License](https://img.shields.io/github/license/cesanta/mongoose-os)]()

**链接**：[Mongoose OS - reduce IoT firmware development time up to 90%](https://mongoose-os.com/)  
**特征**：物联网固件开发框架，支持 C/JavaScript 语言开发，对远程管理及升级有较好支持。开源版功能受限。  

#### 要点

---

### MicroPythonOS

[![GitHub Repo stars](https://img.shields.io/github/stars/MicroPythonOS/MicroPythonOS)](https://github.com/MicroPythonOS/MicroPythonOS/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/MicroPythonOS/MicroPythonOS)](https://github.com/MicroPythonOS/MicroPythonOS/commits) | [![GitHub License](https://img.shields.io/github/license/MicroPythonOS/MicroPythonOS)]()

**链接**：[MicroPythonOS - The Ultimate MicroPython Operating System](https://micropythonos.com/)  
**特征**：MicroPython 构建的轻量级多功能作系统，专为 ESP32 和桌面系统等微控制器而设计，提供类似 Android 的现代触屏界面、应用商店、OTA 等功能。  

#### 要点

---

## ROS

### ROS

[![License: Apache 2.0](https://img.shields.io/badge/license-Apache%202.0-brightgreen.svg)](https://opensource.org/licenses/Apache-2.0)

**链接**：[ROS: Home](https://www.ros.org/)  
**特征**：业界有名的开源机器人操作系统，它实现了一整套的软件库和工具集。  

#### 要点

- 这个系统原本不是直接部署在 MCU 上的，而是 Linux 上的，但目前也支持微处理器和 Windows 系统；

---

### AimRT

[![GitHub Repo stars](https://img.shields.io/github/stars/AimRT/AimRT)](https://github.com/AimRT/AimRT/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/AimRT/AimRT)](https://github.com/AimRT/AimRT/commits) | [![GitHub License](https://img.shields.io/github/license/AimRT/AimRT)]()

**链接**：[aimrt.org](https://aimrt.org/)  
**特征**：是一个基于 Modern C++ 开发，面向现代机器人领域的运行时开发框架。提供了全面的插件开发接口，具有高度可扩展性，与其他 ROS 生态兼容。  

#### 要点

---
