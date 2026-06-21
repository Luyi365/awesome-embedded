# 日志与终端交互库

> 终端、shell、cli、log 等都有很多名称，这里就将只能输出或用于存储日志的库叫作日志库，而能够输入输出或命令解析的库叫作终端库。

## LOG 日志

> ~~参考：((20230201130407-6jnc3l9 'Log 日志'))~~（待发布）

### dbuglib

![Gitee Repo stars](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/git-lib/dbugLib-Prj&query=$.stargazers_count&style=social&logo=gitee&label=Stars) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/git-lib/dbugLib-Prj&query=$.pushed_at&label=last%20commit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/git-lib/dbugLib-Prj&query=$.license&label=license)

**链接**：[dbugLib Prj: 可移植调试诊断库](https://gitee.com/git-lib/dbugLib-Prj)  
**特征**：精小的的日志库，仅提供输出显示功能，可以修改日志的级别用于过滤特定级别的日志。  

#### 要点

- 使用介绍：[分享一款精小调试支持库！](https://mp.weixin.qq.com/s/V7zp4O51HxQWF_KNOcsZug)

---

### log.c

![GitHub Repo stars](https://img.shields.io/github/stars/rxi/log.c) | ![GitHub last commit](https://img.shields.io/github/last-commit/rxi/log.c) | ![GitHub License](https://img.shields.io/github/license/rxi/log.c)

**链接**：[rxi/log.c: A simple logging library implemented in C99](https://github.com/rxi/log.c)  
**特征**：极简的日志库，仅提供输出显示和记录功能，带有线程锁。  

#### 要点

- 若勾选“<ins>Use MicroLIB</ins>”，编译会显示缺少“time”库。但实际上标准的 time 库是不适用于嵌入式项目的，因此还需要重定向 time 库。
- 所有打印函数都是来源于 `stdio.h`，所以还需要对 printf 类的函数进行重定向。
- 使用介绍：[推荐 | 简单到傻瓜都会用的日志库](https://mp.weixin.qq.com/s/8CvHDWN90iy3GTAr0bV1DA)

---

### log

**链接**：[分享一个小巧的嵌入式日志模块（附代码）](https://mp.weixin.qq.com/s/h4UWFGgGEDS_2Mur1hJygw)  
**特征**：小巧的日志模块，输出内容包括时间、日志类型、内容、文件名、行号、函数名等信息。  

#### 要点

---

### alog

![Gitee Repo stars](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/nikolan/alog&query=$.stargazers_count&style=social&logo=gitee&label=Stars) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/nikolan/alog&query=$.pushed_at&label=last%20commit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/nikolan/alog&query=$.license&label=license)

**链接**：[alog: alog是一个非常精简的串口输出日志组件，类似easyloger，但是比easyloger更简单易用,只有2个实际不到百行的文件，实现了基本日志所需的全部功能。 需移植配置的接口选项少，实现了串口输出字符串就可以用了，没有C库以外的其他依赖。 没有存储日志相关的扩展的API，适合新手使用理解和在资源紧张的单片机上移植使用。](https://gitee.com/nikolan/alog)  
**特征**：功能精简的输出日志组件，带颜色带互斥锁。  

#### 要点

---

### LwPRINTF

![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwprintf) | ![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwprintf) | ![GitHub License](https://img.shields.io/github/license/MaJerle/lwprintf)

**链接**：[LwPRINTF latest-develop documentation — LwPRINTF documentation](https://docs.majerle.eu/projects/lwprintf/en/latest/)  
**特征**：安全简约的标准输出功能库，允许重定向多个输出流，所有 API 均可重入。  

#### 要点

- 使用介绍：[嵌入式开发者必备的轻量级printf库！](https://mp.weixin.qq.com/s/sysPpiZgrPxItv-OpaCVeg)
- 需要用户实现回调函数来定向多个输出流。

---

### EasyLogger

![Gitee Repo stars](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Armink/EasyLogger&query=$.stargazers_count&style=social&logo=gitee&label=Stars) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Armink/EasyLogger&query=$.pushed_at&label=last%20commit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Armink/EasyLogger&query=$.license&label=license)

**链接**：[EasyLogger: 一款超轻量级(ROM<1.6K, RAM<0.3k)、高性能的 C/C++ 日志库](https://gitee.com/Armink/EasyLogger)  
**特征**：功能较全面的日志库，支持动态过滤和颜色选择，注重线程安全，且支持异步输出及缓冲输出模式。  

#### 要点

- 通过自带的 FIle 插件，可以将日志自动保存至文件中。

---

### zlog

![GitHub Repo stars](https://img.shields.io/github/stars/HardySimpson/zlog) | ![GitHub last commit](https://img.shields.io/github/last-commit/HardySimpson/zlog) | ![GitHub License](https://img.shields.io/github/license/HardySimpson/zlog)

**链接**：[zlog library homepage](https://hardysimpson.github.io/zlog/)  
**特征**：是一个高可靠性、高性能、线程安全、灵活、概念清晰的纯 C 日志函数库，不支持内容过滤和解析。  

#### 要点

---

## 终端交互

### cmd-parser

![GitHub Repo stars](https://img.shields.io/github/stars/jiejieTop/cmd-parser) | ![GitHub last commit](https://img.shields.io/github/last-commit/jiejieTop/cmd-parser) | ![GitHub License](https://img.shields.io/github/license/jiejieTop/cmd-parser)

**链接**：[jiejieTop/cmd-parser: 一个非常简单好用的命令解析器，占用资源极少极少，采用哈希算法超快匹配命令！](https://github.com/jiejieTop/cmd-parser)  
**特征**：极简的命令解析库，支持忽略大小写。采用哈希算法，哈希算法为 O(n)。  

#### 要点

- 需要注意，该库长时间没有人维护，且issue反馈很多代码上的问题，还有一篇因Diss写出的[库](https://github.com/PING020903/simpleCmd)，不过命令解析使用哈希算法还是值得学习的。
- 目前只支持 MDK 与 IAR 的编译器，对于 gcc 尚未移植；
- 使用介绍：[cmd-parser | 一个基于哈希匹配的超快命令解析器 - 知乎](https://zhuanlan.zhihu.com/p/141409031)

---

### LwSHELL

![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwshell) | ![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwshell) | ![GitHub License](https://img.shields.io/github/license/MaJerle/lwshell)

**链接**：[LwSHELL latest-develop documentation — LwSHELL documentation](https://docs.majerle.eu/projects/lwshell/en/latest/)  
**特征**：轻量级命令行交互库，简单易用，附带命令描述。  

#### 要点

- 带有 cmd -v 选项的简单帮助文本。

---

### debugcmd

![Gitee Repo stars](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/mazcpnt/debugcmd&query=$.stargazers_count&style=social&logo=gitee&label=Stars) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/mazcpnt/debugcmd&query=$.pushed_at&label=last%20commit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/mazcpnt/debugcmd&query=$.license&label=license)

**链接**：[debugcmd: 【稳定版】灵活好用的调试命令接口](https://gitee.com/mazcpnt/debugcmd)  
**特征**：功能完善的命令行解析库，提供Tab补全、帮助查看、子命令注册等功能。  

#### 要点

---

### Argtable3

![GitHub Repo stars](https://img.shields.io/github/stars/argtable/argtable3) | ![GitHub last commit](https://img.shields.io/github/last-commit/argtable/argtable3) | ![GitHub License](https://img.shields.io/github/license/argtable/argtable3)

**链接**：[Argtable.org](https://www.argtable.org/)  
**特征**：规范的命令行解析库，用于自定义操作命令，遵循 POSIX 接口。  

#### 要点

---

### nr\_micro\_shell

![Gitee Repo stars](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/nrush/nr_micro_shell&query=$.stargazers_count&style=social&logo=gitee&label=Stars) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/nrush/nr_micro_shell&query=$.pushed_at&label=last%20commit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/nrush/nr_micro_shell&query=$.license&label=license)

**链接**：[nr_micro_shell: shell for MCU. 单片机命令行交互。](https://gitee.com/nrush/nr_micro_shell)  
**特征**：标准的命令行交互库，提供 Tab 键命令补全，查询历史命令等功能，原生支持 ENV 工具使用。  

#### 要点

- 不支持 ESC 键等控制键（控制符）。
- 使用介绍：[shell for MCU，单片机命令行交互](https://mp.weixin.qq.com/s/13Oj49ll_hcLQbqfBPtG-Q)

---

### letter shell

![GitHub Repo stars](https://img.shields.io/github/stars/NevermindZZT/letter-shell) | ![GitHub last commit](https://img.shields.io/github/last-commit/NevermindZZT/letter-shell) | ![GitHub License](https://img.shields.io/github/license/NevermindZZT/letter-shell)

**链接**：[NevermindZZT/letter-shell: letter shell](https://github.com/NevermindZZT/letter-shell)  
**特征**：功能强大的嵌入式命令行交互库，几乎提供 shell 拥有的所有功能，且能通过函数地址直接执行函数。  

#### 要点

---

### Xradio\_console

![GitHub Repo stars](https://img.shields.io/github/stars/XradioTech/xradio-skylark-sdk) | ![GitHub last commit](https://img.shields.io/github/last-commit/XradioTech/xradio-skylark-sdk?path=src%2Fconsole) | ![GitHub License](https://img.shields.io/github/license/XradioTech/xradio-skylark-sdk)

**链接**：[xradio-skylark-sdk/src/console at master · XradioTech/xradio-skylark-sdk](https://github.com/XradioTech/xradio-skylark-sdk/tree/master/src/console)、[xradio-skylark-sdk/include/console at master · XradioTech/xradio-skylark-sdk](https://github.com/XradioTech/xradio-skylark-sdk/tree/master/include/console)  
**特征**：Xradio SDK 里提取的控制台库，命令采用分层结构，适合有多命令的时候，基于 RTOS。  

#### 要点

- 命令示例：[xradio-skylark-sdk/project/common/cmd at master · XradioTech/xradio-skylark-sdk](https://github.com/XradioTech/xradio-skylark-sdk/tree/master/project/common/cmd)；
- Demo（common 文件）：[xradio-skylark-sdk/project/demo/hello_demo at master · XradioTech/xradio-skylark-sdk](https://github.com/XradioTech/xradio-skylark-sdk/tree/master/project/demo/hello_demo)；
- 还有一些依赖库基于 SDK 里的其他文件；
- 参考：[【XR806 开发板试用】Console 流程解析以及添加自定义指令 - 极术社区 - 连接开发者与智能计算生态](https://aijishu.com/a/1060000000288360)；
- 其中文件 `cmd_util` 里的 API：
  - `cmd_main_exec`：主命令集，也就是最外层命令
  - `cmd_exec`：子命令集
  - `cmd_help_exec`：显示当前层的"help"
  - `cmd2`：代表该命令可以接收多个参数
- 文件夹 `cmd` 里的命令都是子命令，使用前需要先定义子命令，像 demo 一样；

---

### easyShell

![Gitee Repo stars](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/gzbkey/easyShell&query=$.stargazers_count&style=social&logo=gitee&label=Stars) | ![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/gzbkey/easyShell&query=$.pushed_at&label=last%20commit) | ![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/gzbkey/easyShell&query=$.license&label=license)

**链接**：[easyShell: A simple microcontroller shell.一个简单易用的单片机shell。](https://gitee.com/gzbkey/easyShell)  
**特征**：简单易用的单片机shell，支持tab补全。  

#### 要点

---