# 异常快照与测试库

## Coredump

> Coredump又叫做核心转储，它是进程运行时在突然崩溃的那一刻的一个内存快照。操作系统在程序发生异常而异常在进程内部又没有被捕获的情况下，会把进程此刻内存、寄存器状态、运行堆栈等信息转储保存在一个文件里。

### CmBacktrace

**链接**：[armink/CmBacktrace: Advanced fault backtrace library for ARM Cortex-M series MCU | ARM Cortex-M 系列 MCU 错误追踪库 (github.com)](https://github.com/armink/CmBacktrace)
**特征**：针对 ARM Cortex-M 系列 MCU 的错误追踪库，目前几乎所有项目级代码都会添加的库。

#### 要点

- GCC似乎有原生支持类型的功能：[C，你的函数过程全被我看见了！](https://mp.weixin.qq.com/s/oaYbhBmfcg7IRUhZH2kgbQ)
- 对于难以复现的 bug，可将此库生产的 log 信息保存到 Flash 当中，然后再配合 addr2line 工具进行精确定位。
- 需要为该库生成的 log 信息分配一个独立的存储空间，该空间不能被其他程序使用，避免保存的 log 出现错误。

---


## 异常捕捉

### try

**链接**：[C 语言方式实现的 try catch 异常捕获 - 代码片段 - Gitee.com](https://gitee.com/Luyi365/codes/ea8h1g329prm05unxiqtv60)
**特征**：用 C 语言方式实现的 try catch 异常捕获。

#### 要点

---

### **CException**

**链接**：[CException — Throw The Switch](https://www.throwtheswitch.org/cexception)
**特征**：适用于C语言的简单异常处理，比标准库的更快，可以移植到任何支持 setjmp/longjmp 的平台上。

#### 要点

---

### MLA

**链接**：[skullboyer/MLA (github.com)](https://github.com/skullboyer/MLA)
**特征**：通过记录内存分配计数，来进行内存泄漏分析的库，小巧易用。

#### 要点

- 使用介绍：[【MLA】一种内存泄漏分析方法 - 壹点灵异 - 博客园 (cnblogs.com)](https://www.cnblogs.com/skullboyer/p/17982038)

---


## 测试

> 嵌入式领域详细测试介绍，包括代码测试和性能测试：[mollybuild/RISCV-Measurement: This is a repo for recording and reporting RISCV platform's test and measurement continuously. (github.com)](https://github.com/mollybuild/RISCV-Measurement)

### MTTEST

**链接**：[基于RTOS的注册机制代码测试框架 - 代码片段 - Gitee.com](https://gitee.com/Luyi365/codes/fhzm8d4wairyxnqlcup6059)
**特征**：基于RTOS的简易测试框架，采用注册机制。

#### 要点

- 使用介绍：[分享一个自己量产项目上的集成测试软件MTTEST-阿里云开发者社区](https://developer.aliyun.com/article/1325462)

---

### MinUnit

**链接**：[siu/minunit: Minimal unit testing framework for C (github.com)](https://github.com/siu/minunit)
**特征**：C 的最小单元测试框架，不使用内存分配。

#### 要点

- 只适用于Linux和PC端；

---

### CuTest

**链接**：[CuTest: The Cutest C Unit Testing Framework (sourceforge.net)](https://cutest.sourceforge.net/)
**特征**：极简的C单元测试框架，使用动态内存分配。

#### 要点

---

### cmockery

**链接**：[google/cmockery: A lightweight library to simplify and generalize the process of writing unit tests for C applications. (github.com)](https://github.com/google/cmockery)
**特征**：C 单元测试的轻量级框架，基于标准 C 库。

#### 要点

---

### EEMBC

**链接**：[Embedded Microprocessor Benchmark Consortium (eembc.org)](https://www.eembc.org/)
**特征**：EEMBC公司提供嵌入式领域众多测试库，主要测试芯片性能，属于业内标准，适合企业级项目部署。

#### 要点

- 提供ULPMark、CoreMark、IoTMark等测试库，具体介绍查看：[Benchmark Product List - EEMBC - Embedded Microprocessor Benchmark Consortium](https://www.eembc.org/products/)；
- CoreMark使用介绍：[手把手教你在MCU移植CoreMark跑分源码](https://mp.weixin.qq.com/s/1ylgA9fGmyW_vdDNW3AVIQ)

---

### Unity

**链接**：[Unity — Throw The Switch](https://www.throwtheswitch.org/unity)
**特征**：C 语言构建的单元测试框架，专注于使用嵌入式工具链。

#### 要点

- 参考：[ESP32 中的单元测试 - ESP32 - — ESP-IDF 编程指南 latest 文档 (espressif.com)](https://docs.espressif.com/projects/esp-idf/zh_CN/latest/esp32/api-guides/unit-tests.html)

---

### greatest

**链接**：[silentbicycle/greatest: A C testing library in 1 file. No dependencies, no dynamic allocation. ISC licensed. (github.com)](https://github.com/silentbicycle/greatest)
**特征**：小巧的C语言测试系统，使用插桩/覆盖测试，但可以与其他程序一起运行。

#### 要点

- 使用介绍：[C Testing for Embedded Applications with greatest (atomicobject.com)](https://spin.atomicobject.com/greatest-c-testing-embedded/)

---

### Catch2

**链接**：[catchorg/Catch2: A modern, C++-native, test framework for unit-tests, TDD and BDD - using C++14, C++17 and later (C++11 support is in v2.x branch, and C++03 on the Catch1.x branch)](https://github.com/catchorg/Catch2)
**特征**：一个流行的 C++ 单元测试框架，仅一个头文件，它的设计目标是轻量、易用且无依赖。

#### 要点

---