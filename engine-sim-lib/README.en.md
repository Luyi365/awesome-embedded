# Engine (Simulation) Libraries
<!-- i18n:language-selector:start -->
[中文](README.md) | **English**
<!-- i18n:language-selector:end -->

> Engine libraries enable embedded systems to support programming languages they do not natively support.

## SoftFP

### softfp

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)

**Link** - [SoftFP Library](https://bellard.org/softfp/)  
**Features** - A software floating-point implementation for systems without a hardware floating-point unit (FPU).  

#### Key Points

---

## C++

### sds

[![GitHub Repo stars](https://img.shields.io/github/stars/antirez/sds)](https://github.com/antirez/sds/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/antirez/sds)](https://github.com/antirez/sds/commits) | [![GitHub License](https://img.shields.io/github/license/antirez/sds)]()

**Link** - [antirez/sds: Simple Dynamic Strings library for C](https://github.com/antirez/sds)  
**Features** - A simple dynamic-string library that uses heap memory and imitates the C++ `string` type in C.  

#### Key Points

- Usage guide: [Embedded Hodgepodge Weekly | Issue 15](https://mp.weixin.qq.com/s/C77TNpvKvj__ExUEXf4MhA)

---

### STR

[![GitHub Repo stars](https://img.shields.io/github/stars/mickjc750/str)](https://github.com/mickjc750/str/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/mickjc750/str)](https://github.com/mickjc750/str/commits) | [![GitHub License](https://img.shields.io/github/license/mickjc750/str)]()

**Link** - [mickjc750/str: C String handling library inspired by Luca Sas](https://github.com/mickjc750/str)  
**Features** - A more advanced string-processing library with string splitting, trimming, searching, and error-checking functions.  

#### Key Points

---

### etl

[![GitHub Repo stars](https://img.shields.io/github/stars/ETLCPP/etl)](https://github.com/ETLCPP/etl/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/ETLCPP/etl)](https://github.com/ETLCPP/etl/commits) | [![GitHub License](https://img.shields.io/github/license/ETLCPP/etl)]()

**Link** - [ETLCPP/etl: Embedded Template Library](https://github.com/ETLCPP/etl)  
**Features** - A C++ template library for embedded systems.  

#### Key Points

---

### LW_OOPC

[![GitHub Repo stars](https://img.shields.io/github/stars/Akagi201/lw_oopc)](https://github.com/Akagi201/lw_oopc/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/Akagi201/lw_oopc)](https://github.com/Akagi201/lw_oopc/commits) | [![GitHub License](https://img.shields.io/github/license/Akagi201/lw_oopc)]()

**Link** - [Akagi201/lw_oopc: modified from http://sourceforge.net/projects/lwoopc/](https://github.com/Akagi201/lw_oopc)  
**Features** - An object-oriented programming extension for embedded systems. It has been updated and optimized across multiple versions based on the original source and is simple to use.  

#### Key Points

---

### PLOOC

[![GitHub Repo stars](https://img.shields.io/github/stars/GorgonMeducer/PLOOC)](https://github.com/GorgonMeducer/PLOOC/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/GorgonMeducer/PLOOC)](https://github.com/GorgonMeducer/PLOOC/commits) | [![GitHub License](https://img.shields.io/github/license/GorgonMeducer/PLOOC)]()

**Link** - [GorgonMeducer/PLOOC: Protected Low-overhead Object Oriented Programming with ANSI-C](https://github.com/GorgonMeducer/PLOOC)  
**Features** - Provides object-oriented programming extensions in C, including private members, inheritance, overloading, and more.  

#### Key Points

- Usage guides:
  1. [Hands-on Modularization (2.5) - Gentleman's Agreement](https://mp.weixin.qq.com/s/4-cojkgnghB4TtaeEo63bQ)
  2. [Defensive Programming (X), OOPC Development (check)](https://mp.weixin.qq.com/s/enf5sTF1eWpBf0QjiVLdLw)

---

### vlib

[![Gitee Repo stars](https://gitee.com/Lamdonn/vlib/badge/star.svg?theme=gvp)](https://gitee.com/Lamdonn/vlib/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Lamdonn/vlib&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Lamdonn/vlib&query=$.license&label=license)]()

**Link** - [vlib: A C-language STL containing containers for general data types, including queues, stacks, deques, vectors, lists, sets, and maps, plus general sorting algorithms.](https://gitee.com/Lamdonn/vlib)  
**Features** - A C-language template library providing functionality similar to C++ STL, including common containers and support for arbitrary data types.  

#### Key Points

---

## Lua

### MicroLua

[![GitHub Repo stars](https://img.shields.io/github/stars/MicroLua/MicroLua)](https://github.com/MicroLua/MicroLua/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/MicroLua/MicroLua)](https://github.com/MicroLua/MicroLua/commits) | [![GitHub License](https://img.shields.io/github/license/MicroLua/MicroLua)]()

**Link** - [GitHub - MicroLua/MicroLua: Lua for the RP2040 microcontroller](https://github.com/MicroLua/MicroLua)  
**Features** - A LUA development package for Raspberry Pi Pico. With porting changes, it should also work on other microcontroller devices.  

#### Key Points

- Because the Raspberry Pi PR2040 uses the Linux kernel, this engine library should be used on top of that kernel;

---

### eLua

[![GitHub Repo stars](https://img.shields.io/github/stars/elua/elua)](https://github.com/elua/elua/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/elua/elua)](https://github.com/elua/elua/commits) | [![GitHub License](https://img.shields.io/github/license/elua/elua)]()

**Link** - [eLua - eluaproject](https://eluaproject.net/)  
**Features** - A Lua engine for embedded systems that lets Lua scripts run on embedded platforms.  

#### Key Points

- ~~For Lua syntax and usage, see: Lua;~~ (pending release)
- The official source is inconvenient to port. For a simple port of version 5.3.5, see: [Simple STM32-V6 LUA port - STM32F429 - Yinghan Embedded Forum - Powered by Discuz!](https://www.armbbs.cn/forum.php?mod=viewthread&tid=94757&fromuid=58);
- Lua scripts may reside in many places, including eMMC, SD cards, or an external device;
- Lua uses dynamic memory and therefore requires heap-memory allocation;
- It requires a certain amount of RAM (about 20K), so porting may not be possible on small-capacity devices;
- When porting the library, the compiler must not include the `lua.c` and `luac.c` files (they contain the `main` functions of the Lua interpreter and compiler on a PC);

---

## Python

### PikaPython

[![GitHub Repo stars](https://img.shields.io/github/stars/pikasTech/PikaPython)](https://github.com/pikasTech/PikaPython/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/pikasTech/PikaPython)](https://github.com/pikasTech/PikaPython/commits) | [![GitHub License](https://img.shields.io/github/license/pikasTech/PikaPython)]()

**Link** - [Embedded scripting component](https://pikapython.com/)  
**Features** - An ultra-lightweight Python engine with zero dependencies and zero configuration that uses Python instead of C for development. It has extensive Chinese documentation and video materials.  

#### Key Points

---

## Rust

### Rust Embedded

**Link** - [Rust Embedded](https://github.com/rust-embedded)  
**Features** - Focuses on improving the end-to-end experience of using Rust in resource-constrained environments and on nontraditional platforms.  

#### Key Points

---

## JavaScript

### mJS

[![GitHub Repo stars](https://img.shields.io/github/stars/cesanta/mjs)](https://github.com/cesanta/mjs/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/cesanta/mjs)](https://github.com/cesanta/mjs/commits) | [![GitHub License](https://img.shields.io/github/license/cesanta/mjs)]()

**Link** - [cesanta/mjs: Embedded JavaScript engine for C/C++](https://github.com/cesanta/mjs)  
**Features** - A JavaScript engine specifically for microcontrollers, with a small footprint (RAM: 1k, ROM: 50k) and based on the ES6 standard.  

#### Key Points

---

## Arduino

### ArduinoCore-API

[![GitHub Repo stars](https://img.shields.io/github/stars/arduino/ArduinoCore-API)](https://github.com/arduino/ArduinoCore-API/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/arduino/ArduinoCore-API)](https://github.com/arduino/ArduinoCore-API/commits) | [![GitHub License](https://img.shields.io/github/license/arduino/ArduinoCore-API)]()

**Link** - [arduino/ArduinoCore-API: Hardware independent layer of the Arduino cores defining the official API](https://github.com/arduino/ArduinoCore-API)  
**Features** - The hardware-independent layer of the Arduino core. Include the corresponding API files when using Arduino-related libraries.  

#### Key Points

- Usage guide: [X-TRACK/Software/X-Track/ArduinoAPI at main · FASTSHIFT/X-TRACK](https://github.com/FASTSHIFT/X-TRACK/tree/main/Software/X-Track/ArduinoAPI)

---

## Android

### rawdrawandroid

[![GitHub Repo stars](https://img.shields.io/github/stars/cnlohr/rawdrawandroid)](https://github.com/cnlohr/rawdrawandroid/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/cnlohr/rawdrawandroid)](https://github.com/cnlohr/rawdrawandroid/commits) | [![GitHub License](https://img.shields.io/github/license/cnlohr/rawdrawandroid)]()

**Link** - [cnlohr/rawdrawandroid: Build android apps without any java, entirely in C and Make](https://github.com/cnlohr/rawdrawandroid)  
**Features** - A lightweight, cross-platform framework for developing Android applications in C.  

#### Key Points

- Development may involve the [Rawdraw](../ui-menu-lib/README.en.md#rawdraw) and [OpenGL ES](../ui-menu-lib/README.en.md#opengl) libraries;

---

## Virtual Machines (Sandboxes)

### EVM

[![GitHub Repo stars](https://img.shields.io/github/stars/scriptiot/evm)](https://github.com/scriptiot/evm/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/scriptiot/evm)](https://github.com/scriptiot/evm/commits) | [![GitHub License](https://img.shields.io/github/license/scriptiot/evm)]()

**Link** - [EVM IoT virtual machine](https://scriptiot.github.io/)  
**Features** - An ultra-lightweight IoT virtual machine composed of a syntax-parsing frontend framework and a bytecode-execution backend. It runs on resource-constrained microcontrollers and supports running self-developed apps on this virtual-machine engine.  

#### Key Points

---

### uvm32

[![GitHub Repo stars](https://img.shields.io/github/stars/ringtailsoftware/uvm32)](https://github.com/ringtailsoftware/uvm32/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/ringtailsoftware/uvm32)](https://github.com/ringtailsoftware/uvm32/commits) | [![GitHub License](https://img.shields.io/github/license/ringtailsoftware/uvm32)]()

**Link** - [ringtailsoftware/uvm32: Minimalist, dependency-free virtual machine sandbox for microcontrollers and other resource-constrained devices. Single C file, no dynamic memory allocations, asynchronous design, pure C99](https://github.com/ringtailsoftware/uvm32)  
**Features** - A minimalist, dependency-free virtual-machine (RISC-V) sandbox designed for microcontrollers and other resource-constrained devices. It is a single C file with no dynamic memory allocation and an asynchronous architecture. It can replace script engines such as LUA and MicroPython.  

#### Key Points

---

## Multimedia

### FFmpeg

[![GitHub Repo stars](https://img.shields.io/github/stars/FFmpeg/FFmpeg)](https://github.com/FFmpeg/FFmpeg/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/FFmpeg/FFmpeg)](https://github.com/FFmpeg/FFmpeg/commits) | [![GitHub License](https://img.shields.io/github/license/FFmpeg/FFmpeg)]()

**Link** - [FFmpeg](https://ffmpeg.org)  
**Features** - A highly renowned cross-platform audio/video processing framework that provides a suite of audio/video codec development tools.  

#### Key Points

- The development suite includes, but is not limited to:

  **[libavutil](https://ffmpeg.org//libavutil.html)** is a library containing functions that simplify programming, including random-number generators, data structures, mathematical routines, core multimedia utilities, and more.

  **[libavcodec](https://ffmpeg.org//libavcodec.html)** is a library containing decoders and encoders for audio/video codecs.

  **[libav format](https://ffmpeg.org//libavformat.html)** is a library containing multiplexers and demultiplexers for multimedia container formats.

  **[libavdevice](https://ffmpeg.org//libavdevice.html)** is a library containing input and output devices for capture and rendering across many common multimedia input/output frameworks, including Video4Linux, Video4Linux2, VfW, and ALSA.

  **[libavfilter](https://ffmpeg.org//libavfilter.html)** is a library containing media filters.

  **[libswscale](https://ffmpeg.org//libswscale.html)** is a library that performs highly optimized image-scaling and color-space/pixel-format conversion operations.

  **[libswresample](https://ffmpeg.org//libswresample.html)** is a library that performs highly optimized audio resampling, rematrixing, and sample-format conversion operations.
- Usage guide: [ffmpeg-libav-tutorial/README-cn.md at master · leandromoreira/ffmpeg-libav-tutorial](https://github.com/leandromoreira/ffmpeg-libav-tutorial/blob/master/README-cn.md)

---

## Game Frameworks

### Arduboy

**Link** - [Arduboy](https://www.arduboy.com/)  
**Features** - Provides the programming interfaces required to make games, allowing players to create C/C++ games easily, run them on the platform, and share them through the community.  

#### Key Points

- Although official support is only provided for Arduino libraries, many community members have ported it to other chips;

---

### raylib

[![GitHub Repo stars](https://img.shields.io/github/stars/raysan5/raylib)](https://github.com/raysan5/raylib/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/raysan5/raylib)](https://github.com/raysan5/raylib/commits) | [![GitHub License](https://img.shields.io/github/license/raysan5/raylib)]()

**Link** - [raylib | A simple and easy-to-use library to enjoy videogames programming](https://www.raylib.com/)  
**Features** - A game library written entirely in C that provides simple video and game-programming capabilities.  

#### Key Points

---
