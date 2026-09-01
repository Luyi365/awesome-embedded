# Logging and Terminal Interaction Library
<!-- i18n:language-selector:start -->
[中文](README.md) | **English**
<!-- i18n:language-selector:end -->

> Terminals, shells, CLIs, logs, and similar tools have many names. Here, libraries that can only output or store logs are called logging libraries, while libraries that can accept input and output or parse commands are called terminal libraries.

## LOG Logging

> ~~Reference: ((20230201130407-6jnc3l9 'Log Logging'))~~ (pending release)

### dbuglib

[![Gitee Repo stars](https://gitee.com/git-lib/dbugLib-Prj/badge/star.svg?theme=gvp)](https://gitee.com/git-lib/dbugLib-Prj/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/git-lib/dbugLib-Prj&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/git-lib/dbugLib-Prj&query=$.license&label=license)]()

**Link** - [dbugLib Prj: Portable debug diagnostic library](https://gitee.com/git-lib/dbugLib-Prj)  
**Features** - A compact logging library that only provides output display and can adjust log levels to filter logs at specified levels, equivalent to the printf functionality that generic SDKs include;  

#### Key Points

- Introduction: [Sharing a Compact Debug Support Library!](https://mp.weixin.qq.com/s/V7zp4O51HxQWF_KNOcsZug)

---

### log.c

[![GitHub Repo stars](https://img.shields.io/github/stars/rxi/log.c)](https://github.com/rxi/log.c/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/rxi/log.c)](https://github.com/rxi/log.c/commits) | [![GitHub License](https://img.shields.io/github/license/rxi/log.c)]()

**Link** - [rxi/log.c: A simple logging library implemented in C99](https://github.com/rxi/log.c)  
**Features** - A minimalist logging library that only provides output display and recording. Based on the C99 standard, it is not well suited to the embedded field.  

#### Key Points

- If “<ins>Use MicroLIB</ins>” is selected, compilation reports that the “time” library is missing. The standard time library is not suitable for embedded projects, however, so the time library must also be redirected.
- All print functions come from `stdio.h`, so printf-like functions must also be redirected.
- Introduction: [Recommended | A Logging Library So Simple Anyone Can Use It](https://mp.weixin.qq.com/s/8CvHDWN90iy3GTAr0bV1DA)

---

### log

**Link** - [Sharing a Compact Embedded Logging Module (with Code)](https://mp.weixin.qq.com/s/h4UWFGgGEDS_2Mur1hJygw)  
**Features** - A compact logging module whose output includes the time, log type, content, file name, line number, function name, and other information.  

#### Key Points

---

### alog

[![Gitee Repo stars](https://gitee.com/nikolan/alog/badge/star.svg?theme=gvp)](https://gitee.com/nikolan/alog/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/nikolan/alog&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/nikolan/alog&query=$.license&label=license)]()

**Link** - [alog: alog is a highly streamlined serial-output logging component, similar to easyloger but simpler and easier to use. With only two files of fewer than one hundred lines each, it implements all functions required for basic logging. It has few interfaces and options requiring porting configuration; once serial string output is implemented, it is ready to use. It has no dependencies beyond the C library and no extended APIs for log storage. It is suitable for beginners to understand and port to resource-constrained microcontrollers.](https://gitee.com/nikolan/alog)  
**Features** - A streamlined output logging component with color and mutex locking.  

#### Key Points

---

### LwPRINTF

[![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwprintf)](https://github.com/MaJerle/lwprintf/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwprintf)](https://github.com/MaJerle/lwprintf/commits) | [![GitHub License](https://img.shields.io/github/license/MaJerle/lwprintf)]()

**Link** - [LwPRINTF latest-develop documentation — LwPRINTF documentation](https://docs.majerle.eu/projects/lwprintf/en/latest/)  
**Features** - A safe, concise standard-output utility library that allows multiple output streams to be redirected; all APIs are reentrant.  

#### Key Points

- Introduction: [A Must-Have Lightweight printf Library for Embedded Developers!](https://mp.weixin.qq.com/s/sysPpiZgrPxItv-OpaCVeg)
- Users need to implement callback functions to direct multiple output streams.

---

### EasyLogger

[![Gitee Repo stars](https://gitee.com/Armink/EasyLogger/badge/star.svg?theme=gvp)](https://gitee.com/Armink/EasyLogger/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Armink/EasyLogger&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/Armink/EasyLogger&query=$.license&label=license)]()

**Link** - [EasyLogger: An ultra-lightweight (ROM<1.6K, RAM<0.3k), high-performance C/C++ logging library](https://gitee.com/Armink/EasyLogger)  
**Features** - A relatively comprehensive logging library supporting dynamic filtering and color selection. It emphasizes thread safety and supports asynchronous and buffered output modes.  

#### Key Points

- With the bundled FIle plugin, logs can be automatically saved to files.

---

### zlog

[![GitHub Repo stars](https://img.shields.io/github/stars/HardySimpson/zlog)](https://github.com/HardySimpson/zlog/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/HardySimpson/zlog)](https://github.com/HardySimpson/zlog/commits) | [![GitHub License](https://img.shields.io/github/license/HardySimpson/zlog)]()

**Link** - [zlog library homepage](https://hardysimpson.github.io/zlog/)  
**Features** - A pure C logging function library that is highly reliable, high-performance, thread-safe, flexible, and conceptually clear; it does not support content filtering or parsing.  

#### Key Points

---

## Terminal Interaction

### cmd-parser

[![GitHub Repo stars](https://img.shields.io/github/stars/jiejieTop/cmd-parser)](https://github.com/jiejieTop/cmd-parser/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/jiejieTop/cmd-parser)](https://github.com/jiejieTop/cmd-parser/commits) | [![GitHub License](https://img.shields.io/github/license/jiejieTop/cmd-parser)]()

**Link** - [jiejieTop/cmd-parser: A very simple and easy-to-use command parser that uses extremely few resources and a hash algorithm to match commands very quickly!](https://github.com/jiejieTop/cmd-parser)  
**Features** - A minimalist command-parsing library that triggers functions through strings, which is a pretty interesting approach.  

#### Key Points

- Note that this library has not been maintained for a long time, and its issues report many code problems. There is also a [library](https://github.com/PING020903/simpleCmd) written in response, but using a hash algorithm for command parsing is still worth studying.
- Currently supports only MDK and IAR compilers; it has not yet been ported to gcc;
- Introduction: [cmd-parser | An Ultra-Fast Command Parser Based on Hash Matching - Zhihu](https://zhuanlan.zhihu.com/p/141409031)

---

### LwSHELL

[![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwshell)](https://github.com/MaJerle/lwshell/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwshell)](https://github.com/MaJerle/lwshell/commits) | [![GitHub License](https://img.shields.io/github/license/MaJerle/lwshell)]()

**Link** - [LwSHELL latest-develop documentation — LwSHELL documentation](https://docs.majerle.eu/projects/lwshell/en/latest/)  
**Features** - A lightweight shell library that is simple and easy to use and includes command descriptions.  

#### Key Points

- Includes simple help text with the `cmd -v` option.

---

### debugcmd

[![Gitee Repo stars](https://gitee.com/mazcpnt/debugcmd/badge/star.svg?theme=gvp)](https://gitee.com/mazcpnt/debugcmd/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/mazcpnt/debugcmd&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/mazcpnt/debugcmd&query=$.license&label=license)]()

**Link** - [debugcmd: \[Stable Version\] Flexible and Easy-to-Use Debug Command Interface](https://gitee.com/mazcpnt/debugcmd)  
**Features** - A feature-complete command-line parsing library providing Tab completion, help viewing, subcommand registration, and other functions.  

#### Key Points

---

### Argtable3

[![GitHub Repo stars](https://img.shields.io/github/stars/argtable/argtable3)](https://github.com/argtable/argtable3/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/argtable/argtable3)](https://github.com/argtable/argtable3/commits) | [![GitHub License](https://img.shields.io/github/license/argtable/argtable3)]()

**Link** - [Argtable.org](https://www.argtable.org/)  
**Features** - A standardized command-line parsing library for custom operation commands that follows the POSIX interface.  

#### Key Points

---

### nr\_micro\_shell

[![Gitee Repo stars](https://gitee.com/nrush/nr_micro_shell/badge/star.svg?theme=gvp)](https://gitee.com/nrush/nr_micro_shell/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/nrush/nr_micro_shell&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/nrush/nr_micro_shell&query=$.license&label=license)]()

**Link** - [nr_micro_shell: shell for MCU. Microcontroller command-line interaction.](https://gitee.com/nrush/nr_micro_shell)  
**Features** - A standard command-line interaction library that provides Tab command completion and command history lookup, with native support for ENV tools.  

#### Key Points

- Does not support control keys such as ESC (control characters).
- Introduction: [shell for MCU, Microcontroller Command-Line Interaction](https://mp.weixin.qq.com/s/13Oj49ll_hcLQbqfBPtG-Q)

---

### letter shell

[![GitHub Repo stars](https://img.shields.io/github/stars/NevermindZZT/letter-shell)](https://github.com/NevermindZZT/letter-shell/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/NevermindZZT/letter-shell)](https://github.com/NevermindZZT/letter-shell/commits) | [![GitHub License](https://img.shields.io/github/license/NevermindZZT/letter-shell)]()

**Link** - [NevermindZZT/letter-shell: letter shell](https://github.com/NevermindZZT/letter-shell)  
**Features** - A powerful embedded command-line interaction library providing nearly all shell functions and allowing functions to be executed directly through function addresses.  

#### Key Points

---

### Xradio\_console

[![GitHub Repo stars](https://img.shields.io/github/stars/XradioTech/xradio-skylark-sdk)](https://github.com/XradioTech/xradio-skylark-sdk/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/XradioTech/xradio-skylark-sdk?path=src/console)](https://github.com/XradioTech/xradio-skylark-sdk/commits) | [![GitHub License](https://img.shields.io/github/license/XradioTech/xradio-skylark-sdk)]()

**Link** - [xradio-skylark-sdk/src/console at master · XradioTech/xradio-skylark-sdk](https://github.com/XradioTech/xradio-skylark-sdk/tree/master/src/console)、[xradio-skylark-sdk/include/console at master · XradioTech/xradio-skylark-sdk](https://github.com/XradioTech/xradio-skylark-sdk/tree/master/include/console)  
**Features** - A console library extracted from the Xradio SDK. Its commands use a hierarchical structure, making it suitable when there are many commands; it is based on RTOS.  

#### Key Points

- Command example: [xradio-skylark-sdk/project/common/cmd at master · XradioTech/xradio-skylark-sdk](https://github.com/XradioTech/xradio-skylark-sdk/tree/master/project/common/cmd)；
- Demo (common files): [xradio-skylark-sdk/project/demo/hello_demo at master · XradioTech/xradio-skylark-sdk](https://github.com/XradioTech/xradio-skylark-sdk/tree/master/project/demo/hello_demo)；
- Some dependent libraries are based on other files in the SDK;
- Reference: [\[XR806 Development Board Trial\] Console Flow Analysis and Adding Custom Commands - Aijishu Community - Connecting Developers and the Intelligent Computing Ecosystem](https://aijishu.com/a/1060000000288360)；
- APIs in the `cmd_util` file:
  - `cmd_main_exec` - The main command set, namely the outermost commands
  - `cmd_exec` - Subcommand set
  - `cmd_help_exec` - Displays “help” for the current level
  - `cmd2` - Indicates that the command can accept multiple parameters
- All commands in the `cmd` folder are subcommands. Define the subcommands first before using them, as in the demo;

---

### easyShell

[![Gitee Repo stars](https://gitee.com/gzbkey/easyShell/badge/star.svg?theme=gvp)](https://gitee.com/gzbkey/easyShell/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/gzbkey/easyShell&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/gzbkey/easyShell&query=$.license&label=license)]()

**Link** - [easyShell: A simple microcontroller shell. A simple and easy-to-use microcontroller shell.](https://gitee.com/gzbkey/easyShell)  
**Features** - A simple and easy-to-use microcontroller shell that supports Tab completion.  

#### Key Points

---
