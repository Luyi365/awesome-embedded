# Timer and Time Library
<!-- i18n:language-selector:start -->
[中文](README.md) | **English**
<!-- i18n:language-selector:end -->

## Timers

### MultiTimer

[![GitHub Repo stars](https://img.shields.io/github/stars/0x1abin/MultiTimer)](https://github.com/0x1abin/MultiTimer/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/0x1abin/MultiTimer)](https://github.com/0x1abin/MultiTimer/commits) | [![GitHub License](https://img.shields.io/github/license/0x1abin/MultiTimer)]()

**Link** - [0x1abin/MultiTimer: Software timers extend module for embedded](https://github.com/0x1abin/MultiTimer)  
**Features** - Software-simulated timer module that replaces the conventional flag-checking approach, operating almost identically to a hardware timer.  

#### Key Points

- Creating and using this software timer is almost identical to using a hardware timer.
- Introduction: [MultiTimer | An Infinitely Extensible Software Timer](https://mp.weixin.qq.com/s/6Kd3MgkDtczhBEIf1YyEOg)

---

### SmartTimer

[![GitHub Repo stars](https://img.shields.io/github/stars/lmooml/SmartTimer)](https://github.com/lmooml/SmartTimer/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/lmooml/SmartTimer)](https://github.com/lmooml/SmartTimer/commits) | [![GitHub License](https://img.shields.io/github/license/lmooml/SmartTimer)]()

**Link** - [lmooml/SmartTimer: a lightly timer manager base on STM32F10X,to processing asynchronous event.](https://github.com/lmooml/SmartTimer)  
**Features** - Very practical timer scheduler for bare-metal systems. Besides basic polling callbacks, it can also set the number of polling iterations.  

#### Key Points

---

### microseconds

[![GitHub Repo stars](https://img.shields.io/github/stars/JayHeng/microseconds)](https://github.com/JayHeng/microseconds/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/JayHeng/microseconds)](https://github.com/JayHeng/microseconds/commits) | [![GitHub License](https://img.shields.io/github/license/JayHeng/microseconds)]()

**Link** - [JayHeng/microseconds: General microseconds library for MCU | General microsecond timing function framework for MCU, suitable for clock sources above 1MHz](https://github.com/JayHeng/microseconds)  
**Features** - Microsecond-level timer library based on the Cortex-M SysTick, with blocking and non-blocking delays. Most vendors already provide timer functions, so this mainly targets scenarios where the chip or timer module needs to be replaced.  

#### Key Points

- Suitable for MCUs with a timer clock source of at least 1MHz.

---

### perf\_counter

[![GitHub Repo stars](https://img.shields.io/github/stars/GorgonMeducer/perf_counter)](https://github.com/GorgonMeducer/perf_counter/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/GorgonMeducer/perf_counter)](https://github.com/GorgonMeducer/perf_counter/commits) | [![GitHub License](https://img.shields.io/github/license/GorgonMeducer/perf_counter)]()

**Link** - [GorgonMeducer/perf_counter: A dedicated performance counter for Cortex-M systick. It shares the SysTick with users' original SysTick function without interfering it. This library will bring new functionalities, such as performance counter, delay_us and clock() service defined in time.h](https://github.com/GorgonMeducer/perf_counter)  
**Features** - Based on the Cortex-M SysTick, it provides not only basic timer functions but also code-section cycle measurement and timing services, and supports RTOS. The code looks complex and is suited to company-level projects.  

#### Key Points

- The instructions look complicated, but the actual steps are:
  1. Only the source and header files are required; RTOS may also require `lib` and `os`, and possibly several assembly files;
  2. Configure the compiler for GNU extensions or use the gnu99 or gnu11 library;
  3. Add the `user_code_insert_to_systick_handler()` function to the `SysTick_Handler` callback (see the comments; it is unnecessary when the "ual" assembly file is supported);
  4. Initialize with `init_cycle_counter(bool)`;
- Provides timing services for the event recorder in MDK;
- Provides CMSIS-PACK for convenient library updating and loading.
- Introduction: [The Module Handed to You: A Super Embedded-System "Performance/Time" Toolbox](https://mp.weixin.qq.com/s/7RqVhwpzAtyYYMOKKfea-Q)

---

## Watchdogs

### LwWDG

[![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwwdg)](https://github.com/MaJerle/lwwdg/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwwdg)](https://github.com/MaJerle/lwwdg/commits) | [![GitHub License](https://img.shields.io/github/license/MaJerle/lwwdg)]()

**Link** - [LwWDG latest-develop documentation - LwWDG documentation](https://docs.majerle.eu/projects/lwwdg/en/latest/)  
**Features** - Lightweight watchdog library aimed mainly at operating systems. It monitors multiple threads and resets the system when one fails.  

#### Key Points

- Similar to a software-emulated watchdog and unrelated to the chip vendor's watchdog code.

---

## Time-related

### LwDTC

[![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwdtc)](https://github.com/MaJerle/lwdtc/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwdtc)](https://github.com/MaJerle/lwdtc/commits) | [![GitHub License](https://img.shields.io/github/license/MaJerle/lwdtc)]()

**Link** - [LwDTC latest-develop documentation - LwDTC documentation](https://docs.majerle.eu/projects/lwdtc/en/latest/)  
**Features** - Utility library for dates, times, and cron. Because Cron supports only numbers, rather than strings, parsing is faster.  

#### Key Points

- Supports the `tm` data structure in time.h for time calculations;
- Requires familiarity with cron syntax;

---
