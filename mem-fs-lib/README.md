# 内存与文件系统库

> 内存分为两种，一种是硬件层面上的，另一种是软件层面上的。  
> 硬件上，指的是 EEROM 和 FLASH 这类芯片的接口层或是中间封装层；  
> 软件上，指的是堆栈内存管理以及碎片处理等；  
>
> 而文件系统是基于内存之上的，所以把它们两个放在一起。  

## 内存管理

### memory

**链接**：[一个简单的 MCU 内存管理模块(附源码)](https://mp.weixin.qq.com/s/hWcoYVZE3SXgHC3ixrcP1A)  
**特征**：功能极简的内存管理模块，仅提供内存申请与释放，无其他额外功能。  

#### 要点

- 是基于 32 位写的，其他位芯片使用需要注意；

---

### mem\_malloc

[![GitHub Repo stars](https://img.shields.io/github/stars/chenqy2018/mem_malloc)](https://github.com/chenqy2018/mem_malloc/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/chenqy2018/mem_malloc)](https://github.com/chenqy2018/mem_malloc/commits) | [![GitHub License](https://img.shields.io/github/license/chenqy2018/mem_malloc)]()

**链接**：[chenqy2018/mem_malloc](https://github.com/chenqy2018/mem_malloc)  
**特征**：简单实用的内存管理模块，不会产生内存碎片。  

#### 要点

- 使用介绍：[干货 | 分享一个实用的、可应用于单片机的内存管理模块](https://mp.weixin.qq.com/s/BDdlcelPBRQvWV2KPCM_Sg)；
- 该模块只适合管理小内存，大内存的频繁分配释放效率较低；

---

### tlsf

[![GitHub Repo stars](https://img.shields.io/github/stars/mattconte/tlsf)](https://github.com/mattconte/tlsf/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/mattconte/tlsf)](https://github.com/mattconte/tlsf/commits) | [![GitHub License](https://img.shields.io/github/license/mattconte/tlsf)]()

**链接**：[mattconte/tlsf: Two-Level Segregated Fit memory allocator implementation.](https://github.com/mattconte/tlsf)  
**特征**：TLSF 算法的堆内存分配库，支持动态添加、删除内存池区域，分配时间复杂度为 O(1)，不注重线程安全。  

#### 要点

---

### LwMEM

[![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwmem)](https://github.com/MaJerle/lwmem/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwmem)](https://github.com/MaJerle/lwmem/commits) | [![GitHub License](https://img.shields.io/github/license/MaJerle/lwmem)]()

**链接**：[LwMEM latest-develop documentation — LwMEM documentation](https://docs.majerle.eu/projects/lwmem/en/latest/)  
**特征**：专业内存管理库，类 C++ 封装函数，允许使用碎片内存，注重 RTOS 的线程安全。  

#### 要点

---

### jemalloc

[![GitHub Repo stars](https://img.shields.io/github/stars/jemalloc/jemalloc)](https://github.com/jemalloc/jemalloc/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/jemalloc/jemalloc)](https://github.com/jemalloc/jemalloc/commits) | [![GitHub License](https://img.shields.io/github/license/jemalloc/jemalloc)]()

**链接**：[jemalloc](https://jemalloc.net/)  
**特征**：高性能的内存分配器，适合处理多线程环境下大规模内存分配和释放的场景。  

#### 要点

- 使用介绍：[jemalloc是一款高性能、开源的内存分配器](https://mp.weixin.qq.com/s/WuvFjuO3PsUbGBF2ryAWzg)

---

### LWMalloc

[![GitHub Repo stars](https://img.shields.io/github/stars/taehyeon-masu/lwmalloc)](https://github.com/taehyeon-masu/lwmalloc/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/taehyeon-masu/lwmalloc)](https://github.com/taehyeon-masu/lwmalloc/commits) | [![GitHub License](https://img.shields.io/github/license/taehyeon-masu/lwmalloc)]()

**链接**：[taehyeon-masu/lwmalloc --- taehyeon-masu/lwmalloc](https://github.com/taehyeon-masu/lwmalloc)  
**特征**：适用于Linux的轻量级动态内存分配器，旨在替代默认分配器 ptmalloc，性能和内存使用量都更优。  

#### 要点

---

## 读写封装层

### flashMultipleErase

[![GitHub Repo stars](https://img.shields.io/github/stars/chiphome/flashMultipleErase)](https://github.com/chiphome/flashMultipleErase/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/chiphome/flashMultipleErase)](https://github.com/chiphome/flashMultipleErase/commits) | [![GitHub License](https://img.shields.io/github/license/chiphome/flashMultipleErase)]()

**链接**：[chiphome/flashMultipleErase: 如何用单片机FLASH模拟EEPROM，并且通过算法优化实现高达100万次以上的存储次数！](https://github.com/chiphome/flashMultipleErase)  
**特征**：用FLASH模拟EEPROM，采用顺序写入的方法，以实现高达100万次以上的存储次数。  

#### 要点

---

### eepromfs

[![Gitee Repo stars](https://gitee.com/wtau_zaozao/eepromfs/badge/star.svg?theme=gvp)](https://gitee.com/wtau_zaozao/eepromfs/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/wtau_zaozao/eepromfs&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/wtau_zaozao/eepromfs&query=$.license&label=license)]()

**链接**：[eepromfs: eepromfs，基于EEPROM的简易类文件的数据读写库，方便做动态功能增减时参数管理。增减参数块类似增减文件，不会对已有数据存储带来影响。EEPROM硬件资源充裕的情况下使用。](https://gitee.com/wtau_zaozao/eepromfs)  
**特征**：基于 EEPROM 的简易类文件数据读写库，它并不属于真正的文件系统，只是把数据读写模拟成文件的方式。  

#### 要点

- 使用介绍：[分享一款 EEPROM 简易类文件的数据读写库](https://mp.weixin.qq.com/s/TbOcDkux0u1bB7NSx7DGng)
- 最好在资源充裕的情况下使用；
- 该库常年没有人管，注意一下 issues；

---

### Dhara

[![GitHub Repo stars](https://img.shields.io/github/stars/dlbeer/dhara)](https://github.com/dlbeer/dhara/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/dlbeer/dhara)](https://github.com/dlbeer/dhara/commits) | [![GitHub License](https://img.shields.io/github/license/dlbeer/dhara)]()

**链接**：[dlbeer/dhara: NAND flash translation layer for low-memory systems](https://github.com/dlbeer/dhara)  
**特征**：用于小型单片机的 NAND 闪存转换层(FTL)。  

#### 要点

- 闪存转换层介绍：[闪存转换层 - 维基百科，自由的百科全书](https://zh.wikipedia.org/zh-cn/%E5%BF%AB%E9%96%83%E8%A8%98%E6%86%B6%E9%AB%94%E8%BD%89%E6%8F%9B%E5%B1%A4)

---

### kFlashFile

[![GitHub Repo stars](https://img.shields.io/github/stars/JayHeng/kFlashFile)](https://github.com/JayHeng/kFlashFile/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/JayHeng/kFlashFile)](https://github.com/JayHeng/kFlashFile/commits) | [![GitHub License](https://img.shields.io/github/license/JayHeng/kFlashFile)]()

**链接**：[JayHeng/kFlashFile: 基于 NOR Flash 的轻量级文件数据存储方案。主要为 i.MX RT 系列设计，也可轻松移植到其他 MCU 平台](https://github.com/JayHeng/kFlashFile)  
**特征**：基于 NOR Flash 的轻量级文件数据存储方案，主要用于需要断电数据保存的项目。  

#### 要点

---

### esp_partition

[![GitHub Repo stars](https://img.shields.io/github/stars/espressif/esp-idf)](https://github.com/espressif/esp-idf/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/espressif/esp-idf?path=components/esp_partition)](https://github.com/espressif/esp-idf/commits) | [![GitHub License](https://img.shields.io/github/license/espressif/esp-idf)]()

**链接**：[esp-idf/components/esp_partition at be06a6f5ffe36f9554cfc91fe2036e0fc85fea60 · espressif/esp-idf](https://github.com/espressif/esp-idf/tree/be06a6f5ffe36f9554cfc91fe2036e0fc85fea60/components/esp_partition)  
**特征**：ESP 旗下的分区表库，封装 SPI Flash 读写操作，允许以块为单位访问 flash。  

#### 要点

- 参考：[分区表 - ESP32 - — ESP-IDF 编程指南 latest 文档](https://docs.espressif.com/projects/esp-idf/zh_CN/latest/esp32/api-guides/partition-tables.html#)

---

### NVS

[![GitHub Repo stars](https://img.shields.io/github/stars/espressif/esp-idf)](https://github.com/espressif/esp-idf/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/espressif/esp-idf?path=components/nvs_flash)](https://github.com/espressif/esp-idf/commits) | [![GitHub License](https://img.shields.io/github/license/espressif/esp-idf)]()

**链接**：[esp-idf/components/nvs_flash at be06a6f5ffe36f9554cfc91fe2036e0fc85fea60 · espressif/esp-idf](https://github.com/espressif/esp-idf/tree/be06a6f5ffe36f9554cfc91fe2036e0fc85fea60/components/nvs_flash)  
**特征**：ESP 旗下的非易失性存储库，主要用于在 flash 中存储键值格式的数据。配合 ESP 旗下的其他工具，支持加密、生成分区镜像等功能。  

#### 要点

- 参考：[非易失性存储库 - ESP32 - — ESP-IDF 编程指南 latest 文档](https://docs.espressif.com/projects/esp-idf/zh_CN/latest/esp32/api-reference/storage/nvs_flash.html#)；
- 基于 [esp_partition](#esp_partition) 组件；

---

## 文件系统

#### 文件操作常用封装：

```c
// 写操作
static int file_opt_write(const char *filename, void *ptr, int size)
{   
    FILE *fp;
    size_t num;

    fp = fopen(filename, "wb");
    if(NULL == fp)
    {
        printf("open %s file error!\n", filename);
        return -1;   
    }
  
    num = fwrite(ptr, 1, size, fp);
    if(num != size)
    {
        fclose(fp);
        printf("write %s file error!\n", filename);
        return -1;
    } 

    fclose(fp);

    return num;
}
```

```c
// 读操作
static int file_opt_read(const char *filename, void *ptr, int size)
{
    FILE *fp;
    size_t num;

    fp = fopen(filename, "rb");
    if(NULL == fp)
    {
        printf("open %s file error!\n", filename);
        return -1;
    }
  
    num = fread(ptr, 1, size, fp);
    if(num != size)
    {
        fclose(fp);
        printf("write %s file error!\n", filename);
    
        return -1;
    } 
    fclose(fp);

    return num;
}
```

> **文件目录生成镜像文件，且能被文件系统读取的关键：**  
> 文件系统其实就是在 Flash 内存里按照规则存放数据，因此要生成文件树镜像文件其实就是通过文件系统的规则在外部做一个二进制文件。要达成这个目的该文件系统必须满足<ins>在嵌入式和 PC 端都能支持运行</ins>，否则要对文件系统的规则极其熟悉，能够按照规则编写 PC 端应用。可结合这个工具使用：[文件合并助手](https://forum.anfulai.cn/forum.php?mod=viewthread&tid=8627&extra=page=1)

### FatFs

[![License: FatFs](https://img.shields.io/badge/license-FatFs-orange.svg)]()

**链接**：[FatFs - Generic FAT Filesystem Module](http://elm-chan.org/fsw/ff/00index_e.html)  
**8 位微控制器适配版**：[Petit FAT File System Module](http://elm-chan.org/fsw/ff/00index_p.html)  
**特征**：易移植的小型文件系统模块，支持 exFAT 文件系统、64 位 LBA 和 GPT，可根据功能进行宏配置，注重线程安全。  

#### 要点

- 指南：[FatFs Module Application Note](http://elm-chan.org/fsw/ff/doc/appnote.html)、 [24. 串行 FLASH 文件系统 FatFs — \[野火\]STM32 HAL 库开发实战指南——基于 F103 系列开发板 文档](https://doc.embedfire.com/mcu/stm32/f103/hal_general/zh/latest/doc/chapter25/chapter25.html)；
- 存储器太小也不能使用的，最好要 >1M;
- 函数 `f_mkfs()` 是用来格式化的；
- 移植步骤：

  1. 补充“媒体访问接口”（diskio.c）；
  2. 调用 `FATFS_LinkDriver` 进行初始化，作用是 FAT 对接内存的驱动接口；
  3. 使用“应用程序接口”（ff.h）进行操作即可；
- 参考：[FAT 文件系统 - ESP32 - — ESP-IDF 编程指南 latest 文档](https://docs.espressif.com/projects/esp-idf/zh_CN/latest/esp32/api-reference/storage/fatfs.html#)
  ESP 的封装层：[esp-idf/components/fatfs at be06a6f5ffe36f9554cfc91fe2036e0fc85fea60 · espressif/esp-idf](https://github.com/espressif/esp-idf/tree/be06a6f5ffe36f9554cfc91fe2036e0fc85fea60/components/fatfs)，可配合脚本 [fatfsgen.py](https://github.com/espressif/esp-idf/blob/be06a6f/components/fatfs/fatfsgen.py) 或 [fatfsparse.py](https://github.com/espressif/esp-idf/blob/be06a6f/components/fatfs/fatfsparse.py) 生成文件镜像烧录到设备中；
- 目前官方也推出了镜像文件代码示例：[FatFs Module Application Note](https://elm-chan.org/fsw/ff/doc/appnote.html#fs3)

---

### JesFs

[![GitHub Repo stars](https://img.shields.io/github/stars/joembedded/JesFs)](https://github.com/joembedded/JesFs/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/joembedded/JesFs)](https://github.com/joembedded/JesFs/commits) | [![GitHub License](https://img.shields.io/github/license/joembedded/JesFs)]()

**链接**：[joembedded/JesFs: Jo's Embedded Serial File System (for Standard Serial NOR-Flash)](https://github.com/joembedded/JesFs)  
**特征**：专为资源受限的嵌入式系统设计的轻量级串行 NOR 闪存文件系统，适用于各种物联网应用场景，例如数据采集、事件记录和固件更新等。  

#### 要点

- 基本特性是：可以把嵌入式系统的文件通过互联网自动地镜像存储到服务器，两端进行同步；

---

### RanFs

[![License: Unlicense](https://img.shields.io/badge/license-Unlicense-lightgrey.svg)](https://unlicense.org)

**链接**：[RANFS - RFS](http://www.ranfs.com/cn/?RFS)  
**特征**：易移植的小型文件系统模块，提供 POSIX 兼容的文件操作，注重高效和数据可靠性。  

#### 要点

---

### littlefs

[![GitHub Repo stars](https://img.shields.io/github/stars/littlefs-project/littlefs)](https://github.com/littlefs-project/littlefs/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/littlefs-project/littlefs)](https://github.com/littlefs-project/littlefs/commits) | [![GitHub License](https://img.shields.io/github/license/littlefs-project/littlefs)]()

**链接**：[littlefs-project/littlefs: A little fail-safe filesystem designed for microcontrollers](https://github.com/littlefs-project/littlefs)  
**特征**：专为微处理器设计的安全文件系统，具有掉电保护、擦写均衡、低资源消耗等功能。  

#### 要点

---

### SPIFFS

[![GitHub Repo stars](https://img.shields.io/github/stars/pellepl/spiffs)](https://github.com/pellepl/spiffs/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/pellepl/spiffs)](https://github.com/pellepl/spiffs/commits) | [![GitHub License](https://img.shields.io/github/license/pellepl/spiffs)]()

**链接**：[pellepl/spiffs: Wear-leveled SPI flash file system for embedded devices](https://github.com/pellepl/spiffs)  
**特征**：专为低内存（<=128MB）而设计文件系统，使用静态大小的 ram 缓冲区，具有擦写均衡等功能。  

#### 要点

- 尚不支持目录，但可以生成扁平结构。也就是说如果 SPIFFS 挂载在 `/spiffs` 下，在 `/spiffs/tmp/myfile.txt` 路径下创建一个文件则会在 SPIFFS 中生成一个名为 `/tmp/myfile.txt` 的文件，而不是在 `/spiffs/tmp` 下生成名为 `myfile.txt` 的文件；
- 指南：[SPIFFS 文件系统 - ESP32 - — ESP-IDF 编程指南 latest 文档](https://docs.espressif.com/projects/esp-idf/zh_CN/latest/esp32/api-reference/storage/spiffs.html#)
  ESP 的封装层：[esp-idf/components/spiffs at master · espressif/esp-idf](https://github.com/espressif/esp-idf/tree/master/components/spiffs)，可配合脚本 [spiffsgen.py](https://github.com/espressif/esp-idf/blob/be06a6f5ffe36f9554cfc91fe2036e0fc85fea60/components/spiffs/spiffsgen.py) 或 [mkspiffs](https://github.com/igrr/mkspiffs) 生成文件镜像烧录到设备中；
- 需要实现的函数接口有 3 个：`spiffs_read`、`spiffs_write`、`spiffs_erase`
  当宏 `SPIFFS_HAL_CALLBACK_EXTRA` 开启后，接口函数会增加一个接收文件系统句柄的形参；
  这些函数的地址指的是偏移地址，实际读取的地址为 `addr + phys_addr`
- 当使用 RTOS 多线程时，需要再额外实现 2 个接口：`SPIFFS_LOCK`、`SPIFFS_UNLOCK`
  这个接口就是互斥锁的上锁和解锁；
- 初始化时有三个参数与 Flash 硬件相关，且参数只能填写以下指定的倍数：
  - `phys_erase_block`：最小的擦除单位；
  - `log_block_size`：块的单位；
  - `log_page_size`：页的单位；
- 在挂载时（mount），注意`*work`、`*fd_space`、`*cache`参数的工作域，如果不是测试程序请使用不可回收变量类型（全局、动态）；
- “GC”指的是垃圾回收机制；
- 在使用 `spiffsgen.py` 工具时注意以下几点：
  - <image_size>：填写的是十六进制数大小；
  - <output_file>：脚本不带后缀名，需要自行添加。并且可以指定路径；
  - 生成的二进制文件在使用时注意：例如一个文件树为 👇
    ```
    resource
    ├─icon
    │  ├─charge_num
    │  └─pwd_num
    └─pic
    ```
    填写的 <base_dir> 为 `./resource/`，则生成的二进制文件是不包含“resource”这个路径的，使用时格式为：`/icon/charge`，而不是 ~~`resource/icon/charge`~~；

---
