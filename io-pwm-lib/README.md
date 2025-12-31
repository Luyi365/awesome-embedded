# IO与PWM库

> 该库与操作 IO 的相关功能为主，以及间接性的使用 IO 特性，类似 PWM 这种。

## 按键

> 在程序运行时中断会打断按键的状态，再次回到时会再次读取按键的状态，导致按键会在按下一次后被读取很多次导致程序错误，解决办法是<u>在检测到按键按下后关闭中断，按键松开后打开中断</u>。

### key_detect

**链接**：[按键检测框架 - 代码片段 - Gitee.com](https://gitee.com/Luyi365/codes/1bw4y628enkoj3zfupamg78)
**特征**：简易的按键检测组件，采用注册事件，提供最基本的按键功能。

#### 要点

- 使用说明：[按键检测组件.pdf](assets/按键检测组件-20240430172258-n7or4pn.pdf)

---

### key_module

**链接**：[EmbedIoT Studio/key_module - 码云 - 开源中国 (gitee.com)](https://gitee.com/embediot/key_module)
**特征**：简单易用的按键检测模块，采用事件回调，提供除矩阵按键的其他基本功能。

#### 要点

---

### FlexibleButton

**链接**：[murphyzhao/FlexibleButton: 灵活的按键处理库（Flexible Button）| 按键驱动 | 支持单击、双击、连击、长按、自动消抖 | 灵活适配中断和低功耗 | 按需实现组合按键 (github.com)](https://github.com/murphyzhao/FlexibleButton)
**特征**：间断轮询扫描的方式检测按键，一次扫描和处理所有按键状态，支持大多数单个按键事件触发。组合按键和中断触发需要自行添加。

#### 要点

- 使用介绍：[嵌入式大杂烩周记 | 第 6 期](https://mp.weixin.qq.com/s/pts7XOWmb74ZXtz4TR9ViA)
- 由于采用的是一次扫描全按键的方式，当使用中断触发时，必须保证所有按键均具有中断触发功能。
- 矩阵按键只需要修改 `uint8_t  (*usr_button_read)(void*);` 接口函数即可，例如：

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

**链接**：[0x1abin/MultiButton: Button driver for embedded system (github.com)](https://github.com/0x1abin/MultiButton)
**特征**：定时器触发扫描，事件驱动型按键驱动模块，基于面向对象方式设计思路，每个按键对象单独用一份数据结构管理。

#### 要点

- 由于使用定时器触发扫描，当使用中断触发时，需要改写触发函数。

---

### cotKey

**链接**：[cotKey: 嵌入式设备常用的按键动作识别模块组件代码 (gitee.com)](https://gitee.com/cot_package/cot_key)
**特征**：监听型按键识别库，可以实现单击、双击、多击、短按和长按等多种要求的功能，但只支持单一按键功能。

#### 要点

- 使用介绍：[轻量级按键动作识别模块（C语言）](https://mp.weixin.qq.com/s/7Dx1S-rJuFTwMyu1hNCuhg)

---

### key_board

**链接**：[key_board: 用于单片机中的小巧多功能按键支持；最强功能：支持不限数量、任意按键、任意按键的任意状态之间的随意组合！！！ (gitee.com)](https://gitee.com/wei513723/key_board)
**特征**：采用按键注册的方式，默认使用堆内存，一次扫描和处理所有按键状态，带有矩阵键盘和组合的功能。

#### 要点

- 程序默认使用了堆内存，因此要为此分配对空间；
- 使用介绍：[一个小巧的按键处理模块！ (qq.com)](https://mp.weixin.qq.com/s/VGRR7SU0JOKemxEZhBR9Og)

---

### LwBTN

**链接**：[LwBTN latest-develop documentation — LwBTN documentation (majerle.eu)](https://docs.majerle.eu/projects/lwbtn/en/latest/)
**特征**：专业的按键事件管理库。

#### 要点

- 有极为详细的开发文档：[LwBTN latest-develop documentation — LwBTN documentation (majerle.eu)](https://docs.majerle.eu/projects/lwbtn/en/latest/)
- 使用介绍：[一个轻量级的按键管理库！](https://mp.weixin.qq.com/s/MLYz75-7ydv755w4wIP1xQ)

---


## LED

### cotLed

**链接**：[cotLed: 嵌入式设备常用的指示灯控制模块组件代码 (gitee.com)](https://gitee.com/cot_package/cot_led)
**特征**：轻量级的 LED 控制模块，可以实现 LED 灯多种模式状态。

#### 要点

- 现在的芯片内置多种多样的 PWM 控制，用起来效率最高，但比较复杂。这个库适合只有基本的 PWM 控制或想偷懒的时候用，因为估计使用时功耗较高。
- 使用介绍：[轻量级的LED控制模块](https://mp.weixin.qq.com/s/A2arPl2oRYLjFt4STYnljA)

---

### led_module

**链接**：[led_module: 通用的单片机 LED 显示模块，基于嵌入式 C 语言面向对象，采用简单工厂设计模式 (gitee.com)](https://gitee.com/embediot/led_module)
**特征**：基于面向对象和简单工厂模式的通用 LED 显示模块。

#### 要点

- 使用介绍：[基于面向对象和简单工厂模式，设计一个通用的 LED 显示模块。](https://mp.weixin.qq.com/s/AhvTI8-qQHN7eTX6JmpLWA)

---