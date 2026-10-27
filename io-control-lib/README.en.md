# Pin and Control Library
<!-- i18n:language-selector:start -->
[中文](README.md) | **English**
<!-- i18n:language-selector:end -->

> This library primarily contains functions related to pin operations and indirect uses of their capabilities, such as PWM.

## Buttons

> During program execution, an interrupt can interrupt a button state. When execution returns, the button state is read again, causing a single press to be read many times and resulting in program errors. The solution is to <ins>disable interrupts after detecting a button press and enable them after the button is released</ins>.

### key_detect

[![GitHub Repo stars](https://img.shields.io/github/stars/Luyi365/key_detect)](https://github.com/Luyi365/key_detect/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/Luyi365/key_detect)](https://github.com/Luyi365/key_detect/commits) | [![GitHub License](https://img.shields.io/github/license/Luyi365/key_detect)]()

**Link** - [Luyi365/key_detect: A simple button-detection component that uses event registration to provide the most basic button functionality.](https://github.com/Luyi365/key_detect)  
**Features** - Simple button-detection component that uses button registration and lets you set single-click/double-click/long-press properties for each button individually.  

#### Key Points

---

### key_module

[![Gitee Repo stars](https://gitee.com/embediot/key_module/badge/star.svg?theme=gvp)](https://gitee.com/embediot/key_module/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/embediot/key_module&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/embediot/key_module&query=$.license&label=license)]()

**Link** - [key_module: A general-purpose button-detection module for microcontrollers that handles button events including press, release, single click, double click, tap, and long press; combination buttons are planned for expansion.](https://gitee.com/embediot/key_module)  
**Features** - Simple button-detection module that uses event callbacks and provides the other basic functions apart from matrix keys.  

#### Key Points

---

### FlexibleButton

[![GitHub Repo stars](https://img.shields.io/github/stars/hellozimo/FlexibleButton)](https://github.com/hellozimo/FlexibleButton/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/hellozimo/FlexibleButton)](https://github.com/hellozimo/FlexibleButton/commits) | [![GitHub License](https://img.shields.io/github/license/hellozimo/FlexibleButton)]()

**Link** - [murphyzhao/FlexibleButton: Flexible button processing library (Flexible Button) | Button driver | Supports single click, double click, repeated click, long press, and automatic debounce | Flexibly adapts to interrupts and low power | Implement combination buttons as needed](https://github.com/murphyzhao/FlexibleButton)  
**Features** - Stable button-processing library that scans and processes all button states in one pass, with triggers for a variety of button events, and leaves notes on how to implement combination buttons and interrupt triggering.  

#### Key Points

- Introduction: [Embedded Miscellany Weekly | Issue 6](https://mp.weixin.qq.com/s/pts7XOWmb74ZXtz4TR9ViA)
- Because all buttons are scanned at once, when interrupt triggering is used, every button must support interrupt triggering.
- For matrix keys, only the `uint8_t  (*usr_button_read)(void*);` interface function needs to be modified, for example:
  ```c
  static uint8_t common_btn_read(void *arg)
  {
      uint8_t value = 0;

      flex_button_t *btn = (flex_button_t *)arg;

      if(btn->id == Read_key()){    // For a matrix keypad, the key ID is read directly
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
**Features** - State-machine button library designed with an object-oriented approach, so that each button object is managed by its own data structure.  

#### Key Points

- Because scanning is timer-triggered, the trigger function must be rewritten when interrupt triggering is used.

---

### cotKey

[![Gitee Repo stars](https://gitee.com/cot_package/cot_key/badge/star.svg?theme=gvp)](https://gitee.com/cot_package/cot_key/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/cot_package/cot_key&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/cot_package/cot_key&query=$.license&label=license)]()

**Link** - [cotKey: Component code for recognizing common button actions on embedded devices](https://gitee.com/cot_package/cot_key)  
**Features** - Listener-based button-recognition library that is more flexible than other button libraries, covering single click, double click, multiple click, short press, long press, and other requirements.  

#### Key Points

- Introduction: [Lightweight Button Action Recognition Module (C Language)](https://mp.weixin.qq.com/s/7Dx1S-rJuFTwMyu1hNCuhg)

---

### key_board

[![Gitee Repo stars](https://gitee.com/wei513723/key_board/badge/star.svg?theme=gvp)](https://gitee.com/wei513723/key_board/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/wei513723/key_board&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/wei513723/key_board&query=$.license&label=license)]()

**Link** - [key_board: Compact multifunction button support for microcontrollers; its strongest feature supports unlimited numbers of buttons and arbitrary combinations of any states of any buttons.](https://gitee.com/wei513723/key_board)  
**Features** - Uses button registration and heap memory by default, scanning and processing all button states at once, and includes matrix-keypad and combination-button functionality.  

#### Key Points

- Introduction: [A Compact Button Processing Module!](https://mp.weixin.qq.com/s/VGRR7SU0JOKemxEZhBR9Og)

---

### LwBTN

![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwbtn) | ![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwbtn) | ![GitHub License](https://img.shields.io/github/license/MaJerle/lwbtn)

**Link** - [LwBTN latest-develop documentation — LwBTN documentation](https://docs.majerle.eu/projects/lwbtn/en/latest/)  
**Features** - Professional button-event management library with rich configuration and comprehensive features.  

#### Key Points

- Introduction: [A Lightweight Button Management Library!](https://mp.weixin.qq.com/s/MLYz75-7ydv755w4wIP1xQ)

---

## LED

### cotLed

![Gitee Repo stars](https://gitee.com/cot_package/cot_led/badge/star.svg?theme=gvp) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/cot_package/cot_led&query=$.pushed_at&label=lastcommit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/cot_package/cot_led&query=$.license&label=license)

**Link** - [cotLed: Component code for controlling common indicator lights on embedded devices](https://gitee.com/cot_package/cot_led)  
**Features** - Lightweight LED control module capable of driving multiple LED mode states (blinking, breathing, custom, and so on).  

#### Key Points

- Modern chips include a wide variety of built-in IO controls, and the vendor's own modes are often the most efficient. This library is suitable when only basic PWM control is available.
- Introduction: [Lightweight LED Control Module](https://mp.weixin.qq.com/s/A2arPl2oRYLjFt4STYnljA)

---

### led_module

![Gitee Repo stars](https://gitee.com/embediot/led_module/badge/star.svg?theme=gvp) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/embediot/led_module&query=$.pushed_at&label=lastcommit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/embediot/led_module&query=$.license&label=license)

**Link** - [led_module: General microcontroller LED display module, based on embedded C object-oriented programming and the simple factory design pattern](https://gitee.com/embediot/led_module)  
**Features** - Simple LED display library built on object-oriented and simple-factory patterns, with no custom modes but with color attributes.  

#### Key Points

- Introduction: [Design a General LED Display Module with Object-Oriented Programming and the Simple Factory Pattern.](https://mp.weixin.qq.com/s/AhvTI8-qQHN7eTX6JmpLWA)

---

## PID

### pid_temperature_control

[![Gitee Repo stars](https://gitee.com/jiezhuonew/pid_temperature_control/badge/star.svg?theme=gvp)](https://gitee.com/jiezhuonew/pid_temperature_control/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/jiezhuonew/pid_temperature_control&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/jiezhuonew/pid_temperature_control&query=$.license&label=license)]()

**Link** - [pid_temperature_control: PID temperature control](https://gitee.com/jiezhuonew/pid_temperature_control)  
**Features** - PID temperature control; a solid example whose approach extends well to other domains.  

#### Key Points

---

## CNC

> An abbreviation for Computer Numerical Control, referring to machine tools whose movement (direction, speed, machining amount, and so on) is automated through programming.  
> The programming languages used are G-code (for motion and positioning) together with M-code (for auxiliary functions).  

### Grbl

[![GitHub Repo stars](https://img.shields.io/github/stars/gnea/grbl)](https://github.com/gnea/grbl/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/gnea/grbl)](https://github.com/gnea/grbl/commits) | [![GitHub License](https://img.shields.io/github/license/gnea/grbl)]()

**Link** - [gnea/grbl: An open source, embedded, high performance g-code-parser and CNC milling controller written in optimized C that will run on a straight Arduino](https://github.com/gnea/grbl)  
**Features** - An industry-renowned open-source CNC codebase used for laser cutters, automated handwriting machines, drilling machines, graffiti painters, and quirky plotters; a maker favorite and an industry standard.  

#### Key Points

- Grbl was originally designed for 8-bit Arduino platforms. To accommodate more advanced 32-bit processors, a developer rewrote the code and separated the abstraction and core layers, enabling support for more processors: [grblHAL](https://github.com/grblHAL)
- Introduction: [grbl-learning: Close Reading and Analysis of Grbl Source Code, with Line-Level Chinese Comments and Detailed Examples](https://gitee.com/ren12345/grbl-learning);

---

### µCNC

[![GitHub Repo stars](https://img.shields.io/github/stars/Paciente8159/uCNC)](https://github.com/Paciente8159/uCNC/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/Paciente8159/uCNC)](https://github.com/Paciente8159/uCNC/commits) | [![GitHub License](https://img.shields.io/github/license/Paciente8159/uCNC)]()

**Link** - [Paciente8159/uCNC: µCNC - Universal CNC firmware for microcontrollers](https://github.com/Paciente8159/uCNC)  
**Features** - General-purpose CNC firmware for microcontrollers that keeps its features compact and its components modular.  

#### Key Points

---
