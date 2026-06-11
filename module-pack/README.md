# 模块集合包

> 大多数模块集合包包含了各种各样的功能，无法对其进行子类划分，就都甩在这里了。

### ToolKit

**链接**：[cproape/toolkit: ToolKit 是一套应用于嵌入式系统的通用工具包，目前为止工具包包含：循环队列、软件定时器、事件集 (github.com)](https://github.com/cproape/toolkit)  
**特征**：一个小功能的嵌入式工具包，提供循环队列、软件定时器、事件集三个功能，文档写的很清楚。  

#### 要点

- 模块可以选择使用静态或动态内存。

---

### lwUTIL

**链接**：[MaJerle/lwutil: Versatile and easy to use C language utility library with functions and macros commonly used in various applications (github.com)](https://github.com/MaJerle/lwutil)  
**特征**：实用工具包，包含值运算、大小端存储、位运算、ascii 转化等。  

#### 要点

---

### sc

**链接**：[tezc/sc: Common libraries and data structures for C. (github.com)](https://github.com/tezc/sc)  
**特征**：高性能且小内存占用的独立工具包，主要提供数据结构的相关功能。  

#### 要点

---

### cotUtils

**链接**：[cotUtils: C 语言常用工具类，包括了各类容器（队列、链表、动态数组等）、移植了 C++ boost 库的 preprocessor 库（宏编程）等 (gitee.com)](https://gitee.com/cot_package/cot_utils)  
**特征**：C 语言的通用扩展库，包括多种容器（队列、栈、双向链表、动态数组），序列化/反序列化的结构体，PP 库（多功能宏）等功能。  

#### 要点

- 使用介绍：[C 语言扩展库 + 结构体序列化](https://mp.weixin.qq.com/s/X9OkwsTqCCfvN7D62Wv02A)

---

### mr-library

**链接**：[MacRsh/mr-library - 码云 - 开源中国 (gitee.com)](https://gitee.com/MacRsh/mr-library)  
**特征**：嵌入式轻量级框架，提供标准化的驱动接口和简单的内核功能组件等。  

#### 要点

- 使用介绍：[一个面向嵌入式系统的轻量级框架！ (qq.com)](https://mp.weixin.qq.com/s/NwOgiCFkIlwgkIqK6_n_vg)

---

### Zorb Framework

**链接**：[54zorb/Zorb-Framework: 一个轻量级嵌入式框架 (github.com)](https://github.com/54zorb/Zorb-Framework)  
**特征**：轻量级的嵌入式框架，包含基本的内核功能，都是单独集成，方便裁剪使用。  

#### 要点

- 使用介绍：[嵌入式框架 | 搭建调试输出、建立时间系统 (qq.com)](https://mp.weixin.qq.com/s/xotrxGumAE-igqtomA_lfw)
- 环形缓冲区功能介绍：[嵌入式框架 | 环形缓冲区的实现 (qq.com)](https://mp.weixin.qq.com/s/6nQjsxiB20p3xFca3f-jFw)
- 函数式状态机功能介绍：[嵌入式框架 | 状态机的实现 (qq.com)](https://mp.weixin.qq.com/s/bgwvDfTEYN2W2tWi0z6eyA)

---

### Gear-Lib

**链接**：[gozfree/gear-lib: Gear-Lib, C library for IOT Embedded Multimedia and Network (github.com)](https://github.com/gozfree/gear-lib/tree/master)  
**特征**：一组通用的 Ｃ 基础库，全部用 POSIX C 实现，旨在兼容 linux, windows, android, ios 等跨平台，包括数据结构、异步、I/O、状态机、动态加载等功能。  

#### 要点

---

### c-algorithms

**链接**：[C Algorithms (fragglet.github.io)](https://fragglet.github.io/c-algorithms/)  
**特征**：提供常用算法和数据结构的集合来弥补标准库的缺失，并且比 C 标准库编译出来的小得多。  

#### 要点

---

### klib

**链接**：[Klib — a generic library in C (attractivechaos.github.io)](https://attractivechaos.github.io/klib/#About)  
**特征**：一个独立的轻量级 C 库，提供多种基础算法、数据结构和解析器等功能。  

#### 要点

---

### AMetal

**链接**：[ametal: AMetal 是芯片级的裸机软件包，定义了跨平台的通用接口（使得基于 AMetal 的应用程序可以和具体硬件完全分离,实现跨平台复用），并提供了一系列驱动及常用的软件服务。 (gitee.com)](https://gitee.com/zlgmcuopen/ametal)  
**特征**：软件包比较冗余，核心思想就是分为三层，即硬件层、驱动层（抽象层）和标准接口层。提供多个平台的通用接口，采用服务式框架搭建，将运行效率放在第一位。  

#### 要点

- 移植的话主要用两个文件夹，即 components 和 interface；
- 硬件层（位于 soc）：对于不同型号的芯片需要自行编写寄存器操作；
- 驱动层（抽象层）（位于 components）：集合硬件层的操作，直接拿来用即可；
- 标准接口层（位于 interface）：对应用层的接口，直接拿来用即可；
- 使用介绍：[嵌入式大杂烩周记 | 第 8 期](https://mp.weixin.qq.com/s/Hor8QJ_8nNFOBFZ3JCTyqw)

---

### eLab

**链接**：[elab: eLab 是集成了多种技术和特性的嵌入式开发平台。 (gitee.com)](https://gitee.com/event-os/elab)  
**特征**：综合开发平台，包含嵌入式所需大部分功能包，尤其注重跨平台开发和 PC 仿真。  

#### 要点

---

### TheAlgorithms

**链接**：[The Algorithms (github.com)](https://github.com/TheAlgorithms/)  
**特征**：开源组织 TheAlgorithms 维护的各种基础算法、数据结构、机器学习等库，内容十分丰富，且包含各个流行语言的版本。  

#### 要点

- C/C++ 库基于 C11 标志编写，不依赖其他外部库，因此可以方便用于嵌入式领域。

---

### simpostOS

**链接**：[simpostOS: 极简应用系统 (gitee.com)](https://gitee.com/simpost/simpostOS)  
**特征**：是一套设计方法，以及多个软件组件、服务的集合。其理念是将所有功能模块化，并极大地增加功能复用性。使用的是纯 C++ 语言，库写的十分现代化，对新手使用不友好。  

#### 要点

- 目前全网几乎都找不到相关例程，库里面所包含的组件说明只能看简介：[docs/1-introduce.md · 极简美/simpostOS - Gitee.com](https://gitee.com/simpost/simpostOS/blob/master/docs/1-introduce.md)

---

### PetiteDrv

**链接**：[wujique/PetiteDrv: a petite driver base on mcu such as stm32(f103/f407/h750), RT1052 (github.com)](https://github.com/wujique/PetiteDrv)  
**特征**：通用的 SDK 库，其思想是层层抽象，在不使用复杂的代码完成解耦功能，适合小公司小项目的开发。  

#### 要点

---

### varch

**链接**：[Lamdonn/varch - 码云 - 开源中国 (gitee.com)](https://gitee.com/Lamdonn/varch)  
**特征**：是嵌入式 C 语言常用代码模块库，包含了嵌入式中常用的算法库、数据结构（容器）库,、解析器库、独立 C 语言 std 库、工具库等等，每个库独立使用，简单高效。  

#### 要点

---

### ctool

**链接**：[ctool: 常用的 C 语言工具 (gitee.com)](https://gitee.com/Lamdonn/ctool)  
**特征**：常用但一般库里并不包含的工具，包括不定参数、日期、内存测试等。  

#### 要点

---

### Generic\_MCU\_Software\_Infrastructure

**链接**：[GorgonMeducer/Generic_MCU_Software_Infrastructure: Provide necessary software infrastructure, service, macros to support some high level abstract concept or paradigm, such as OOPC, FSM, delegate (event-driven) and etc](https://github.com/GorgonMeducer/Generic_MCU_Software_Infrastructure)  
**特征**：提供必要的软件基础设施、服务、宏来支持一些高级的抽象概念和范式。  

#### 要点

---

### appkit

**链接**：[appkit: appkit 是一个基于嵌入式 Linux 的具有可移植性的 C++ 程序开发框架，其目的是为了加快 LInux 应用程序的开发速度，解放程序员的大脑和双手，让大家把精力投入到更有意义的事情当中去。](https://gitee.com/newgolo/appkit)  
**特征**：基于 C++ 的 Linux 应用开发库，包括开发中常用的模块功能（线程管理、定时器、文件 IO、串口通信等）。  

#### 要点

- 使用介绍：[一个面向嵌入式 Linux C++ 的应用开发框架!](https://mp.weixin.qq.com/s/0TZ9G2G0aTZKkdmOIefcfw)

---