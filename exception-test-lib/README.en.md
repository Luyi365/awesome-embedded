# Exception Snapshot and Testing Libraries
<!-- i18n:language-selector:start -->
[中文](README.md) | **English**
<!-- i18n:language-selector:end -->

## Coredump

> A coredump, also called a core dump, is a memory snapshot taken when a process suddenly crashes. When an exception occurs and is not caught within the process, the operating system dumps the process memory, register state, call stack, and other information to a file.

### CmBacktrace

[![GitHub Repo stars](https://img.shields.io/github/stars/armink/CmBacktrace)](https://github.com/armink/CmBacktrace/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/armink/CmBacktrace)](https://github.com/armink/CmBacktrace/commits) | [![GitHub License](https://img.shields.io/github/license/armink/CmBacktrace)]()

**Link** - [armink/CmBacktrace: Advanced fault backtrace library for ARM Cortex-M series MCU | Error tracing library for ARM Cortex-M series MCU](https://github.com/armink/CmBacktrace)  
**Features** - An error tracing library for ARM Cortex-M series MCU, now included in nearly all project-level codebases.  

#### Key Points

- GCC appears to provide native support for this: [C, I Can See All Your Function Calls!](https://mp.weixin.qq.com/s/oaYbhBmfcg7IRUhZH2kgbQ)
- For bugs that are difficult to reproduce, save the log produced by this library to Flash, then use addr2line for precise location.
- Allocate a dedicated storage area for the log produced by this library. No other program may use this area, preventing saved log errors.

---

## Exception Handling

### try

**Link** - [try-catch exception handling implemented in C - Code snippet - Gitee.com](https://gitee.com/Luyi365/codes/ea8h1g329prm05unxiqtv60)  
**Features** - try-catch exception handling implemented in C.  

#### Key Points

---

### CException

[![GitHub Repo stars](https://img.shields.io/github/stars/ThrowTheSwitch/CException)](https://github.com/ThrowTheSwitch/CException/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/ThrowTheSwitch/CException)](https://github.com/ThrowTheSwitch/CException/commits) | [![GitHub License](https://img.shields.io/github/license/ThrowTheSwitch/CException)]()

**Link** - [CException — Throw The Switch](https://www.throwtheswitch.org/cexception)  
**Features** - Simple exception handling for C, faster than the standard library and portable to any platform supporting setjmp/longjmp.  

#### Key Points

---

### MLA

[![GitHub Repo stars](https://img.shields.io/github/stars/skullboyer/MLA)](https://github.com/skullboyer/MLA/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/skullboyer/MLA)](https://github.com/skullboyer/MLA/commits) | [![GitHub License](https://img.shields.io/github/license/skullboyer/MLA)]()

**Link** - [skullboyer/MLA](https://github.com/skullboyer/MLA)  
**Features** - A small, easy-to-use memory leak analysis library that records allocation counts.  

#### Key Points

- Introduction: [MLA: A Memory Leak Analysis Method - Yidianlingyi - Blog Park](https://www.cnblogs.com/skullboyer/p/17982038)

---

## Testing

> A detailed introduction to testing in the embedded field, including code testing and performance testing: [mollybuild/RISCV-Measurement: This is a repo for recording and reporting RISCV platform's test and measurement continuously.](https://github.com/mollybuild/RISCV-Measurement)

### MTTEST

**Link** - [RTOS-based test framework using a registration mechanism - Code snippet - Gitee.com](https://gitee.com/Luyi365/codes/fhzm8d4wairyxnqlcup6059)  
**Features** - A simple RTOS-based testing framework using a registration mechanism.  

#### Key Points

- Introduction: [Sharing Integrated Test Software MTTEST from My Mass-production Project - Alibaba Cloud Developer Community](https://developer.aliyun.com/article/1325462)

---

### MinUnit

[![GitHub Repo stars](https://img.shields.io/github/stars/siu/minunit)](https://github.com/siu/minunit/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/siu/minunit)](https://github.com/siu/minunit/commits) | [![GitHub License](https://img.shields.io/github/license/siu/minunit)]()

**Link** - [siu/minunit: Minimal unit testing framework for C](https://github.com/siu/minunit)  
**Features** - A minimal unit testing framework for C without memory allocation.  

#### Key Points

- Only suitable for Linux and PCs;

---

### CuTest

[![License: CuTest](https://img.shields.io/badge/License-CuTest-blue.svg)]()

**Link** - [CuTest: The Cutest C Unit Testing Framework](https://cutest.sourceforge.net/)  
**Features** - A minimalist C unit testing framework using dynamic memory allocation.  

#### Key Points

---

### cmockery

[![GitHub Repo stars](https://img.shields.io/github/stars/google/cmockery)](https://github.com/google/cmockery/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/google/cmockery)](https://github.com/google/cmockery/commits) | [![GitHub License](https://img.shields.io/github/license/google/cmockery)]()

**Link** - [google/cmockery: A lightweight library to simplify and generalize the process of writing unit tests for C applications.](https://github.com/google/cmockery)  
**Features** - A lightweight C unit testing framework based on the standard C library.  

#### Key Points

---

### EEMBC

**Link** - [Embedded Microprocessor Benchmark Consortium](https://www.eembc.org/)  
**Features** - EEMBC provides many testing libraries for embedded applications, mainly for chip performance testing. It is an industry standard suitable for enterprise projects.  

#### Key Points

- Provides test suites such as ULPMark, CoreMark, and IoTMark. See: [Benchmark Product List - EEMBC - Embedded Microprocessor Benchmark Consortium](https://www.eembc.org/products/);
- CoreMark introduction: [A Step-by-step Guide to Porting and Benchmarking CoreMark on an MCU](https://mp.weixin.qq.com/s/1ylgA9fGmyW_vdDNW3AVIQ)

---

### Unity

[![GitHub Repo stars](https://img.shields.io/github/stars/ThrowTheSwitch/Unity)](https://github.com/ThrowTheSwitch/Unity/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/ThrowTheSwitch/Unity)](https://github.com/ThrowTheSwitch/Unity/commits) | [![GitHub License](https://img.shields.io/github/license/ThrowTheSwitch/Unity)]()

**Link** - [Unity — Throw The Switch](https://www.throwtheswitch.org/unity)  
**Features** - A unit testing framework written in C and focused on embedded toolchains.  

#### Key Points

- Reference: [Unit Testing in ESP32 - ESP32 - ESP-IDF Programming Guide latest documentation](https://docs.espressif.com/projects/esp-idf/zh_CN/latest/esp32/api-guides/unit-tests.html)

---

### greatest

[![GitHub Repo stars](https://img.shields.io/github/stars/silentbicycle/greatest)](https://github.com/silentbicycle/greatest/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/silentbicycle/greatest)](https://github.com/silentbicycle/greatest/commits) | [![GitHub License](https://img.shields.io/github/license/silentbicycle/greatest)]()

**Link** - [silentbicycle/greatest: A C testing library in 1 file. No dependencies, no dynamic allocation. ISC licensed.](https://github.com/silentbicycle/greatest)  
**Features** - A compact C testing system that uses instrumentation/coverage testing and can run with other programs.  

#### Key Points

- Introduction: [C Testing for Embedded Applications with greatest](https://spin.atomicobject.com/greatest-c-testing-embedded/)

---

### Catch2

[![GitHub Repo stars](https://img.shields.io/github/stars/catchorg/Catch2)](https://github.com/catchorg/Catch2/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/catchorg/Catch2)](https://github.com/catchorg/Catch2/commits) | [![GitHub License](https://img.shields.io/github/license/catchorg/Catch2)]()

**Link** - [catchorg/Catch2: A modern, C++-native, test framework for unit-tests, TDD and BDD - using C++14, C++17 and later (C++11 support is in v2.x branch, and C++03 on the Catch1.x branch)](https://github.com/catchorg/Catch2)  
**Features** - A popular C++ unit testing framework with only one header file, designed to be lightweight, easy to use, and dependency-free.  

#### Key Points

---
