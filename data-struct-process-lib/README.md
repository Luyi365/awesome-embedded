# 数据结构与数据处理库

## 流

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

---

### xprintf

[![License: xprintf](https://img.shields.io/badge/License-xprintf-blue.svg)]()

**链接**：[ELM - Embedded String Functions](http://elm-chan.org/fsw/strf/xprintf.html)  
**特征**：嵌入式字符串函数，代替不足以实现常规 printf 功能，可以动态的将字符串写入不同外设。  

#### 要点

---

### CMSIS-Stream

[![GitHub Repo stars](https://img.shields.io/github/stars/ARM-software/CMSIS-Stream)](https://github.com/ARM-software/CMSIS-Stream/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/ARM-software/CMSIS-Stream)](https://github.com/ARM-software/CMSIS-Stream/commits) | [![GitHub License](https://img.shields.io/github/license/ARM-software/CMSIS-Stream)]()

**链接**：[ARM-software/CMSIS-Stream: CMSIS-Stream software component](https://github.com/ARM-software/CMSIS-Stream)  
**特征**：ARM 官方出品的数据流处理组件，提供图形表示，需要 Python 和 C++ 联合完成。  

#### 要点

- 由 Python 根据配置生成 C++ 代码；

---

## 数据结构

### CBUF

[![GitHub Repo stars](https://img.shields.io/github/stars/barraq/BRBrain)](https://github.com/barraq/BRBrain/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/barraq/BRBrain?path=firmware/CBUF.h)](https://github.com/barraq/BRBrain/commits) | [![GitHub License](https://img.shields.io/github/license/barraq/BRBrain)]()

**链接**：[BRBrain/firmware/CBUF.h at master · barraq/BRBrain · GitHub](https://github.com/barraq/BRBrain/blob/master/firmware/CBUF.h)  
**特征**：极优雅的宏实现环形缓冲区，功能简单易用。  

#### 要点

- 用的是 C++ 的类，需要创建一个类的实体（句柄），来充当对象。

---

### sys/queue

**链接**：[queue.h source code \[glibc/misc/sys/queue.h\] - Codebrowser](https://codebrowser.dev/glibc/glibc/misc/sys/queue.h.html)  
**特征**：Linux、FreeBSD 中使用的队列、链表头文件，全部用宏来实现的，且能够链接任意类型，如结构体等。  

#### 要点

- 使用介绍：[嵌入式大杂烩周记 | 第 3 期](https://mp.weixin.qq.com/s/nDTkTw0RH-6pTjJWelrEfg)
- 会用到`typeof()`运算符，因此需要C23或GNU编译的支持。在嵌入式编译套件的使用中把编译器修改为gnu即可；

---

### byte\_queue

[![Gitee Repo stars](https://gitee.com/Aladdin-Wang/byte_queue/badge/star.svg?theme=gvp)](https://gitee.com/Aladdin-Wang/byte_queue/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Aladdin-Wang/byte_queue&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Aladdin-Wang/byte_queue&query=$.license&label=license)]()

**链接**：[byte_queue: 一个C语言编写的支持任意类型的环形队列](https://gitee.com/Aladdin-Wang/byte_queue)  
**特征**：C语言编写的支持任意类型的环形队列，带宏包装，使用简单。  

#### 要点

---

### queue

[![Gitee Repo stars](https://gitee.com/Lamdonn/queue/badge/star.svg?theme=gvp)](https://gitee.com/Lamdonn/queue/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Lamdonn/queue&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Lamdonn/queue&query=$.license&label=license)]()

**链接**：[queue: Very small and convenient general-purpose queue in C language version. C语言版本的非常小且方便的通用队列。](https://gitee.com/Lamdonn/queue)  
**特征**：C语言通用队列，支持任意数据类型，使用简单高效。  

#### 要点

---

### Ring-Buffer

[![GitHub Repo stars](https://img.shields.io/github/stars/AndersKaloer/Ring-Buffer)](https://github.com/AndersKaloer/Ring-Buffer/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/AndersKaloer/Ring-Buffer)](https://github.com/AndersKaloer/Ring-Buffer/commits) | [![GitHub License](https://img.shields.io/github/license/AndersKaloer/Ring-Buffer)]()

**链接**：[AndersKaloer/Ring-Buffer: A simple ring buffer (circular buffer) designed for embedded systems.](https://github.com/AndersKaloer/Ring-Buffer)  
**特征**：简单高效的环形缓冲库，功能简单易用。  

#### 要点

- 内存缓冲区的大小必须是 2 的幂；
- 环形缓冲区最多可以包含字节：(buf_size - 1)；

---

### wl\_queue

[![GitHub Repo stars](https://img.shields.io/github/stars/Aladdin-Wang/wl_queue)](https://github.com/Aladdin-Wang/wl_queue/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/Aladdin-Wang/wl_queue)](https://github.com/Aladdin-Wang/wl_queue/commits) | [![GitHub License](https://img.shields.io/github/license/Aladdin-Wang/wl_queue)]()

**链接**：[Aladdin-Wang/wl_queue: 一款支持任意类似的队列](https://github.com/Aladdin-Wang/wl_queue)  
**特征**：支持任意数据类型的环形队列，运用了C重载的技巧，注重纤程安全。  

#### 要点

- 代码使用了`typeof()`函数进行类型判断，该函数并不是C标准函数，只被特定编译器扩展支持；

---

### RingBuffer

[![GitHub Repo stars](https://img.shields.io/github/stars/XinLiGH/RingBuffer)](https://github.com/XinLiGH/RingBuffer/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/XinLiGH/RingBuffer)](https://github.com/XinLiGH/RingBuffer/commits) | [![GitHub License](https://img.shields.io/github/license/XinLiGH/RingBuffer)]()

**链接**：[XinLiGH/RingBuffer: 模仿 kfifo 实现的环形缓冲区](https://github.com/XinLiGH/RingBuffer)  
**特征**：实用的环形缓冲库，功能完整，使用的是堆内存分配。  

#### 要点

- 使用介绍：[一个环形缓冲区的实现](https://mp.weixin.qq.com/s/BORniHooGGcoPasFYhY2Xg)

---

### queue

[![Gitee Repo stars](https://gitee.com/const-zpc/queue/badge/star.svg?theme=gvp)](https://gitee.com/const-zpc/queue/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/const-zpc/queue&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/const-zpc/queue&query=$.license&label=license)]()

**链接**：[queue: 基于 C 语言实现的队列功能，扩展性强，同时支持零拷贝读写队列（适用于大内存的单个元素，可以有效减少函数耗时）](https://gitee.com/const-zpc/queue)  
**特征**：简单的队列功能库，扩展性强，同时支持零拷贝读写队列（适用于大内存的单个元素，可以有效减少函数耗时）。  

#### 要点

---

### QueueForMcu

[![GitHub Repo stars](https://img.shields.io/github/stars/xiaoxinpro/QueueForMcu)](https://github.com/xiaoxinpro/QueueForMcu/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/xiaoxinpro/QueueForMcu)](https://github.com/xiaoxinpro/QueueForMcu/commits) | [![GitHub License](https://img.shields.io/github/license/xiaoxinpro/QueueForMcu)]()

**链接**：[xiaoxinpro/QueueForMcu: 基于单片机实现的队列功能模块，主要用于 8 位、16 位、32 位非运行 RTOS 的单片机应用，兼容大多数单片机平台。](https://github.com/xiaoxinpro/QueueForMcu)  
**特征**：队列功能模块，适用于非 RTOS 系统，动态创建队列对象和缓冲区。  

#### 要点

- 使用介绍：[QueueForMcu | 用于单片机的队列功能模块](https://mp.weixin.qq.com/s/JehE4zq4eKVbRghE5smHcg)

---

### ConcurrentQueue

[![GitHub Repo stars](https://img.shields.io/github/stars/cameron314/concurrentqueue)](https://github.com/cameron314/concurrentqueue/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/cameron314/concurrentqueue)](https://github.com/cameron314/concurrentqueue/commits) | [![GitHub License](https://img.shields.io/github/license/cameron314/concurrentqueue)]()

**链接**：[cameron314/concurrentqueue: A fast multi-producer, multi-consumer lock-free concurrent queue for C++11](https://github.com/cameron314/concurrentqueue)  
**特征**：基于C++的工业级无锁队列，无需锁也极其注重线程安全。  

#### 要点

---

### uthash

[![GitHub Repo stars](https://img.shields.io/github/stars/troydhanson/uthash)](https://github.com/troydhanson/uthash/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/troydhanson/uthash)](https://github.com/troydhanson/uthash/commits) | [![GitHub License](https://img.shields.io/github/license/troydhanson/uthash)]()

**链接**：[troydhanson/uthash: C macros for hash tables and more](https://github.com/troydhanson/uthash)  
**特征**：提供哈希、列表、环形等数据结构库，只用包含头文件即可使用。  

#### 要点

---

### LwRB

[![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwrb)](https://github.com/MaJerle/lwrb/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwrb)](https://github.com/MaJerle/lwrb/commits) | [![GitHub License](https://img.shields.io/github/license/MaJerle/lwrb)]()

**链接**：[LwRB latest-develop documentation — LwRB documentation](https://docs.majerle.eu/projects/lwrb/en/latest/)  
**特征**：专业的 FIFO 环形缓冲库，无动态内存分配，适用于 MDA 传输，注重线程和中断安全。  

#### 要点

- 使用介绍：[适用于嵌入式的轻量级环缓冲区管理库！](https://mp.weixin.qq.com/s/jmgYYWlX-mkhAoL2-MRLFw)
- 回调函数是处理 `lwrb_evt_type_t` 里各个事件的。

---

### fifofast

[![GitHub Repo stars](https://img.shields.io/github/stars/nqtronix/fifofast)](https://github.com/nqtronix/fifofast/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/nqtronix/fifofast)](https://github.com/nqtronix/fifofast/commits) | [![GitHub License](https://img.shields.io/github/license/nqtronix/fifofast)]()

**链接**：[nqtronix/fifofast: A fast, generic fifo for MCUs.](https://github.com/nqtronix/fifofast)  
**特征**：针对MCU优化的FIFO库，旨在尽可能减少CPU和SRAM的消耗。  

#### 要点

---

## 数据库

### cotParam

[![Gitee Repo stars](https://gitee.com/cot_package/cot_param/badge/star.svg?theme=gvp)](https://gitee.com/cot_package/cot_param/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/cot_package/cot_param&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/cot_package/cot_param&query=$.license&label=license)]()

**链接**：[cotParam: 轻量级参数管理框架(C 语言)](https://gitee.com/cot_package/cot_param)  
**特征**：采用表驱动方式进行参数管理，包括缺省值、最小值和最大值等。  

#### 要点

- 和普通变量赋值最大的区别目前来看有两点：
  - 可以键值配对；
  - 给参数定范围，一旦不符合范围即赋为规定的值；
- 使用介绍：[C 语言参数管理代码框架-重大更新](https://mp.weixin.qq.com/s/Q0ROGgkxjDGXyKAxnu-aHQ)

---

### EasyFlash

[![Gitee Repo stars](https://gitee.com/Armink/EasyFlash/badge/star.svg?theme=gvp)](https://gitee.com/Armink/EasyFlash/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Armink/EasyFlash&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Armink/EasyFlash&query=$.license&label=license)]()

**链接**：[EasyFlash: 轻量级物联网设备信息存储方案，让 Flash 成为小型 KV 数据库。 全新一代版本请移步至 https://gitee.com/armink/FlashDB](https://gitee.com/Armink/EasyFlash)  
**特征**：Key-Value 型简易数据库，主要提供：变量的 KV 配对，IAP 数据修改（可用于升级），log 存储等功能。  

#### 要点

- log 的存储需要用到旗下的：[EasyLogger](../log-term-lib/README.md#easylogger) ；

---

### FlashDB

[![Gitee Repo stars](https://gitee.com/Armink/FlashDB/badge/star.svg?theme=gvp)](https://gitee.com/Armink/FlashDB/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Armink/FlashDB&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Armink/FlashDB&query=$.license&label=license)]()

**链接**：[FlashDB: 一款支持 KV 数据和时序数据的超轻量级数据库](https://gitee.com/Armink/FlashDB)  
**特征**：提供 KV 和 TS 两种数据库，比起 [EasyFlash](#easyflash) 更专注于数据库本身，而不提供过多的额外功能。  

#### 要点

- ~~介绍：FlashDB；~~（待发布）
- 使用该库可以用来解决 Flash 地址内数据在设备迭代升级时被移动的问题，因为使用的是键值映射；

---

### Nanopb

[![GitHub Repo stars](https://img.shields.io/github/stars/nanopb/nanopb)](https://github.com/nanopb/nanopb/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/nanopb/nanopb)](https://github.com/nanopb/nanopb/commits) | [![GitHub License](https://img.shields.io/github/license/nanopb/nanopb)]()

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

[![GitHub Repo stars](https://img.shields.io/github/stars/haifenghuang/linq4c)](https://github.com/haifenghuang/linq4c/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/haifenghuang/linq4c)](https://github.com/haifenghuang/linq4c/commits) | [![GitHub License](https://img.shields.io/github/license/haifenghuang/linq4c)]()

**链接**：[haifenghuang/linq4c: LINQ for C(GroupBy, GroupJoin, Join, Take, Where, Select, etc)](https://github.com/haifenghuang/linq4c)  
**特征**：在 C 语言里实现了 C# 的 linq 方法。  

#### 要点

- 什么是 LINQ？将代码中的数据集合成一个数据库，给定其标签，并用类似于 SQL 的查询语法来操作该集合，能够以一种更直观、更简洁的方式来查询和处理数据。

---

### SQLite

[![License: SQLite](https://img.shields.io/badge/license-SQLite-blue.svg)]()

**链接**：[SQLite Home Page](https://www.sqlite.org/)  
**特征**：业界用的最多的嵌入式标准的数据库，使用 SQL 语法，可使用磁盘文件。  

#### 要点

- ~~详细解释可参见：SQLite（MySQL）；~~（待发布）

---

## 压缩库

### lz4

[![GitHub Repo stars](https://img.shields.io/github/stars/lz4/lz4)](https://github.com/lz4/lz4/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/lz4/lz4)](https://github.com/lz4/lz4/commits) | [![GitHub License](https://img.shields.io/github/license/lz4/lz4)]()

**链接**：[LZ4 - Extremely fast compression](https://lz4.org/)  
**特征**：极快的无损压缩算法库，适合通信时的数据压缩。  

#### 要点

---

### heatshrink

[![GitHub Repo stars](https://img.shields.io/github/stars/atomicobject/heatshrink)](https://github.com/atomicobject/heatshrink/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/atomicobject/heatshrink)](https://github.com/atomicobject/heatshrink/commits) | [![GitHub License](https://img.shields.io/github/license/atomicobject/heatshrink)]()

**链接**：[atomicobject/heatshrink: data compression library for embedded/real-time systems](https://github.com/atomicobject/heatshrink)  
**特征**：超低资源消耗的嵌入式解压缩库。相关文档较少。  

#### 要点

- 目前还不清楚是否能和文件系统联动，能够解压 PC 上的压缩包；

---

### TJpgDec

[![License: TJpgDec](https://img.shields.io/badge/License-TJpgDec-blue.svg)]()

**链接**：[TJpgDec - Tiny JPEG Decompressor](http://elm-chan.org/fsw/tjpgd/00index.html)  
**特征**：针对嵌入式系统优化的 JPEG 图像解压缩模块。  

#### 要点

- 支持像素格式：RGB888、RGB565 或灰度；

---
