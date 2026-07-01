# 引擎（仿真）库

> 引擎库就是在嵌入式里使其支持本不支持的编程语言。

## SoftFP

### <a name="softfp-project"></a>softfp

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)

**链接**：[SoftFP Library](https://bellard.org/softfp/)  
**特征**：用于没有硬件浮点单元（FPU）的情况下，作为软件浮点运算的实现方式。  

#### 要点

---

## C++

### sds

[![GitHub Repo stars](https://img.shields.io/github/stars/antirez/sds)](https://github.com/antirez/sds/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/antirez/sds)](https://github.com/antirez/sds/commits) | [![GitHub License](https://img.shields.io/github/license/antirez/sds)]()

**链接**：[antirez/sds: Simple Dynamic Strings library for C](https://github.com/antirez/sds)  
**特征**：简单动态字符串库，使用堆内存，其作用就是在 C 语言中仿照 C++ 的 string 类型。  

#### 要点

- 使用介绍：[嵌入式大杂烩周记 | 第 15 期](https://mp.weixin.qq.com/s/C77TNpvKvj__ExUEXf4MhA)

---

### STR

[![GitHub Repo stars](https://img.shields.io/github/stars/mickjc750/str)](https://github.com/mickjc750/str/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/mickjc750/str)](https://github.com/mickjc750/str/commits) | [![GitHub License](https://img.shields.io/github/license/mickjc750/str)]()

**链接**：[mickjc750/str: C String handling library inspired by Luca Sas](https://github.com/mickjc750/str)  
**特征**：更高级的字符串处理库，拥有字符串分割/修剪/搜索/查错等功能。  

#### 要点

---

### etl

[![GitHub Repo stars](https://img.shields.io/github/stars/ETLCPP/etl)](https://github.com/ETLCPP/etl/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/ETLCPP/etl)](https://github.com/ETLCPP/etl/commits) | [![GitHub License](https://img.shields.io/github/license/ETLCPP/etl)]()

**链接**：[ETLCPP/etl: Embedded Template Library](https://github.com/ETLCPP/etl)  
**特征**：适用于嵌入式的 C++ 模板库。  

#### 要点

---

### LW_OOPC

[![GitHub Repo stars](https://img.shields.io/github/stars/Akagi201/lw_oopc)](https://github.com/Akagi201/lw_oopc/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/Akagi201/lw_oopc)](https://github.com/Akagi201/lw_oopc/commits) | [![GitHub License](https://img.shields.io/github/license/Akagi201/lw_oopc)]()

**链接**：[Akagi201/lw_oopc: modified from http://sourceforge.net/projects/lwoopc/](https://github.com/Akagi201/lw_oopc)  
**特征**：适合嵌入式的面向对象的编程扩展，在源码的基础上进行了多个版本的更新优化，简单易用。  

#### 要点

---

### PLOOC

[![GitHub Repo stars](https://img.shields.io/github/stars/GorgonMeducer/PLOOC)](https://github.com/GorgonMeducer/PLOOC/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/GorgonMeducer/PLOOC)](https://github.com/GorgonMeducer/PLOOC/commits) | [![GitHub License](https://img.shields.io/github/license/GorgonMeducer/PLOOC)]()

**链接**：[GorgonMeducer/PLOOC: Protected Low-overhead Object Oriented Programming with ANSI-C](https://github.com/GorgonMeducer/PLOOC)  
**特征**：在 C 语言中提供面向对象的编程扩展，可以实现私有成员、继承、重载等功能。  

#### 要点

- 使用介绍：
  1. [真刀真枪模块化（2.5）—— 君子协定](https://mp.weixin.qq.com/s/4-cojkgnghB4TtaeEo63bQ)
  2. [防御性编程（X）OOPC 开发（√）](https://mp.weixin.qq.com/s/enf5sTF1eWpBf0QjiVLdLw)

---

### vlib

[![Gitee Repo stars](https://gitee.com/Lamdonn/vlib/badge/star.svg?theme=gvp)](https://gitee.com/Lamdonn/vlib/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Lamdonn/vlib&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Lamdonn/vlib&query=$.license&label=license)]()

**链接**：[vlib: C 语言版 STL，包含通用数据类型的队列、堆栈、双端队列、向量、列表、集合、映射等容器，以及通用的排序算法](https://gitee.com/Lamdonn/vlib)  
**特征**：C 语言模板库，提供了类似 C++ STL 的功能，包含了常用的容器，且可以使用任意数据类型。  

#### 要点

---

## Lua

### MicroLua

[![GitHub Repo stars](https://img.shields.io/github/stars/MicroLua/MicroLua)](https://github.com/MicroLua/MicroLua/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/MicroLua/MicroLua)](https://github.com/MicroLua/MicroLua/commits) | [![GitHub License](https://img.shields.io/github/license/MicroLua/MicroLua)]()

**链接**：[GitHub - MicroLua/MicroLua: Lua for the RP2040 microcontroller](https://github.com/MicroLua/MicroLua)  
**特征**：适用于树莓派 Pico 的 LUA 开发软件包，通过移植修改应该可以用于其他微控制器设备。  

#### 要点

- 由于树莓派 PR2040 采用的是 Linux 内核，因此该引擎库应该是在此内核基础上使用的；

---

### eLua

[![GitHub Repo stars](https://img.shields.io/github/stars/elua/elua)](https://github.com/elua/elua/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/elua/elua)](https://github.com/elua/elua/commits) | [![GitHub License](https://img.shields.io/github/license/elua/elua)]()

**链接**：[eLua - eluaproject](https://eluaproject.net/)  
**特征**：适用于嵌入式的 Lua 引擎。可在嵌入式平台使用 lua 脚本语言。  

#### 要点

- ~~lua 语法及使用方法可参考：((20230820124403-yaiem3a 'Lua'))；~~（待发布）
- 官方源码移植起来不方便，有个 5.3.5 版本的简易移植版，参考：[STM32-V6 LUA 简单移植 - STM32F429 - 硬汉嵌入式论坛 - Powered by Discuz!](https://www.armbbs.cn/forum.php?mod=viewthread&tid=94757&fromuid=58)；
- lua 脚本可能存在于各种地方，包括 emmc，sd 卡，外部的某个设备上；
- lua 使用的是动态内存，因此需要分配堆内存；
- 需要占用一定的 RAM 空间（20K 左右），小容量设备可能无法移植；
- 库移植时编译器不能包含 lua.c 和 luac.c 这两个文件，（它们包含 PC 上 Lua 解释器和编译器的 main 函数）；

---

## Python

### PikaPython

[![GitHub Repo stars](https://img.shields.io/github/stars/pikasTech/PikaPython)](https://github.com/pikasTech/PikaPython/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/pikasTech/PikaPython)](https://github.com/pikasTech/PikaPython/commits) | [![GitHub License](https://img.shields.io/github/license/pikasTech/PikaPython)]()

**链接**：[嵌入式脚本组件](https://pikapython.com/)  
**特征**：超轻量级 python 引擎，零依赖，零配置，使用 Python 代替 C 开发。具有大量的中文文档和视频资料。  

#### 要点

---

## Rust

### Rust Embedded

**链接**：[Rust Embedded](https://github.com/rust-embedded)  
**特征**：专注于改善在资源受限的环境和非传统平台中使用 Rust 的端到端体验。  

#### 要点

---

## JavaScript

### mJS

[![GitHub Repo stars](https://img.shields.io/github/stars/cesanta/mjs)](https://github.com/cesanta/mjs/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/cesanta/mjs)](https://github.com/cesanta/mjs/commits) | [![GitHub License](https://img.shields.io/github/license/cesanta/mjs)]()

**链接**：[cesanta/mjs: Embedded JavaScript engine for C/C++](https://github.com/cesanta/mjs)  
**特征**：专用于微控制器的 JavaScript 引擎，空间占用量小(RAM:1k,ROM:50k)，基于 ES6 标准。  

#### 要点

---

## Arduino

### ArduinoCore-API

[![GitHub Repo stars](https://img.shields.io/github/stars/arduino/ArduinoCore-API)](https://github.com/arduino/ArduinoCore-API/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/arduino/ArduinoCore-API)](https://github.com/arduino/ArduinoCore-API/commits) | [![GitHub License](https://img.shields.io/github/license/arduino/ArduinoCore-API)]()

**链接**：[arduino/ArduinoCore-API: Hardware independent layer of the Arduino cores defining the official API](https://github.com/arduino/ArduinoCore-API)  
**特征**：Arduino 内核的硬件独立层，使用基于 Arduino 相关的库时需要包含对应的 API 文件。  

#### 要点

- 使用介绍：[X-TRACK/Software/X-Track/ArduinoAPI at main · FASTSHIFT/X-TRACK](https://github.com/FASTSHIFT/X-TRACK/tree/main/Software/X-Track/ArduinoAPI)

---

## Android

### rawdrawandroid

[![GitHub Repo stars](https://img.shields.io/github/stars/cnlohr/rawdrawandroid)](https://github.com/cnlohr/rawdrawandroid/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/cnlohr/rawdrawandroid)](https://github.com/cnlohr/rawdrawandroid/commits) | [![GitHub License](https://img.shields.io/github/license/cnlohr/rawdrawandroid)]()

**链接**：[cnlohr/rawdrawandroid: Build android apps without any java, entirely in C and Make](https://github.com/cnlohr/rawdrawandroid)  
**特征**：使用 C 语言开发 Android 应用的开发框架，轻量且跨平台。  

#### 要点

- 开发时可能会关联 [Rawdraw](../ui-menu-lib/README.md#rawdraw) 和 [OpenGL ES](../ui-menu-lib/README.md#opengl) 库；

---

## 虚拟机（沙盒）

### EVM

[![GitHub Repo stars](https://img.shields.io/github/stars/scriptiot/evm)](https://github.com/scriptiot/evm/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/scriptiot/evm)](https://github.com/scriptiot/evm/commits) | [![GitHub License](https://img.shields.io/github/license/scriptiot/evm)]()

**链接**：[EVM 物联网虚拟机](https://scriptiot.github.io/)  
**特征**：针对物联网的超轻量虚拟机，由语法解析前端框架和字节码运行后端构成，可运行在资源受限制的单片机上。支持自行开发 app 运行在此虚拟机引擎上。  

#### 要点

---

### uvm32

[![GitHub Repo stars](https://img.shields.io/github/stars/ringtailsoftware/uvm32)](https://github.com/ringtailsoftware/uvm32/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/ringtailsoftware/uvm32)](https://github.com/ringtailsoftware/uvm32/commits) | [![GitHub License](https://img.shields.io/github/license/ringtailsoftware/uvm32)]()

**链接**：[ringtailsoftware/uvm32: Minimalist, dependency-free virtual machine sandbox for microcontrollers and other resource-constrained devices. Single C file, no dynamic memory allocations, asynchronous design, pure C99](https://github.com/ringtailsoftware/uvm32)  
**特征**：一款极简、无依赖的虚拟机（RISC-V）沙箱，专为微控制器及其他资源受限设备设计。单C文件，无动态内存分配，采用异步架构设计。可作为LUA、MicroPython等脚本引擎的替代品。  

#### 要点

---

## 游戏框架

### Arduboy

**链接**：[Arduboy](https://www.arduboy.com/)  
**特征**：提供游戏制作所需的编程接口，使其允许游戏玩家轻松制作 C/C++游戏，运行在该平台上，并通过社区共享。  

#### 要点

- 虽然官方只针对Arduino库提供了支持，但社区很多人将其移植到了其他芯片上；

---

### raylib

[![GitHub Repo stars](https://img.shields.io/github/stars/raysan5/raylib)](https://github.com/raysan5/raylib/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/raysan5/raylib)](https://github.com/raysan5/raylib/commits) | [![GitHub License](https://img.shields.io/github/license/raysan5/raylib)]()

**链接**：[raylib | A simple and easy-to-use library to enjoy videogames programming](https://www.raylib.com/)  
**特征**：纯C编写的游戏库，简易的视频、游戏编程库。  

#### 要点

---
