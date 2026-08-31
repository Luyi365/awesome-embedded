# System and Thread Library
<!-- i18n:language-selector:start -->
[中文](README.md) | **English**
<!-- i18n:language-selector:end -->

> OSs generally fall into two categories: bare-metal systems and RTOSs. Here, however, I divide them into five categories:
>
> - [Time-Slice Scheduling Systems](#time-slice-scheduling-systems): timers or polling control task execution;
> - [Quasi-Real-Time Systems](#quasi-real-time-systems): emphasize hard real-time task stacks but have not yet reached the RTOS level;
> - [RTOS](#rtos): provide rich kernel functions and real-time capabilities;
> - [IoT-RTOS](#iot-rtos): in addition to RTOS characteristics, focus on IoT transmission; most follow the [POSIX](./appendix.en.md#what-is-posix) standard and are compatible with Linux;
> - [ROS](#ros): robot-specific systems that generally use distributed communication frameworks to help program processes communicate more conveniently. Therefore, they do not control all robot-component modules, but manage each component, which can itself use a different OS.

## Time-Slice Scheduling Systems

### ztask

[![GitHub Repo stars](https://img.shields.io/github/stars/tomzbj/ztask)](https://github.com/tomzbj/ztask/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/tomzbj/ztask)](https://github.com/tomzbj/ztask/commits) | [![GitHub License](https://img.shields.io/github/license/tomzbj/ztask)]()

**Link** - [GitHub - tomzbj/ztask: A simple timer-based scheduler](https://github.com/tomzbj/ztask)  
**Features** - An extremely simple time-slice scheduler with only five APIs; the kind of framework you could write on the fly.  

#### Key Points

---

### ETP

[![Gitee Repo stars](https://gitee.com/ecbm/timeslice-polling/badge/star.svg?theme=gvp)](https://gitee.com/ecbm/timeslice-polling/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/ecbm/timeslice-polling&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/ecbm/timeslice-polling&query=$.license&label=license)]()

**Link** - [Time-slice polling framework: This is a cross-platform ETP (Ecbm-Timeslice-Polling) framework. It uses time-slice polling; tasks are non-preemptive, and priority is determined by the order in which tasks are installed.](https://gitee.com/ecbm/timeslice-polling)  
**Features** - A time-slice polling framework intended to decouple tasks with different time slices in the main polling loop; it is the most basic polling framework.  

#### Key Points

---

### cotTask

[![Gitee Repo stars](https://gitee.com/cot_package/cot_task/badge/star.svg?theme=gvp)](https://gitee.com/cot_package/cot_task/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/cot_package/cot_task&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/cot_package/cot_task&query=$.license&label=license)]()

**Link** - [cotTask: A module component for task scheduling on embedded devices using timers](https://gitee.com/cot_package/cot_task)  
**Features** - A time-slice polling framework for initialization, startup, and task-scheduling management.  

#### Key Points

- The preceding link has the same content as [cTask](https://gitee.com/const-zpc/cTask); use either one;
- Unlike [ETP](#etp), it can set task priorities;
- Usage guide: [Open-source task scheduling code](https://mp.weixin.qq.com/s/7rf_9xq63wi0muo63bqkSw)

---

### CodeBrick

[![Gitee Repo stars](https://gitee.com/moluo-tech/CodeBrick/badge/star.svg?theme=gvp)](https://gitee.com/moluo-tech/CodeBrick/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/moluo-tech/CodeBrick&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/moluo-tech/CodeBrick&query=$.license&label=license)]()

**Link** - [CodeBrick: A practical MCU software management system without an OS, including a task polling framework, command manager, low-power management, ring buffer, and other practical modules.](https://gitee.com/moluo-tech/CodeBrick)  
**Features** - A time-slice polling framework including task polling management, a command manager, low-power management, ring buffers, and other practical modules, without a driver layer.  

#### Key Points

- Module initialization, task loading, and CLI command loading are all performed by registering them to a memory segment.
- Usage guide: [A practical microcontroller software framework](https://mp.weixin.qq.com/s/hCmV3kJTC_TFXSzuklmUVA)

---

### vkern

[![Gitee Repo stars](https://gitee.com/Lamdonn/vkern/badge/star.svg?theme=gvp)](https://gitee.com/Lamdonn/vkern/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Lamdonn/vkern&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Lamdonn/vkern&query=$.license&label=license)]()

**Link** - [vkern: A simple periodic task scheduling kernel](https://gitee.com/Lamdonn/vkern)  
**Features** - A task scheduling kernel written by imitating the RTOS architecture; its principle is still to use timers to create a foreground-background system.  

#### Key Points

---

### cola_os

[![Gitee Repo stars](https://gitee.com/schuck/cola_os/badge/star.svg?theme=gvp)](https://gitee.com/schuck/cola_os/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/schuck/cola_os&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/schuck/cola_os&query=$.license&label=license)]()

**Link** - [cola_os: An OS implementing multitasking management in 300 lines of code. In much MCU development, functionality is simple and real-time requirements are not strict; using an RTOS seems wasteful, while many poorly managed tasks become chaotic, hence the idea of polling task management. Simple and easy to use! CSDN:https://blog.csdn.net/ziqi5543/article/details/101512722](https://gitee.com/schuck/cola_os)  
**Features** - A foreground-background system containing an initcall initialization mechanism, an rt_thread-like hardware abstraction layer, a task pool, and a Timer pool.  

#### Key Points

- The core adds linked lists on top of bare metal to manage processes, decoupling the main loop into multiple independent tasks;
- Apart from code size, it consumes no other resources, so using this OS does not affect power consumption or performance and is well suited to somewhat complex bare-metal systems;
- Compiling the `cola_init` component with AC6 produces an error; see: [Problem when using ARM Compiler 6, needs fixing · Issue #I6TF6K · schuck/cola_os - Gitee.com](https://gitee.com/schuck/cola_os/issues/I6TF6K)
- Usage guide: [Embedded miscellany weekly | Issue 4](https://mp.weixin.qq.com/s/7seVk1q5SOa3Lq_yU3_XOQ)

---

### JxOS

[![Gitee Repo stars](https://gitee.com/jeremyceng/JxOS/badge/star.svg?theme=gvp)](https://gitee.com/jeremyceng/JxOS/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/jeremyceng/JxOS&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/jeremyceng/JxOS&query=$.license&label=license)]()

**Link** - [JxOS: A small foreground-background system for MCUs. Its design philosophy is to highly decouple functional modules from hardware to improve code-module reusability; avoid complex data structures and syntax to improve compatibility across hardware platforms and compilers, enabling rapid project porting between MCUs; provide practical, stable, and commonly used functional modules for rapid project development; and define a standard application-development framework to reduce the workload and difficulty of application development.](https://gitee.com/jeremyceng/JxOS)  
**Features** - A foreground-background system with no complex registration or function-pointer structures, providing system kernel functions: tasks, events, messages, bulletin boards, mailboxes, pipes, registration, memory allocation...  

#### Key Points

- It contains many small functions and is clearly decoupled, so they can be ported one by one as needed.
- Usage guide: [A small foreground-background system for MCUs](https://mp.weixin.qq.com/s/Qlir_JqmOJtdNkuAeygoQQ)

---

### EventOS

[![Gitee Repo stars](https://gitee.com/event-os/eventos/badge/star.svg?theme=gvp)](https://gitee.com/event-os/eventos/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/event-os/eventos&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/event-os/eventos&query=$.license&label=license)]()

**Link** - [eventos: An event-driven, ultra-lightweight embedded development framework. It occupies as little as 1.5 KB ROM and 172 bytes RAM. Its core technology is an event bus and it supports both Reactor and state-machine modes; it has a cooperative kernel, is extremely reliable, can be deeply tailored, and is easy to port.](https://gitee.com/event-os/eventos)  
**Features** - An event-driven embedded system that provides kernel functions and more.  

#### Key Points

---

### BabyOS

[![Gitee Repo stars](https://gitee.com/notrynohigh/BabyOS/badge/star.svg?theme=gvp)](https://gitee.com/notrynohigh/BabyOS/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/notrynohigh/BabyOS&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/notrynohigh/BabyOS&query=$.license&label=license)]()

**Link** - [BabyOS: A code framework designed to accelerate MCU project development](https://gitee.com/notrynohigh/BabyOS)  
**Features** - A registration-service framework for bare-metal MCU projects. It manages functional modules and peripheral drivers, has very clear code layering and standards, RTT-like "MenuConfig" terminal configuration, and PC simulation.  

#### Key Points

- Because it uses a shelf structure, this OS aims to provide convenient, replaceable, verifiable, and storable code structures for bare-metal MCUs. It is therefore well suited to project development at small and medium-sized companies.
- Because it has terminal configuration capabilities, new code must be written strictly according to the rules provided by this OS.
- Usage guide: [A framework for managing functional modules and peripheral drivers](https://mp.weixin.qq.com/s/3yeVTiNWkLj1yevq3lSb9Q)

---

## Quasi-Real-Time Systems

### cotOs

[![Gitee Repo stars](https://gitee.com/cot_package/cot_os/badge/star.svg?theme=gvp)](https://gitee.com/cot_package/cot_os/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/cot_package/cot_os&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/cot_package/cot_os&query=$.license&label=license)]()

**Link** - [cotOs: A simple query-based cooperative multitasking scheduling system for embedded devices implemented with setjmp/longjmp](https://gitee.com/cot_package/cot_os)  
**Features** - A simple query-based cooperative multitasking system that does not require timers for task switching; it creates tasks like RTOS does, but provides no other functions.  

#### Key Points

- Comparisons with other bare-metal OSs and RTOSs are provided in the link;
- Usage guide: [Query-based cooperative multitasking system](https://mp.weixin.qq.com/s/qouyA6IApyktT9XxSFTuYA)

---

### BasicOS

[![Gitee Repo stars](https://gitee.com/event-os/basic-os/badge/star.svg?theme=gvp)](https://gitee.com/event-os/basic-os/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/event-os/basic-os&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/event-os/basic-os&query=$.license&label=license)]()

**Link** - [basic-os: A cooperative kernel supporting a shared task stack, specifically intended for MCUs with little RAM. It currently provides basic functions such as shared-stack task scheduling and software timers, and is exceptionally suitable for small microcontroller projects that are not hard real-time and have tight RAM resources.](https://gitee.com/event-os/basic-os)  
**Features** - An extremely simple cooperative system in which all tasks share one task stack, including simple kernel functional components and more.  

#### Key Points

---

### TaskScheduler

[![GitHub Repo stars](https://img.shields.io/github/stars/arkhipenko/TaskScheduler)](https://github.com/arkhipenko/TaskScheduler/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/arkhipenko/TaskScheduler)](https://github.com/arkhipenko/TaskScheduler/commits) | [![GitHub License](https://img.shields.io/github/license/arkhipenko/TaskScheduler)]()

**Link** - [arkhipenko/TaskScheduler: Cooperative multitasking for Arduino, ESPx, STM32, nRF and other microcontrollers](https://github.com/arkhipenko/TaskScheduler)  
**Features** - A cooperative multitasking framework with preemptive programming, but without concerns about concurrent-processing safety. It supports various configurations of task execution parameters.  

#### Key Points

- Usage guide: [A powerful cooperative multitasking library](https://mp.weixin.qq.com/s/lhapcjI4JVzqI-VL3lnasg)

---

### QuarkTS

[![GitHub Repo stars](https://img.shields.io/github/stars/kmilo17pet/QuarkTS)](https://github.com/kmilo17pet/QuarkTS/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/kmilo17pet/QuarkTS)](https://github.com/kmilo17pet/QuarkTS/commits) | [![GitHub License](https://img.shields.io/github/license/kmilo17pet/QuarkTS)]()

**Link** - [kmilo17pet/QuarkTS: An open-source OS for embedded applications that supports prioritized cooperative scheduling, time control, inter-task communications primitives, hierarchical state machines and CoRoutines.](https://github.com/kmilo17pet/QuarkTS)  
**C++ Version Link** - [kmilo17pet/QuarkTS-cpp: The QuarkTS port for C++. An open-source OS for embedded applications that supports prioritized cooperative scheduling, time control, inter-task communications primitives, hierarchical state machines and CoRoutines.](https://github.com/kmilo17pet/QuarkTS-cpp)  
**Features** - An event-driven multitasking scheduling system that avoids concurrency pitfalls (resource sharing, race conditions, deadlocks, and so on) and provides complete kernel functions, complies with multiple industry standards, and is suitable for basic enterprise projects.  

#### Key Points

---

### VSF

[![GitHub Repo stars](https://img.shields.io/github/stars/vsfteam/vsf)](https://github.com/vsfteam/vsf/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/vsfteam/vsf)](https://github.com/vsfteam/vsf/commits) | [![GitHub License](https://img.shields.io/github/license/vsfteam/vsf)]()

**Link** - [vsfteam/vsf: Versaloon Software Framework -- a tiny preemptive-capable event-driven incremental software framework for embedded systems](https://github.com/vsfteam/vsf)  
**Features** - An event-driven preemptive multitasking framework that includes a kernel and commonly used components, suitable for enterprise-level projects.  

#### Key Points

- Introduces the concept of "skins," which can disguise tasks as interfaces of other systems;

---

## RTOS

> Real-time operating systems usually have two modes: cooperative and preemptive. Their main difference is how tasks are handed over. A cooperative RTOS requires tasks to voluntarily relinquish CPU control, while a preemptive RTOS has the kernel scheduler decide which task to execute. The pseudocode is as follows:
> ```c
> /* Cooperative RTOS */
> void task_yield() {
>     save_context(current_task);    // Save current task
>     current_task = next_task;      // Select next task
>     restore_context(current_task); // Resume execution
> }
>
> // The task says "switch"
> while(1) {
>     do_work();
>     task_yield();  // <- It hangs if not called!
> }
> ```
>
> ```c
> /* Preemptive RTOS */
> void systick_isr() {
>     save_context(current_task);    // Save current task
>     if (higher_priority_ready()) { // Check priority
>         current_task = highest_task(); // Select highest
>     }
>     restore_context(current_task); // Resume execution
> }
>
> // The system says "switch"
> while(1) {
>     do_work();  // Can be switched even without yield
> }
> ```

### KLite

[![Gitee Repo stars](https://gitee.com/kerndev/klite/badge/star.svg?theme=gvp)](https://gitee.com/kerndev/klite/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/kerndev/klite&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/kerndev/klite&query=$.license&label=license)]()

**Link** - [KLite: A concise and easy-to-use embedded operating system kernel. QQ discussion group: 317930646](https://gitee.com/kerndev/klite)  
**Features** - A very concise and easy-to-use RTOS with the most basic practical kernel functions.  

#### Key Points

- Usage guide: [A concise and easy-to-use embedded operating system kernel](https://mp.weixin.qq.com/s/uAMewkX7Ax_w3aQi7KUKhg)

---

### FreeRTOS

[![GitHub Repo stars](https://img.shields.io/github/stars/FreeRTOS/FreeRTOS)](https://github.com/FreeRTOS/FreeRTOS/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/FreeRTOS/FreeRTOS)](https://github.com/FreeRTOS/FreeRTOS/commits) | [![GitHub License](https://img.shields.io/github/license/FreeRTOS/FreeRTOS)]()

**Link** - [FreeRTOS™ - FreeRTOS™](https://www.freertos.org)  
**Independently Usable Components** - [FreeRTOS Core - FreeRTOS](https://www.freertos.org/zh-cn-cmn-s/freertos-core/overview.html)  
**Components Dependent on the OS Kernel** - [FreeRTOS+ Feature libraries designed to work with FreeRTOS](https://www.freertos.org/zh-cn-cmn-s/FreeRTOS-Plus/index.html)  
**Features** - An OS used by many small vendors, with abundant online materials. It is fairly conventional and suitable for a basic project preparing to adopt an RTOS.  

#### Key Points

- ~~Reference: FreeRTOS~~ (to be released)

---

### uC/OS

[![GitHub Repo stars](https://img.shields.io/github/stars/weston-embedded/uC-OS3)](https://github.com/weston-embedded/uC-OS3/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/weston-embedded/uC-OS3)](https://github.com/weston-embedded/uC-OS3/commits) | [![GitHub License](https://img.shields.io/github/license/weston-embedded/uC-OS3)]()

**Link** - [Overview - Weston Embedded Solutions](https://weston-embedded.com/micrium/overview)  
**Features** - An OS that was relatively popular early on. Its features are similar to [FreeRTOS](#freertos), but it has somewhat stronger functionality.  

#### Key Points

- ~~Reference: μC/OS~~ (to be released)

---

### RT-Thread

[![GitHub Repo stars](https://img.shields.io/github/stars/RT-Thread/rt-thread)](https://github.com/RT-Thread/rt-thread/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/RT-Thread/rt-thread)](https://github.com/RT-Thread/rt-thread/commits) | [![GitHub License](https://img.shields.io/github/license/RT-Thread/rt-thread)]()

**Link** - [rt-thread.org](https://www.rt-thread.org)  
**Nano Version, a streamlined kernel without packages or extra functions** - [Nano Introduction and Download](https://www.rt-thread.org/document/site/#/rt-thread-version/rt-thread-nano/an0038-nano-introduction)  
**Smart Version** - [smart introduction](https://www.rt-thread.org/document/site/#/rt-thread-version/rt-thread-smart/introduction/rt-smart-intro/rt-smart-intro)  
**Features** - A shining star among domestic products, an excellent and practical RTOS with multiple components and extra functions. Its detailed documentation makes it very suitable for an OS project starting from scratch.  

#### Key Points

- Provides console interaction through the FinSH component;
- Uses initcall for initialization;
- Uses the Env tool to modify project config macro parameters;
- ~~`xxx_EXPORT` feature reference: segment registration and invocation mechanism;~~ (to be released)

---

### RTX

[![GitHub Repo stars](https://img.shields.io/github/stars/ARM-software/CMSIS-FreeRTOS)](https://github.com/ARM-software/CMSIS-FreeRTOS/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/ARM-software/CMSIS-FreeRTOS)](https://github.com/ARM-software/CMSIS-FreeRTOS/commits) | [![GitHub License](https://img.shields.io/github/license/ARM-software/CMSIS-FreeRTOS)]()

**Link** - [Main Page](https://arm-software.github.io/CMSIS_5/RTOS2/html/index.html)  
**Features** - ARM's RTOS, with strong compatibility with Keil.  

#### Key Points

- This system has several generations, and many are included in ARM's MDK package.

---

### NuttX

[![GitHub Repo stars](https://img.shields.io/github/stars/apache/nuttx)](https://github.com/apache/nuttx/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/apache/nuttx)](https://github.com/apache/nuttx/commits) | [![GitHub License](https://img.shields.io/github/license/apache/nuttx)]()

**Link** - [apache/nuttx: Apache NuttX is a mature, real-time embedded operating system (RTOS)](https://github.com/apache/nuttx)  
**Features** - An operating system emphasizing standard compatibility and compact packaging that follows the [POSIX](./appendix.en.md#what-is-posix) standard and ANSI standards.  

#### Key Points

---

### embOS

[![License: embOS](https://img.shields.io/badge/License-embOS-blue.svg)]()

**Link** - [embOS - RTOS](https://www.segger.com/products/rtos/embos/)  
**Features** - SEGGER's RTOS, free for non-commercial use.  

#### Key Points

---

### Azure RTOS

[![GitHub Repo stars](https://img.shields.io/github/stars/eclipse-threadx/rtos-docs)](https://github.com/eclipse-threadx/rtos-docs/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/eclipse-threadx/rtos-docs)](https://github.com/eclipse-threadx/rtos-docs/commits) | [![GitHub License](https://img.shields.io/github/license/eclipse-threadx/rtos-docs)]()

**Link** - [Microsoft Azure RTOS Documentation Center | Microsoft Learn](https://learn.microsoft.com/zh-cn/azure/rtos/)  
**Features** - Microsoft's RTOS, with a rich set of components.  

#### Key Points

- In addition to the official website, the Hardcore forum tutorials are also very comprehensive;
- Components: ThreadX, NetX, FileX, GUIX, USBX, TraceX, and more...

---

### Zephyr

[![GitHub Repo stars](https://img.shields.io/github/stars/zephyrproject-rtos/zephyr)](https://github.com/zephyrproject-rtos/zephyr/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/zephyrproject-rtos/zephyr)](https://github.com/zephyrproject-rtos/zephyr/commits) | [![GitHub License](https://img.shields.io/github/license/zephyrproject-rtos/zephyr)]()

**Link** - [The Zephyr Project – A proven RTOS ecosystem, by developers, for developers.](https://zephyrproject.org/)  
**Features** - An RTOS maintained by Linux, well suited to learning Linux development philosophy.  

#### Key Points

- Introduction: [Will Zephyr become a leader among RTOSs in the IoT era?](https://mp.weixin.qq.com/s/TiFY68XX3x6trfffo5hvKQ)

---

### At-RTOS

[![GitHub Repo stars](https://img.shields.io/github/stars/At-EC/At-RTOS)](https://github.com/At-EC/At-RTOS/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/At-EC/At-RTOS)](https://github.com/At-EC/At-RTOS/commits) | [![GitHub License](https://img.shields.io/github/license/At-EC/At-RTOS)]()

**Link** - [At-EC/At-RTOS: At-RTOS is an open and user-friendly real-time operating system (RTOS) for embedded controller (EC).](https://github.com/At-EC/At-RTOS)  
**Features** - A user-friendly real-time operating system for embedded controllers, providing only basic kernel functions.  

#### Key Points

---

### Embox

[![GitHub Repo stars](https://img.shields.io/github/stars/embox/embox)](https://github.com/embox/embox/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/embox/embox)](https://github.com/embox/embox/commits) | [![GitHub License](https://img.shields.io/github/license/embox/embox)]()

**Link** - [Embox | Real-time operating system](https://embox.github.io/)  
**Features** - A multitasking operating system characterized by supporting Linux open-source components without using Linux itself. This open-source system aims to make Linux software usable everywhere.  

#### Key Points

- When you want to tailor out and use some Linux functions yourself, this library provides an excellent reference solution;

---

### YiYiYa OS

[![GitHub Repo stars](https://img.shields.io/github/stars/evilbinary/YiYiYa)](https://github.com/evilbinary/YiYiYa/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/evilbinary/YiYiYa)](https://github.com/evilbinary/YiYiYa/commits) | [![GitHub License](https://img.shields.io/github/license/evilbinary/YiYiYa)]()

**Link** - [evilbinary/YiYiYa: YiYiYa, an OS](https://github.com/evilbinary/YiYiYa)  
**Features** - A full-featured OS with an architecture designed in layers from top to bottom. It can almost be regarded as a simplified Android system, suitable for phone-like products.  

#### Key Points

---

### LK

[![GitHub Repo stars](https://img.shields.io/github/stars/littlekernel/lk)](https://github.com/littlekernel/lk/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/littlekernel/lk)](https://github.com/littlekernel/lk/commits) | [![GitHub License](https://img.shields.io/github/license/littlekernel/lk)]()

**Link** - [littlekernel/lk: LK embedded kernel](https://github.com/littlekernel/lk)  
**Features** - Short for Little Kernel, a tiny embedded system whose BootLoader is particularly well known and used in native Android systems.  

#### Key Points

- Usage guide: [A seriously underrated embedded-system microkernel!](https://mp.weixin.qq.com/s/M0v1vEp63zeqJE0wrGFU-g?color_scheme=light)

---

### SKRTOS\_sparrow

[![GitHub Repo stars](https://img.shields.io/github/stars/skaiui2/SKRTOS_sparrow)](https://github.com/skaiui2/SKRTOS_sparrow/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/skaiui2/SKRTOS_sparrow)](https://github.com/skaiui2/SKRTOS_sparrow/commits) | [![GitHub License](https://img.shields.io/github/license/skaiui2/SKRTOS_sparrow)]()

**Link** - [skaiui2/SKRTOS_sparrow: Lightweight rtos inspired by SKRTOS](https://github.com/skaiui2/SKRTOS_sparrow)  
**Features** - An ultra-small system of only a few hundred lines that implements basic scheduling and IPC mechanisms; some call it a children's version of FreeRTOS.  

#### Key Points

---

### CosyOS

[![Gitee Repo stars](https://gitee.com/cosyos/cosyos/badge/star.svg?theme=gvp)](https://gitee.com/cosyos/cosyos/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/cosyos/cosyos&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/cosyos/cosyos&query=$.license&label=license)]()

**Link** - [CosyOS: CosyOS is an open-source real-time operating system from China. From classic 8051 cores to popular Arm Cortex-M cores, it can achieve no global interrupt disablement and zero interrupt latency, suitable for scenarios with high requirements for system real-time performance and interrupt response speed. QQ discussion group: 303421780.](https://gitee.com/cosyos/cosyos)  
**Features** - An operating system with zero interrupt latency that can maintain real-time performance without globally disabling interrupts, including many innovative and practical kernel functions.  

#### Key Points

---

### scmRTOS

[![GitHub Repo stars](https://img.shields.io/github/stars/scmrtos/scmrtos)](https://github.com/scmrtos/scmrtos/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/scmrtos/scmrtos)](https://github.com/scmrtos/scmrtos/commits) | [![GitHub License](https://img.shields.io/github/license/scmrtos/scmrtos)]()

**Link** - [scmrtos/scmrtos: scmRTOS embedded operating system](https://github.com/scmrtos/scmrtos)  
**Features** - A lightweight RTOS written in C++, providing only the most basic kernel functions such as scheduling and messages.  

#### Key Points

---

### MuditaOS

[![GitHub Repo stars](https://img.shields.io/github/stars/mudita/MuditaOS)](https://github.com/mudita/MuditaOS/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/mudita/MuditaOS)](https://github.com/mudita/MuditaOS/commits) | [![GitHub License](https://img.shields.io/github/license/mudita/MuditaOS)]()

**Link** - [MuditaOS - Open Source E Ink mobile operating system | Mudita](https://mudita.com/products/phones/mudita-pure/muditaos/)  
**Features** - A mobile operating system built on [FreeRTOS](#freertos), optimized specifically for E-Ink displays.  

#### Key Points

---

## IoT-RTOS

### Contiki-NG

[![GitHub Repo stars](https://img.shields.io/github/stars/contiki-ng/contiki-ng)](https://github.com/contiki-ng/contiki-ng/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/contiki-ng/contiki-ng)](https://github.com/contiki-ng/contiki-ng/commits) | [![GitHub License](https://img.shields.io/github/license/contiki-ng/contiki-ng)]()

**Link** - [contiki-ng/contiki-ng: Contiki-NG: The OS for Next Generation IoT Devices](https://github.com/contiki-ng/contiki-ng)  
**Features** - A multitasking IoT operating system maintained by the authors of uIP and LwIP. It focuses on reliable, secure low-power communication and standard Internet protocols.  

#### Key Points

---

### Mbed OS

[![GitHub Repo stars](https://img.shields.io/github/stars/ARMmbed/mbed-os)](https://github.com/ARMmbed/mbed-os/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/ARMmbed/mbed-os)](https://github.com/ARMmbed/mbed-os/commits) | [![GitHub License](https://img.shields.io/github/license/ARMmbed/mbed-os)]()

**Link** - [Mbed OS | Mbed](https://os.mbed.com/mbed-os/)  
**Features** - An easy-to-use IoT operating system from ARM.  

#### Key Points

---

### Huawei LiteOS

[![Gitee Repo stars](https://gitee.com/LiteOS/LiteOS/badge/star.svg?theme=gvp)](https://gitee.com/LiteOS/LiteOS/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/LiteOS/LiteOS&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/LiteOS/LiteOS&query=$.license&label=license)]()

**Link** - [Huawei LiteOS: A lightweight operating system driving perception, connection, and intelligence for everything](https://gitee.com/LiteOS)  
**Features** - A lightweight IoT operating system from Huawei for the IoT domain.  

#### Key Points

---

### Xiaomi Vela

**Link** - [iot.mi.com/vela](https://iot.mi.com/vela)  
**Features** - An IoT operating system from Xiaomi, built on [NuttX](#nuttx). Kernel creation.  

#### Key Points

---

### AliOS Things

[![Gitee Repo stars](https://gitee.com/alios-things-admin/AliOS-Things/badge/star.svg?theme=gvp)](https://gitee.com/alios-things-admin/AliOS-Things/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/alios-things-admin/AliOS-Things&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/alios-things-admin/AliOS-Things&query=$.license&label=license)]()

**Link** - [AliOS Things: AliOS Things is an open-source project incubated and operated by the OpenAtom Foundation, and is a new-generation IoT operating system for developers.](https://gitee.com/alios-things)  
**Features** - A highly scalable IoT operating system from Alibaba for the IoT domain.  

#### Key Points

---

### TencentOS Tiny

[![Gitee Repo stars](https://gitee.com/Tencent/TencentOS-tiny/badge/star.svg?theme=gvp)](https://gitee.com/Tencent/TencentOS-tiny/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Tencent/TencentOS-tiny&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Tencent/TencentOS-tiny&query=$.license&label=license)]()

**Link** - [TencentOS-tiny: TencentOS tiny is a real-time operating system developed by Tencent for the IoT domain. It features low power consumption, low resource usage, modularity, safety, and reliability, and can effectively improve IoT terminal product development efficiency](https://gitee.com/Tencent/TencentOS-tiny)  
**Features** - A real-time operating system developed by Tencent for the IoT domain.  

#### Key Points

---

### OneOS

**Link** - [OneOS - China Mobile IoT Operating System](https://os.iot.10086.cn/)  
**Features** - A lightweight operating system introduced by China Mobile for the IoT domain, featuring configurability, cross-platform support, low power consumption, and high security. It supports mainstream chip architectures such as ARM Cortex-M/A, MIPS, and RISC-V; is compatible with standard interfaces such as POSIX and CMSIS; and supports JavaScript and MicroPython development.  

#### Key Points

---

### LuatOS

[![Gitee Repo stars](https://gitee.com/openLuat/LuatOS/badge/star.svg?theme=gvp)](https://gitee.com/openLuat/LuatOS/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/openLuat/LuatOS&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/openLuat/LuatOS&query=$.license&label=license)]()

**Link** - [LuatOS Documentation](https://wiki-zh.luatos.org)  
**Features** - A Lua script runtime framework for embedded systems, with the functional scope of an operating system.  

#### Key Points

- The MCUs currently supported are relatively limited;

---

### Lua-RTOS-ESP32

[![GitHub Repo stars](https://img.shields.io/github/stars/whitecatboard/Lua-RTOS-ESP32)](https://github.com/whitecatboard/Lua-RTOS-ESP32/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/whitecatboard/Lua-RTOS-ESP32)](https://github.com/whitecatboard/Lua-RTOS-ESP32/commits) | [![GitHub License](https://img.shields.io/github/license/whitecatboard/Lua-RTOS-ESP32)]()

**Link** - [whitecatboard/Lua-RTOS-ESP32: Lua RTOS for ESP32](https://github.com/whitecatboard/Lua-RTOS-ESP32)  
**Features** - A real-time operating system supporting a Lua interpreter, providing all Lua-required resources, basic modules, and middleware, and portable to other 32-bit platforms.  

#### Key Points

---

### Apache Mynewt OS

[![GitHub Repo stars](https://img.shields.io/github/stars/apache/mynewt-core)](https://github.com/apache/mynewt-core/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/apache/mynewt-core)](https://github.com/apache/mynewt-core/commits) | [![GitHub License](https://img.shields.io/github/license/apache/mynewt-core)]()

**Link** - [apache/mynewt-core: An OS to build, deploy and securely manage billions of devices](https://github.com/apache/mynewt-core)  
**Features** - An Apache OS designed for low-power wireless devices, with built-in Bluetooth and IEEE protocol stacks, ready to use out of the box.  

#### Key Points

---

### Mongoose OS

[![GitHub Repo stars](https://img.shields.io/github/stars/cesanta/mongoose-os)](https://github.com/cesanta/mongoose-os/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/cesanta/mongoose-os)](https://github.com/cesanta/mongoose-os/commits) | [![GitHub License](https://img.shields.io/github/license/cesanta/mongoose-os)]()

**Link** - [Mongoose OS - reduce IoT firmware development time up to 90%](https://mongoose-os.com/)  
**Features** - An IoT firmware development framework supporting C/JavaScript development, with good support for remote management and upgrades. The open-source edition has limited functionality.  

#### Key Points

---

### MicroPythonOS

[![GitHub Repo stars](https://img.shields.io/github/stars/MicroPythonOS/MicroPythonOS)](https://github.com/MicroPythonOS/MicroPythonOS/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/MicroPythonOS/MicroPythonOS)](https://github.com/MicroPythonOS/MicroPythonOS/commits) | [![GitHub License](https://img.shields.io/github/license/MicroPythonOS/MicroPythonOS)]()

**Link** - [MicroPythonOS - The Ultimate MicroPython Operating System](https://micropythonos.com/)  
**Features** - A lightweight, multifunctional operating system built with MicroPython, designed for microcontrollers such as ESP32 and desktop systems. It provides a modern Android-like touch interface, an app store, OTA, and more.  

#### Key Points

---

## ROS

### ROS

[![License: Apache 2.0](https://img.shields.io/badge/license-Apache%202.0-brightgreen.svg)](https://opensource.org/licenses/Apache-2.0)

**Link** - [ROS: Home](https://www.ros.org/)  
**Features** - A well-known open-source robot operating system in the industry that implements a complete set of software libraries and tools.  

#### Key Points

- This system was originally not deployed directly on MCUs, but on Linux; it now also supports microprocessors and Windows systems;

---

### AimRT

[![GitHub Repo stars](https://img.shields.io/github/stars/AimRT/AimRT)](https://github.com/AimRT/AimRT/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/AimRT/AimRT)](https://github.com/AimRT/AimRT/commits) | [![GitHub License](https://img.shields.io/github/license/AimRT/AimRT)]()

**Link** - [aimrt.org](https://aimrt.org/)  
**Features** - A runtime development framework built with Modern C++ for modern robotics. It provides comprehensive plugin development interfaces, is highly extensible, and compatible with other ROS ecosystems.  

#### Key Points

---
