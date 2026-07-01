# TIMER与TIME库

> 这里的 TIMER 其实就是定时器，而 TIME 指的是类似于 `time.h` 这种时间、日期相关库。

## 定时器

### MultiTimer

[![GitHub Repo stars](https://img.shields.io/github/stars/0x1abin/MultiTimer)](https://github.com/0x1abin/MultiTimer/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/0x1abin/MultiTimer)](https://github.com/0x1abin/MultiTimer/commits) | [![GitHub License](https://img.shields.io/github/license/0x1abin/MultiTimer)]()

**链接**：[0x1abin/MultiTimer: Software timers extend module for embedded](https://github.com/0x1abin/MultiTimer)  
**特征**：取代传统的标志位判断方式，采用软件模拟定时器来更优雅更便捷地管理程序的时间触发时序。  

#### 要点

- 该软定时器的创建及使用几乎和硬定时器一致。
- 使用介绍：[MultiTimer | 一款可无限扩展的软件定时器](https://mp.weixin.qq.com/s/6Kd3MgkDtczhBEIf1YyEOg)

---

### SmartTimer

[![GitHub Repo stars](https://img.shields.io/github/stars/lmooml/SmartTimer)](https://github.com/lmooml/SmartTimer/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/lmooml/SmartTimer)](https://github.com/lmooml/SmartTimer/commits) | [![GitHub License](https://img.shields.io/github/license/lmooml/SmartTimer)]()

**链接**：[lmooml/SmartTimer: a lightly timer manager base on STM32F10X,to processing asynchronous event.](https://github.com/lmooml/SmartTimer)  
**特征**：裸机下十分好用的定时器调度器，除了基本轮询回调外，还可以设置轮询次数。  

#### 要点

---

### microseconds

[![GitHub Repo stars](https://img.shields.io/github/stars/JayHeng/microseconds)](https://github.com/JayHeng/microseconds/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/JayHeng/microseconds)](https://github.com/JayHeng/microseconds/commits) | [![GitHub License](https://img.shields.io/github/license/JayHeng/microseconds)]()

**链接**：[JayHeng/microseconds: General microseconds library for MCU | 适用 MCU 的通用微秒计时函数框架，适用 1MHz 以上时钟源](https://github.com/JayHeng/microseconds)  
**特征**：基于 Cortex-M 内核的 SysTick 做的微秒级别定时器库，有阻塞和非阻塞延迟。  

#### 要点

- 适合定时器时钟源不小于 1MHz 的 MCU。

---

### perf\_counter

[![GitHub Repo stars](https://img.shields.io/github/stars/GorgonMeducer/perf_counter)](https://github.com/GorgonMeducer/perf_counter/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/GorgonMeducer/perf_counter)](https://github.com/GorgonMeducer/perf_counter/commits) | [![GitHub License](https://img.shields.io/github/license/GorgonMeducer/perf_counter)]()

**链接**：[GorgonMeducer/perf_counter: A dedicated performance counter for Cortex-M systick. It shares the SysTick with users' original SysTick function without interfering it. This library will bring new functionalities, such as performance counter, delay_us and clock() service defined in time.h](https://github.com/GorgonMeducer/perf_counter)  
**特征**：基于 Cortex-M 内核的 SysTick，不仅拥有基本的定时器功能，还具有代码段的周期测量、定时服务等功能，且支持 RTOS。  

#### 要点

- 说明看起来很复杂，但其实要做的是：
  1. 文件只需要源文件和头文件，RTOS 可能需要"lib"和"os"，也可能需要几个汇编文件；
  2. 编译器设置 GNU 扩展库或使用 gnu99 或 gnu11 库；
  3. `user_code_insert_to_systick_handler()`函数添加到 `SysTick_Handler`回调中（看注释，如果支持"ual"汇编文件，则不需要添加）；
  4. 初始化使用 `init_cycle_counter(bool)`即可；
- 在 MDK 中为事件记录器提供定时服务；
- 提供 CMSIS-PACK，方便更新加载库。
- 使用介绍：[【喂到嘴边了的模块】超级嵌入式系统“性能/时间”工具箱](https://mp.weixin.qq.com/s/7RqVhwpzAtyYYMOKKfea-Q)

---

## 看门狗

### LwWDG

[![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwwdg)](https://github.com/MaJerle/lwwdg/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwwdg)](https://github.com/MaJerle/lwwdg/commits) | [![GitHub License](https://img.shields.io/github/license/MaJerle/lwwdg)]()

**链接**：[LwWDG latest-develop documentation — LwWDG documentation](https://docs.majerle.eu/projects/lwwdg/en/latest/)  
**特征**：轻量级的看门狗库，主要针对操作系统， 监视多个线程并在其中一个线程失败时重置系统。  

#### 要点

- 类似软件方式模拟看门狗程序，与芯片厂商的开门狗代码无交集。

---

## TIME 相关

### LwDTC

[![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwdtc)](https://github.com/MaJerle/lwdtc/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwdtc)](https://github.com/MaJerle/lwdtc/commits) | [![GitHub License](https://img.shields.io/github/license/MaJerle/lwdtc)]()

**链接**：[LwDTC latest-develop documentation — LwDTC documentation](https://docs.majerle.eu/projects/lwdtc/en/latest/)  
**特征**：用于日期、时间和 cron 实用程序库，因为 Cron 仅支持数字，没有字符串，所以解析速度更快。  

#### 要点

- 支持 time.h 结构 tm 数据结构以进行时间运算；
- 需要了解 cron 语法；

---
