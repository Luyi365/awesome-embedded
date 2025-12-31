# UI与菜单库

> 参考：((20230811124459-5041le3 '何为渲染？'))
>
> 另外，很多菜单框架会联系上 UI 来做，所以将这两种类型的库放在一起。

## HMI

> 对于少量图片、文字，完全可以采用<u>图片取模</u>的方式生成数组，然后给到源驱动函数中使用。
>
> 该网站提供[图像转编码](https://projedefteri.com/en/tools/lcd-assistant/)和[字符编辑器](https://projedefteri.com/en/tools/lcd-character-generator/)。

### tslib

**链接**：[libts/tslib: Touchscreen access library (github.com)](https://github.com/libts/tslib)
**特征**：嵌入式中使用最广泛的电阻触摸屏校正算法库，但好像只能用在 Linux 上。

#### 要点

---

### tslib\_for\_mcu

**链接**：[wujique/tslib_for_mcu: 整理裁剪一个 tslib 用于单片机平台，例程基于 STM32 (github.com)](https://github.com/wujique/tslib_for_mcu)
**特征**：linux 下裁剪的一个电阻屏触摸校准库。

#### 要点

---


## 单色

> 要想在单色屏上显示灰度效果，可以已知两种方式：PWM 原理和抖动算法。

### ECBM\_GUI

**链接**：[ECBM 工作室/ECBM_GUI - 码云 - 开源中国 (gitee.com)](https://gitee.com/ecbm/ecbm_gui)
**特征**：超基础的单色 GUI 库，仅通过内建缓存来存放画面内容实现 GUI 功能。

#### 要点

---

### SimpleGUI

**链接**：[SimpleGUI: 一个面向单色显示屏的开源 GUI 接口库。 (gitee.com)](https://gitee.com/Polarix/simplegui)
**特征**：针对单色显示屏设计的 GUI 库，提供简单的绘制功能。

#### 要点

---

### U8g2

**链接**：[GitHub - olikraus/u8g2: U8glib library for monochrome displays, version 2](https://github.com/olikraus/u8g2)
**特征**：单色显示器库，提供多种控制器支持和基本图形绘制。

#### 要点

---

### MonoGUI

**链接**：[MonoGUI: MonoGUI （黑白图形用户接口系统）是针对电子词典、高级计算器、电子手表、标签打印机、收款机、电子货签等具有黑白屏幕的小电子设备开发的专用 GUI 系统。本系统具有结构简单、使用容易、内存占用小、单线程、处理器负担轻等特点。虽然图形能力仅有黑与白，但其支持完整的中文显示处理功能（GB18030 中 2 字节汉字，即旧 GB13000 标准），其 Edit 控件和中文输入法（包括九键输入法）功能上达到 Windows 和 Android 的输入法水平，且扩展容易。 (gitee.com)](https://gitee.com/liuxinouc/MonoGUI)
**特征**：针对黑白屏幕的小电子设备开发的专用 GUI 系统，功能全面，附带输入法功能。

#### 要点

---

### WouoUI

**链接**：[GitHub - RQNG/WouoUI: 模仿稚晖君 MonoUI 风格的超丝滑菜单，使用 EC11 旋转编码器控制。](https://github.com/RQNG/WouoUI)
**特征**：模仿自稚晖君暂未开源的 MonoUI，用于实现类似 UltraLink 的丝滑界面，使用编码器作为控制器，还有个特流畅好看的升级版。

#### 要点

- 升级版：[GitHub - RQNG/WOW-OS: 简易的拖影风格多级菜单系统，满足小设备功能设置和展示的基本需求](https://github.com/RQNG/WOW-OS)；

---

### astra UI

**链接**：[GitHub - AstraThreshold/oled-ui-astra: A smooth, easy-to-deploy, and easy-to-extend OLED UI framework, based on C++.](https://github.com/AstraThreshold/oled-ui-astra)
**特征**：基于 C++ 的 OLED 多级菜单 UI，带有丝滑的过渡动画效果。

#### 要点

---

### GLCD

**链接**：[andygock/glcd：基于微控制器嵌入式系统的图形 LCD 库。兼容 PCD854、ST7565R、NTD75451 以及许多 AVR、LPC、PIC、STM32 设备。 --- andygock/glcd: Graphic LCD Library for microcontrollers based embedded systems. Compatible with chipsets PCD854, ST7565R, NTD75451 and many AVR, LPC, PIC, STM32 devices.](https://github.com/andygock/glcd)
**特征**：微控制器嵌入式系统图形 LCD 库，包含硬件驱动、文本及基础图形绘制。

#### 要点

- 由于涉及硬件驱动，因此对设备选型有一定要求，但也可以自己修改接口来适配设备；

---


## 彩色

### GuiLite

**链接**：[idea4good/GuiLite: ✔️The smallest header-only GUI library(4 KLOC) for all platforms (github.com)](https://github.com/idea4good/GuiLite)
**特征**：超轻量级 GUI 库，支持多平台，支持第三方库。

#### 要点

- 使用介绍：[STM32 | GuiLite 初体验 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/494786697)

---

### Olive.c

**链接**：[tsoding/olive.c: Simple 2D Graphics Library for C (github.com)](https://github.com/tsoding/olive.c/tree/master)
**特征**：适用于 C 语言的简单 2D 图形库，仅使用画布特征进行绘制。

#### 要点

---

### microui

**链接**：[rxi/microui: A tiny immediate-mode UI library (github.com)](https://github.com/rxi/microui)
**特征**：一个微小而便携的 UI 库，其特点是占用极少的内存空间，适用于任何可以绘制矩形和文本的渲染系统。

#### 要点

---

### LingLongGUI

**链接**：[LingLongGUI: 玲珑 GUI 是高效的界面开发解决方案。 代替串口屏、组态，降低产品成本，产品软硬件自主可控。 配套界面开发软件，图形化编辑界面，生成 C 代码。 (gitee.com)](https://gitee.com/gzbkey/LingLongGUI)
**特征**：高效的 GUI 生成库，配套有图形化编辑界面，方便之间生成代码使用。

#### 要点

- 教程：[玲珑 GUI 教程 (yuque.com)](https://www.yuque.com/gzbkey/ag59k9?)

---

### LingDongGUI

**链接**：[LingDongGUI: 灵动 GUI 是基于 ARM-2D 进行开发的 GUI，极大降低 ARM-2D 的使用难度](https://gitee.com/gzbkey/LingDongGUI)
**特征**：对 ((20230812185114-y5t0g6r 'Arm-2D')) 进行二次封装的 GUI 库，旨在提高易用性，同时也支持原生 API 的使用。

#### 要点

- 提供原生上位机支持：((20250911130644-rmpmeww 'GuiEasyEditor'))

---

### AAGUI

**链接**：[AAGUI: AAGUI 是一个不依赖特定硬件、操作系统的跨平台通用型半声明式 GUI。采用 C(兼容 C89)与 C++(兼容 C++98)编写。 (gitee.com)](https://gitee.com/QQ1159465634/aagui)
**特征**：跨平台通用型 GUI，旨在嵌入式里实现类安卓的高级 UI 开发。可使用半声明式（json）编程，适合类似于手机应用的项目开发。

#### 要点

- 由于跨平台特点，可以直接在 PC 上开发后移植到 MCU 端；

---

### GT-HMI

**链接**：[GT-HMI-Engine: GT-HMI ：专为国内嵌入式 GUI 设计开发打造的免费神器！ (gitee.com)](https://gitee.com/genitop/GT-HMI-Engine)
**特征**：高通旗下专为国人使用的 UI 库，带有多种语种多字库，带有模拟器和上位机。RTOS、裸机均可使用，适合实用的项目级产品。

#### 要点

---

### LVGL

**链接**：[LVGL - Light and Versatile Embedded Graphics Library](https://lvgl.io/)
**特征**：轻量级通用图形库，开源免费，几乎拥有 GUI 所需的一切。

#### 要点

- 参考：((20230129205449-88dk4cv 'LVGL'))
- [LVGL 的多语言转换工具--MCU_Font_Release](https://aijishu.com/a/1060000000297013)
- NXP 旗下的免费图形化编辑器：[GUI Guider | NXP 半导体](https://www.nxp.com.cn/design/design-center/software/development-software/gui-guider:GUI-GUIDER)
- lvgl 图形化编辑器：[SquareLine Studio - Design and build UIs with ease](https://squareline.io/)
- 开源的 LVGL 界面编辑器：[CURTLab/LVGLBuilder: GUI Builder for littlevgl. (github.com)](https://github.com/CURTLab/LVGLBuilder)

---

### AWTK

**链接**：[zlgopen/awtk: AWTK = Toolkit AnyWhere(a cross-platform embedded GUI) (github.com)](https://github.com/zlgopen/awtk)
**特征**：周立功旗下的 GUI 图形库，开源免费。

#### 要点

- 参考：((20230129205449-zdv5owi 'AWTK'))

---

### TouchGFX

**链接**：[STM32 Graphical User Interface - 意法半导体 STMicroelectronics](https://www.touchgfx.com/)
**特征**：STM32 旗下的 GUI 图形库，功能强劲，配有图形编辑软件，一般只适用于 STM32 的开发。

#### 要点

---

### **GUIX**

**链接**：[azure-rtos/guix: Azure RTOS GUIX Studio provides a complete, embedded graphical user interface (GUI) library and design environment, facilitating the creation and maintenance of all graphical elements needed by your device. (github.com)](https://github.com/azure-rtos/guix)
**特征**：Azure RTOS 提供的 GUI 图形库，开发十分成熟和方便，开源免费。

#### 要点

- 可以看安富莱的教程。

---

### **emWin**

**链接**：[emWin (segger.com)](https://www.segger.com/products/user-interface/emwin/)
**特征**：又名(uCGUI)，是 Segger 旗下的 GUI 图形库，很多知名大厂芯片都是可以授权使用的。

#### 要点

- 可以看安富莱和野火的教程。

---

### **Embedded Wizard GUI**

**链接**：[Simplify Your GUI Development - Embedded Wizard (embedded-wizard.de)](https://www.embedded-wizard.de/)
**特征**：超强大的 GUI 图形库，但需要收钱。配有图形化编辑器。

#### 要点

---

### Qt for MCU

**链接**：[Qt - 设计、开发嵌入式设备软件](https://www.qt.io/zh-cn/product/develop-embedded-devices)
**特征**：QT 旗下的 GUI 图形库，适合有 QT 经验的开发者，需要收费。

#### 要点

---

### μGFX

**链接**：[uGFX - lightweight embedded GUI library](https://ugfx.io/)
**特征**：可用于触摸屏的轻量级UI库，注重性能，非商用免费。

#### 要点

- 原先还提供名为“uGFX Studio”的布局上位机，但目前官网已经看不到该工具了，不清楚后续是否还会提供；

---

### MiniGUI

**链接**：[Home :: MiniGUI](https://minigui.com)
**特征**：多平台、高度可定制的UI库，可用于不同性能的芯片，适合移动设备及工业等领域，非商用免费。

#### 要点

---

### **μGUI**

**链接**：[μGUI - free Open Source GUI module for embedded systems | Embedded Lightning](http://embeddedlightning.com/ugui/)
**特征**：开源的极简图形库，独立于平台，仅一个源文件。

#### 要点

---

### Aeropoint GUI

**链接**：[CRI Aeropoint GUI - CRI Middleware (cri-mw.co.jp)](https://www.cri-mw.co.jp/business/product/embedded/aeropointgui/)
**特征**：使用 PPT 方式进行 GUI 的创建，需要收费，且没有试用版。

#### 要点

---

### Clay

**链接**：[Clay - UI Layout Library](https://www.nicbarker.com/clay)
**特征**：高性能 2D UI 布局库，提供响应式布局能力，适合嵌入式 Web 的制作。

#### 要点

---

### Nuklear

**链接**：[Nuklear: Nuklear](https://immediate-mode-ui.github.io/Nuklear/index.html)
**特征**：无依赖的图形用户界面工具包，通过使用输入状态和绘制命令来构建图形，适合快速响应的应用。

#### 要点

- 由于该库不提供平台支持，在嵌入式上使用时需要自己接入渲染层；

---

### LinaVG

**链接**：[inanevin/LinaVG: 2D Vector-Graphics library for drawing anti-aliased convex shapes, lines and texts. (github.com)](https://github.com/inanevin/LinaVG)
**特征**：适用于 2D 矢量图形的渲染库。

#### 要点

---

### BlurHash

**链接**：[BlurHash](https://blurha.sh/)
**特征**：开源的图片占位符算法和实现，能够在图片预载时先显示框图和缩略图，嵌入式领域可能会用得到。

#### 要点

---

### OpenGL

**链接**：[OpenGL - 高性能图形的行业标准](https://www.opengl.org/)
**特征**：跨语言、跨平台的 2D/3D 渲染库，主要使用 C 语言开发，但也可以支持 C++、Python、Java 等语言开发，功能极其强大，适合游戏开发、科学可视化、虚拟现实等领域。

#### 要点

- OpenGL ES：是 OpenGL 的子集，专注于嵌入式及移动端的图形渲染；

  - WebGL：基于 OpenGL ES 的图形接口，但加入了 JavaScript 语言，专注于 Web 网页的渲染开发；

---

### Rawdraw

**链接**：[cntools/rawdraw: Primitive Platform Agnostic Graphics Library](https://github.com/cntools/rawdraw)
**特征**：跨平台无依赖的 UI 绘制系统，为 OpenGL 提供良好的接口抽象。

#### 要点

---

### TinyGL

**链接**：[TinyGL : a Small, Free and Fast Subset of OpenGL*](https://bellard.org/TinyGL/)
**特征**：是 ((20241028095609-ueqg612 'OpenGL')) 的一个小型实现，适用于嵌入式系统。将复杂的接口精简为更易于理解和操作的形式。

#### 要点

---

### foolrenderer

**链接**：[cadenji/foolrenderer: A tiny software renderer implemented from scratch without the use of graphics API, used to understand how GPUs work. (github.com)](https://github.com/cadenji/foolrenderer/tree/main)
**特征**：用 C 语言实现的软件渲染器，不依赖图形库，仅用几千行代码，实现了一套类似 OpenGL 的基本图形功能，以及应用于游戏开发的实时渲染技术，如阴影、切线空间法线映射、基于物理的材质系统等。

#### 要点

- 由于是基于 PC 平台，移植到嵌入式里使用需要稍微改改；

---

### EmberGL

**链接**：[EmberGL-org/EmberGL: EmberGL - 2D/3D graphics library featuring a tiled software rasterizer. (github.com)](https://github.com/EmberGL-org/EmberGL)
**特征**：用于 MCU 的类似于 OpenGL 的实时 2D / 3D 光栅渲染库。

#### 要点

---


## 加速

### Arm-2D

**链接**：[ARM-software/Arm-2D: 2D Graphic Library optimized for Cortex-M processors (github.com)](https://github.com/ARM-software/Arm-2D)
**特征**：针对 Cortex-M 处理器优化的 2D 图形加速库，处于 GUI 库和驱动层之间。

#### 要点

- 使用介绍：[#Arm-2D (qq.com)](https://mp.weixin.qq.com/mp/appmsgalbum?action=getalbum&__biz=MzAxMzc2ODMzNg==&scene=1&album_id=1842127987152896001&count=3&from=industrynews&version=4.1.27.6032&platform=win#wechat_redirect)
- 提供 CMSIS-Pack。

---

### GUIslice

**链接**：[GUIslice: Touchscreen GUI in C for Raspberry Pi & Arduino - ImpulseAdventure](https://www.impulseadventure.com/elec/guislice-gui.html)
**特征**：简单好用的开源GUI框架，极客的风格，无动态内存分配，并提供布局上位机。

#### 要点

---


## 图形

### qrencode

**链接**：[qrencode: 用 C 语言生成二维码的演示代码 (gitee.com)](https://gitee.com/kerndev/qrencode)
**特征**：二维码生成库，适用于单片机。

#### 要点

---

### QR Code generator library

**C库链接**：[QR-Code-generator/c at master · nayuki/QR-Code-generator](https://github.com/nayuki/QR-Code-generator/tree/master/c)
**C++库链接**：[QR-Code-generator/cpp at master · nayuki/QR-Code-generator](https://github.com/nayuki/QR-Code-generator/tree/master/cpp)
**特征**：通用的QR码生成库，包含多个语言版本，旨在用更少的代码实现更好的性能。

#### 要点

- Web端演示及竞品分析：[QR Code generator library](https://www.nayuki.io/page/qr-code-generator-library)

---

### QRCode

**链接**：[ricmoo/QRCode: QR code generation library in C, optimized for low-power devices, such as Arduino.](https://github.com/ricmoo/QRCode)
**特征**：QR码生成库，参考了((20251105131018-mfpyp7w 'QR Code generator library'))，并针对处理器和内存受限的系统进行了优化，支持从 Version 1 到 Version 40 的所有规格。

#### 要点

- 使用介绍：[嵌入式系统中的极简二维码生成方案！](https://mp.weixin.qq.com/s/HXGs1TSmQDFNYP4pSAATsQ)

---

### oledlib

**链接**：[oledlib: 一个开源的 oled 图形库，使用 32 单片机 keil 平台进行开发，支持 I2C 和 SPI 驱动，能够绘制矩形，圆，椭圆，多边形，图片文字等简单内容 (gitee.com)](https://gitee.com/jiezhuonew/oledlib)
**特征**：一个开源的 oled 图形库，带有一些适合做屏保的图形。

#### 要点

---


## 字形

### MCUFont

**链接**：[mcufont/mcufont: A font rendering library for microcontrollers. (github.com)](https://github.com/mcufont/mcufont)
**特征**：专用于字体的库，实现字体压缩、解压缩和文本渲染（调节）功能。

#### 要点

---

### Unicorn

**链接**：[Unicorn: Embeddable Unicode® Algorithms | Railgun](https://railgunlabs.com/unicorn/)
**特征**：基于 C99 的 Unicode 编解码库，提供对此编码的基本算法和功能。

#### 要点

---


## 多媒体

### FFmpeg

**链接**：[FFmpeg](https://ffmpeg.org//)
**特征**：业界极为知名的一个跨平台音视频处理框架，提供一组音视频编解码开发套件。

#### 要点

- 开发套件包含但不限于：

  **[libavutil](https://ffmpeg.org//libavutil.html)** 是一个包含函数的库 简化编程，包括随机数生成器、数据 结构、数学例程、核心多媒体实用程序等等 更多。

  **[libavcodec](https://ffmpeg.org//libavcodec.html)** 是一个包含解码器和编码器的库 用于音频/视频编解码器。

  **[libav 格式](https://ffmpeg.org//libavformat.html)**是一个包含多路复用器的库，并且 多媒体容器格式的多路复用器。

  **[libavdevice](https://ffmpeg.org//libavdevice.html)** 是一个包含输入和输出的库 用于抓取和渲染到许多常见多媒体的设备 输入/输出软件框架，包括 Video4Linux、Video4Linux2、 VfW 和 ALSA.

  **[libavfilter](https://ffmpeg.org//libavfilter.html)** 是一个包含媒体过滤器的库。

  **[libswscale](https://ffmpeg.org//libswscale.html)** 是一个执行高度优化图像的库 缩放和色彩空间/像素格式转换操作。

  **[libswresample](https://ffmpeg.org//libswresample.html)** 是一个执行高度优化的库 音频重采样、重矩阵化和样本格式转换操作。
- 使用介绍：[ffmpeg-libav-tutorial/README-cn.md at master · leandromoreira/ffmpeg-libav-tutorial](https://github.com/leandromoreira/ffmpeg-libav-tutorial/blob/master/README-cn.md)

---


## 菜单框架

### zBitsView

**链接**：[figght/zBitsView (github.com)](https://github.com/figght/zBitsView)
**特征**：虚拟多层菜单，仅存在于逻辑层，与有无屏幕无关。

#### 要点

---

### emenu

**链接**：[PetiteDrv/components/emenu at master · wujique/PetiteDrv (github.com)](https://github.com/wujique/PetiteDrv/tree/master/components/emenu)
**特征**：不寻常的菜单框架，在代码上就可以反映菜单结构。

#### 要点

- 使用介绍：[实用 | 一个简单易用的菜单框架](https://mp.weixin.qq.com/s/1rC6vkRqlwsXLMq-JhlGYA)

---

### Menu

**链接**：[简易实用的菜单框架 - 代码片段 - Gitee.com](https://gitee.com/Luyi365/codes/kg3qocwb2r57m1anjsxdl95)
**特征**：简单实用的菜单框架，适合在公司小型项目上使用。

#### 要点

- 使用介绍：[完全由 C 编写，高度可移植，超级牛逼的菜单架构！](https://mp.weixin.qq.com/s/Z7OmHJaI-Ffz71f-QTmCnQ)

---

### cotMenu

**链接**：[cotMenu: 嵌入式设备常用的菜单框架模块组件代码（轻量级） (gitee.com)](https://gitee.com/cot_package/cot_menu#https://gitee.com/link?target=https%3A%2F%2Fblog.csdn.net%2Fqq_24130227%2Farticle%2Fdetails%2F121167276%3Fcsdn_share_tail%3D%257B%2522type%2522%253A%2522blog%2522%252C%2522rType%2522%253A%2522article%2522%252C%2522rId%2522%253A%2522121167276%2522%252C%2522source%2522%253A%2522qq_24130227%2522%257D%26ctrtid%3DVbyfV)
**特征**：采用链表方式实现多级深度菜单，相当于显示的逻辑层，与按键、显示屏完全解耦。

#### 要点

- 使用介绍：[轻量级多级菜单控制框架（C 语言）](https://mp.weixin.qq.com/s/NwVfvWY5OscDOgfwBqwcAA)

---

### MiaoUI

**链接**：[GitHub - JFeng-Z/MiaoUI: MiaoUI 是一个基于 u8g2 的单色 OLED 菜单 UI 框架。MiaoUI 使用 C 语言实现，采用双向链表结构，使用非线性动画、移植方便、内存占用较小、能够快速部署，适用于具有小型 OLED 屏幕的嵌入式设备。](https://github.com/JFeng-Z/MiaoUI)
**特征**：基于 ((20250216001136-52a1lbo "U8g2")) 的 OLED 菜单 UI 框架，支持列表与图标类菜单、非线性动画、任务弹窗等功能。

#### 要点

---

### MultMenu

**链接**：[GitHub - JFeng-Z/MultMenu: 这是一个用于单色 OLED 屏幕的单片机多级菜单。支持菜单扩展、图形界面、文本界面、调参、功能调用，全局使用非线性动画，动画可打断。](https://github.com/JFeng-Z/MultMenu)
**特征**：多级菜单 + 单色 OLED 非线性动画库，组合使用，移植简单方便，适合类似需求的创客项目。

#### 要点

---

### SMF

**链接**：[SMF-1.0.zip](assets/SMF-1.0-20231024190735-uw9r3ks.zip)
**特征**：基于 C++ 的菜单框架，提供多级菜单、菜单对象，适合项目级工程。

#### 要点

- 使用介绍：[软件 | 一个简单易用的菜单框架 (qq.com)](https://mp.weixin.qq.com/s/hqisQUgKoQNHkTXNokUipw)

---

### PageManager

**链接**：[X-TRACK/Software/X-Track/USER/App/Utils/PageManager at main · FASTSHIFT/X-TRACK (github.com)](https://github.com/FASTSHIFT/X-TRACK/tree/main/Software/X-Track/USER/App/Utils/PageManager)
**特征**：基于 C++ 的页面生命周期管理库，提供完整的页面调度功能，适合项目级工程。

#### 要点

---