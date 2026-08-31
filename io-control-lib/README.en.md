# Pin and Control Library
<!-- i18n:language-selector:start -->
[中文](README.md) | **English**
<!-- i18n:language-selector:end -->

> This library primarily contains functions related to pin operations and indirect uses of their capabilities, such as PWM.

## Buttons

> During program execution, an interrupt can interrupt a button state. When execution returns, the button state is read again, causing a single press to be read many times and resulting in program errors. The solution is to <ins>disable interrupts after detecting a button press and enable them after the button is released</ins>.

### key_detect

**Link** - [Button Detection Framework - Code Snippet - Gitee.com](https://gitee.com/Luyi365/codes/1bw4y628enkoj3zfupamg78)  
**Features** - A simple button-detection component that uses event registration and provides basic button functionality.  

#### Key Points

- Usage guide: [Button Detection Component.pdf](assets/按键检测组件-20240430172258-n7or4pn.pdf)

---

### key_module

[![Gitee Repo stars](https://gitee.com/embediot/key_module/badge/star.svg?theme=gvp)](https://gitee.com/embediot/key_module/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/embediot/key_module&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/embediot/key_module&query=$.license&label=license)]()

**Link** - [key_module: A general-purpose button-detection module for microcontrollers that handles button events including press, release, single click, double click, tap, and long press; combination buttons are planned for expansion.](https://gitee.com/embediot/key_module)  
**Features** - An easy-to-use button-detection module that uses event callbacks and provides basic functionality other than matrix-key buttons.  

#### Key Points

---

### FlexibleButton

[![GitHub Repo stars](https://img.shields.io/github/stars/hellozimo/FlexibleButton)](https://github.com/hellozimo/FlexibleButton/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/hellozimo/FlexibleButton)](https://github.com/hellozimo/FlexibleButton/commits) | [![GitHub License](https://img.shields.io/github/license/hellozimo/FlexibleButton)]()

**Link** - [murphyzhao/FlexibleButton: Flexible button processing library (Flexible Button) | Button driver | Supports single click, double click, repeated click, long press, and automatic debounce | Flexibly adapts to interrupts and low power | Implement combination buttons as needed](https://github.com/murphyzhao/FlexibleButton)  
**Features** - Detects buttons through intermittent polling scans, scanning and processing all button states at once. It supports most individual button events; combination buttons and interrupt triggering must be added manually.  

#### Key Points

- Introduction: [Embedded Miscellany Weekly | Issue 6](https://mp.weixin.qq.com/s/pts7XOWmb74ZXtz4TR9ViA)
- Because all buttons are scanned at once, when interrupt triggering is used, every button must support interrupt triggering.
- For matrix keys, only the `uint8_t  (*usr_button_read)(void*);` interface function needs to be modified, for example:
  ```c
  static uint8_t common_btn_read(void *arg)
  {
      uint8_t value = 0;

      flex_button_t *btn = (flex_button_t *)arg;

      if(btn->id == Read_key()){    //矩阵按键是直接读取按键ID的
          value = 1;
      }
      else{
          value = 0;
      }

      return value;
  }
  ```

---

### MultiButton

[![GitHub Repo stars](https://img.shields.io/github/stars/0x1abin/MultiButton)](https://github.com/0x1abin/MultiButton/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/0x1abin/MultiButton)](https://github.com/0x1abin/MultiButton/commits) | [![GitHub License](https://img.shields.io/github/license/0x1abin/MultiButton)]()

**Link** - [0x1abin/MultiButton: Button driver for embedded system](https://github.com/0x1abin/MultiButton)  
**Features** - A timer-triggered, event-driven button driver module designed with an object-oriented approach; each button object is managed by a separate data structure.  

#### Key Points

- Because scanning is timer-triggered, the trigger function must be rewritten when interrupt triggering is used.

---

### cotKey

[![Gitee Repo stars](https://gitee.com/cot_package/cot_key/badge/star.svg?theme=gvp)](https://gitee.com/cot_package/cot_key/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/cot_package/cot_key&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/cot_package/cot_key&query=$.license&label=license)]()

**Link** - [cotKey: Component code for recognizing common button actions on embedded devices](https://gitee.com/cot_package/cot_key)  
**Features** - A listener-based button-recognition library that supports single click, double click, multiple click, short press, and long press, but supports only a single button.  

#### Key Points

- Introduction: [Lightweight Button Action Recognition Module (C Language)](https://mp.weixin.qq.com/s/7Dx1S-rJuFTwMyu1hNCuhg)

---

### key_board

[![Gitee Repo stars](https://gitee.com/wei513723/key_board/badge/star.svg?theme=gvp)](https://gitee.com/wei513723/key_board/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/wei513723/key_board&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/wei513723/key_board&query=$.license&label=license)]()

**Link** - [key_board: Compact multifunction button support for microcontrollers; its strongest feature supports unlimited numbers of buttons and arbitrary combinations of any states of any buttons.](https://gitee.com/wei513723/key_board)  
**Features** - Uses button registration, heap memory by default, and scans and processes all button states at once. It includes matrix keypad and combination-button functionality.  

#### Key Points

- The program uses heap memory by default, so space must be allocated for it;
- Introduction: [A Compact Button Processing Module!](https://mp.weixin.qq.com/s/VGRR7SU0JOKemxEZhBR9Og)

---

### LwBTN

![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwbtn) | ![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwbtn) | ![GitHub License](https://img.shields.io/github/license/MaJerle/lwbtn)

**Link** - [LwBTN latest-develop documentation — LwBTN documentation](https://docs.majerle.eu/projects/lwbtn/en/latest/)  
**Features** - A professional button-event management library.  

#### Key Points

- Introduction: [A Lightweight Button Management Library!](https://mp.weixin.qq.com/s/MLYz75-7ydv755w4wIP1xQ)

---

## LED

### cotLed

![Gitee Repo stars](https://gitee.com/cot_package/cot_led/badge/star.svg?theme=gvp) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/cot_package/cot_led&query=$.pushed_at&label=lastcommit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/cot_package/cot_led&query=$.license&label=license)

**Link** - [cotLed: Component code for controlling common indicator lights on embedded devices](https://gitee.com/cot_package/cot_led)  
**Features** - A lightweight LED control module that can implement multiple LED mode states.  

#### Key Points

- Modern chips include a variety of PWM controls. They are the most efficient to use, but relatively complex. This library is suitable when only basic PWM control is available or when convenience is desired, because its power consumption is likely higher.
- Introduction: [Lightweight LED Control Module](https://mp.weixin.qq.com/s/A2arPl2oRYLjFt4STYnljA)

---

### led_module

![Gitee Repo stars](https://gitee.com/embediot/led_module/badge/star.svg?theme=gvp) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/embediot/led_module&query=$.pushed_at&label=lastcommit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/embediot/led_module&query=$.license&label=license)

**Link** - [led_module: General microcontroller LED display module, based on embedded C object-oriented programming and the simple factory design pattern](https://gitee.com/embediot/led_module)  
**Features** - A general LED display module based on object-oriented programming and the simple factory pattern.  

#### Key Points

- Introduction: [Design a General LED Display Module with Object-Oriented Programming and the Simple Factory Pattern.](https://mp.weixin.qq.com/s/AhvTI8-qQHN7eTX6JmpLWA)

---

## PID

### pid_temperature_control

[![Gitee Repo stars](https://gitee.com/jiezhuonew/pid_temperature_control/badge/star.svg?theme=gvp)](https://gitee.com/jiezhuonew/pid_temperature_control/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/jiezhuonew/pid_temperature_control&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/jiezhuonew/pid_temperature_control&query=$.license&label=license)]()

**Link** - [pid_temperature_control: PID temperature control](https://gitee.com/jiezhuonew/pid_temperature_control)  
**Features** - PID temperature control; an excellent example that can extend PID control to other domains.  

#### Key Points

---

## CNC

> An abbreviation for Computer Numerical Control, referring to machine tools whose movement (direction, speed, machining amount, and so on) is automated through programming.  
> The programming languages used are G-code (for motion and positioning) together with M-code (for auxiliary functions).  

### Grbl

[![GitHub Repo stars](https://img.shields.io/github/stars/gnea/grbl)](https://github.com/gnea/grbl/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/gnea/grbl)](https://github.com/gnea/grbl/commits) | [![GitHub License](https://img.shields.io/github/license/gnea/grbl)]()

**Link** - [gnea/grbl: An open source, embedded, high performance g-code-parser and CNC milling controller written in optimized C that will run on a straight Arduino](https://github.com/gnea/grbl)  
**Features** - A well-known open-source CNC codebase used for laser cutters, automated handwriting machines, drilling machines, graffiti painters, and quirky plotters. It is a maker favorite and an industry standard.  

#### Key Points

- Grbl was originally designed for 8-bit Arduino platforms. To accommodate more advanced 32-bit processors, a developer rewrote the code and separated the abstraction and core layers, enabling support for more processors: [grblHAL](https://github.com/grblHAL)
- Introduction: [grbl-learning: Close Reading and Analysis of Grbl Source Code, with Line-Level Chinese Comments and Detailed Examples](https://gitee.com/ren12345/grbl-learning)；

---

### µCNC

[![GitHub Repo stars](https://img.shields.io/github/stars/Paciente8159/uCNC)](https://github.com/Paciente8159/uCNC/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/Paciente8159/uCNC)](https://github.com/Paciente8159/uCNC/commits) | [![GitHub License](https://img.shields.io/github/license/Paciente8159/uCNC)]()

**Link** - [Paciente8159/uCNC: µCNC - Universal CNC firmware for microcontrollers](https://github.com/Paciente8159/uCNC)  
**Features** - General-purpose CNC firmware for microcontrollers.  

#### Key Points

---
