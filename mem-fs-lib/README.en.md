# Memory and File System Library
<!-- i18n:language-selector:start -->
[中文](README.md) | **English**
<!-- i18n:language-selector:end -->

> Memory has two forms: one at the hardware level and the other at the software level.  
> At the hardware level, it refers to the interface layer or intermediate wrapper layer for chips such as EEROM and FLASH;  
> At the software level, it refers to stack and heap memory management, fragmentation handling, and so on;  
>
> Since file systems are built on memory, they are grouped together here.  

## Memory Management

### memory

**Link** - [A Simple MCU Memory Management Module (with Source Code)](https://mp.weixin.qq.com/s/hWcoYVZE3SXgHC3ixrcP1A)  
**Features** - A minimalist memory management module that only provides memory allocation and release, with no other features.  

#### Key Points

- It was written for 32-bit systems; care is needed when using it on chips of other bit widths;

---

### mem\_malloc

[![GitHub Repo stars](https://img.shields.io/github/stars/chenqy2018/mem_malloc)](https://github.com/chenqy2018/mem_malloc/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/chenqy2018/mem_malloc)](https://github.com/chenqy2018/mem_malloc/commits) | [![GitHub License](https://img.shields.io/github/license/chenqy2018/mem_malloc)]()

**Link** - [chenqy2018/mem_malloc](https://github.com/chenqy2018/mem_malloc)  
**Features** - A simple and practical memory management module that does not produce memory fragmentation.  

#### Key Points

- Introduction: [Practical Guide | Sharing a Practical Memory Management Module for Microcontrollers](https://mp.weixin.qq.com/s/BDdlcelPBRQvWV2KPCM_Sg)；
- This module is suitable only for managing small memory; frequent allocation and release of large memory is inefficient;

---

### tlsf

[![GitHub Repo stars](https://img.shields.io/github/stars/mattconte/tlsf)](https://github.com/mattconte/tlsf/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/mattconte/tlsf)](https://github.com/mattconte/tlsf/commits) | [![GitHub License](https://img.shields.io/github/license/mattconte/tlsf)]()

**Link** - [mattconte/tlsf: Two-Level Segregated Fit memory allocator implementation.](https://github.com/mattconte/tlsf)  
**Features** - A heap allocator using the TLSF algorithm. It supports dynamically adding and removing memory-pool regions, has $O(1)$ allocation complexity, and does not emphasize thread safety.  

#### Key Points

---

### LwMEM

[![GitHub Repo stars](https://img.shields.io/github/stars/MaJerle/lwmem)](https://github.com/MaJerle/lwmem/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/MaJerle/lwmem)](https://github.com/MaJerle/lwmem/commits) | [![GitHub License](https://img.shields.io/github/license/MaJerle/lwmem)]()

**Link** - [LwMEM latest-develop documentation — LwMEM documentation](https://docs.majerle.eu/projects/lwmem/en/latest/)  
**Features** - A professional memory management library with C++-like wrapper functions. It permits fragmented memory use and emphasizes RTOS thread safety.  

#### Key Points

---

### jemalloc

[![GitHub Repo stars](https://img.shields.io/github/stars/jemalloc/jemalloc)](https://github.com/jemalloc/jemalloc/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/jemalloc/jemalloc)](https://github.com/jemalloc/jemalloc/commits) | [![GitHub License](https://img.shields.io/github/license/jemalloc/jemalloc)]()

**Link** - [jemalloc](https://jemalloc.net/)  
**Features** - A high-performance memory allocator suitable for large-scale memory allocation and release in multithreaded environments.  

#### Key Points

- Introduction: [jemalloc Is a High-Performance, Open-Source Memory Allocator](https://mp.weixin.qq.com/s/WuvFjuO3PsUbGBF2ryAWzg)

---

### LWMalloc

[![GitHub Repo stars](https://img.shields.io/github/stars/taehyeon-masu/lwmalloc)](https://github.com/taehyeon-masu/lwmalloc/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/taehyeon-masu/lwmalloc)](https://github.com/taehyeon-masu/lwmalloc/commits) | [![GitHub License](https://img.shields.io/github/license/taehyeon-masu/lwmalloc)]()

**Link** - [taehyeon-masu/lwmalloc --- taehyeon-masu/lwmalloc](https://github.com/taehyeon-masu/lwmalloc)  
**Features** - A lightweight dynamic memory allocator for Linux, designed to replace the default ptmalloc allocator with better performance and memory usage.  

#### Key Points

---

## Read/Write Wrapper Layer

### flashMultipleErase

[![GitHub Repo stars](https://img.shields.io/github/stars/chiphome/flashMultipleErase)](https://github.com/chiphome/flashMultipleErase/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/chiphome/flashMultipleErase)](https://github.com/chiphome/flashMultipleErase/commits) | [![GitHub License](https://img.shields.io/github/license/chiphome/flashMultipleErase)]()

**Link** - [chiphome/flashMultipleErase: How to emulate EEPROM with microcontroller FLASH and use algorithmic optimization to achieve more than one million storage cycles!](https://github.com/chiphome/flashMultipleErase)  
**Features** - Emulates EEPROM with FLASH and uses sequential writing to achieve more than one million storage cycles.  

#### Key Points

---

### eepromfs

[![Gitee Repo stars](https://gitee.com/wtau_zaozao/eepromfs/badge/star.svg?theme=gvp)](https://gitee.com/wtau_zaozao/eepromfs/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/wtau_zaozao/eepromfs&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/wtau_zaozao/eepromfs&query=$.license&label=license)]()

**Link** - [eepromfs: eepromfs is a simple file-like data read/write library based on EEPROM, making parameter management convenient when dynamically adding or removing functions. Adding and removing parameter blocks is like adding and removing files, without affecting existing stored data. Use it when EEPROM hardware resources are ample.](https://gitee.com/wtau_zaozao/eepromfs)  
**Features** - A simple file-like data read/write library based on EEPROM. It is not a true file system, but simulates data reads and writes as files.  

#### Key Points

- It is best used when resources are ample;
- This library has been unmaintained for years; pay attention to its issues;

---

### Dhara

[![GitHub Repo stars](https://img.shields.io/github/stars/dlbeer/dhara)](https://github.com/dlbeer/dhara/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/dlbeer/dhara)](https://github.com/dlbeer/dhara/commits) | [![GitHub License](https://img.shields.io/github/license/dlbeer/dhara)]()

**Link** - [dlbeer/dhara: NAND flash translation layer for low-memory systems](https://github.com/dlbeer/dhara)  
**Features** - A NAND flash translation layer (FTL) for small microcontrollers.  

#### Key Points

- Flash translation layer introduction: [Flash Translation Layer - Wikipedia, the Free Encyclopedia](https://zh.wikipedia.org/zh-cn/%E5%BF%AB%E9%96%83%E8%A8%98%E6%86%B6%E9%AB%94%E8%BD%89%E6%8F%9B%E5%B1%A4)

---

### kFlashFile

[![GitHub Repo stars](https://img.shields.io/github/stars/JayHeng/kFlashFile)](https://github.com/JayHeng/kFlashFile/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/JayHeng/kFlashFile)](https://github.com/JayHeng/kFlashFile/commits) | [![GitHub License](https://img.shields.io/github/license/JayHeng/kFlashFile)]()

**Link** - [JayHeng/kFlashFile: A lightweight file-data storage solution based on NOR Flash. Primarily designed for the i.MX RT series, it can also be easily ported to other MCU platforms](https://github.com/JayHeng/kFlashFile)  
**Features** - A lightweight file-data storage solution based on NOR Flash, primarily for projects that require data to be preserved after power loss.  

#### Key Points

---

### esp_partition

[![GitHub Repo stars](https://img.shields.io/github/stars/espressif/esp-idf)](https://github.com/espressif/esp-idf/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/espressif/esp-idf?path=components/esp_partition)](https://github.com/espressif/esp-idf/commits) | [![GitHub License](https://img.shields.io/github/license/espressif/esp-idf)]()

**Link** - [esp-idf/components/esp_partition at be06a6f5ffe36f9554cfc91fe2036e0fc85fea60 · espressif/esp-idf](https://github.com/espressif/esp-idf/tree/be06a6f5ffe36f9554cfc91fe2036e0fc85fea60/components/esp_partition)  
**Features** - A partition-table library from ESP that wraps SPI Flash read/write operations and allows flash access by block.  

#### Key Points

- Reference: [Partition Tables - ESP32 - — ESP-IDF Programming Guide latest documentation](https://docs.espressif.com/projects/esp-idf/zh_CN/latest/esp32/api-guides/partition-tables.html#)

---

### NVS

[![GitHub Repo stars](https://img.shields.io/github/stars/espressif/esp-idf)](https://github.com/espressif/esp-idf/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/espressif/esp-idf?path=components/nvs_flash)](https://github.com/espressif/esp-idf/commits) | [![GitHub License](https://img.shields.io/github/license/espressif/esp-idf)]()

**Link** - [esp-idf/components/nvs_flash at be06a6f5ffe36f9554cfc91fe2036e0fc85fea60 · espressif/esp-idf](https://github.com/espressif/esp-idf/tree/be06a6f5ffe36f9554cfc91fe2036e0fc85fea60/components/nvs_flash)  
**Features** - A non-volatile storage library from ESP, primarily for storing key-value data in flash. Together with other ESP tools, it supports encryption, partition-image generation, and other functions.  

#### Key Points

- Reference: [Non-Volatile Storage Library - ESP32 - — ESP-IDF Programming Guide latest documentation](https://docs.espressif.com/projects/esp-idf/zh_CN/latest/esp32/api-reference/storage/nvs_flash.html#)；
- Based on the [esp_partition](#esp_partition) component;

---

## File Systems

#### Common File Operation Wrappers:

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

> **The key to generating an image file from a file directory that the file system can read:**  
> A file system stores data in Flash memory according to rules, so generating a file-tree image means creating an external binary file according to those rules. To accomplish this, the file system must <ins>support operation on both embedded devices and PCs</ins>; otherwise, you must be extremely familiar with its rules and be able to write a PC application accordingly. It can be used together with this tool: [File Merge Assistant](https://forum.anfulai.cn/forum.php?mod=viewthread&tid=8627&extra=page=1)

### FatFs

[![License: FatFs](https://img.shields.io/badge/license-FatFs-orange.svg)]()

**Link** - [FatFs - Generic FAT Filesystem Module](http://elm-chan.org/fsw/ff/00index_e.html)  
**8-bit microcontroller edition** - [Petit FAT File System Module](http://elm-chan.org/fsw/ff/00index_p.html)  
**Features** - A portable, compact file system module supporting the exFAT file system, 64-bit LBA, and GPT. It can be configured with macros according to required functionality and emphasizes thread safety.  

#### Key Points

- Guides: [FatFs Module Application Note](http://elm-chan.org/fsw/ff/doc/appnote.html)、 [24. Serial FLASH File System FatFs — [Wildfire] STM32 HAL Library Development Practice Guide — Based on the F103 Series Development Board Documentation](https://doc.embedfire.com/mcu/stm32/f103/hal_general/zh/latest/doc/chapter25/chapter25.html)；
- Storage that is too small cannot be used either; it is best to have >1M;
- The `f_mkfs()` function is used for formatting;
- Porting steps:

  1. Add the “media access interface” (diskio.c);
  2. Call `FATFS_LinkDriver` for initialization; it is the FAT driver interface to memory;
  3. Use the “application interface” (ff.h) for operations;
- Reference: [FAT File System - ESP32 - — ESP-IDF Programming Guide latest documentation](https://docs.espressif.com/projects/esp-idf/zh_CN/latest/esp32/api-reference/storage/fatfs.html#)
  ESP wrapper layer: [esp-idf/components/fatfs at be06a6f5ffe36f9554cfc91fe2036e0fc85fea60 · espressif/esp-idf](https://github.com/espressif/esp-idf/tree/be06a6f5ffe36f9554cfc91fe2036e0fc85fea60/components/fatfs), which can use the scripts [fatfsgen.py](https://github.com/espressif/esp-idf/blob/be06a6f/components/fatfs/fatfsgen.py) or [fatfsparse.py](https://github.com/espressif/esp-idf/blob/be06a6f/components/fatfs/fatfsparse.py) to generate a file image for flashing to the device;
- The official project has also released an image-file code example: [FatFs Module Application Note](https://elm-chan.org/fsw/ff/doc/appnote.html#fs3)

---

### JesFs

[![GitHub Repo stars](https://img.shields.io/github/stars/joembedded/JesFs)](https://github.com/joembedded/JesFs/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/joembedded/JesFs)](https://github.com/joembedded/JesFs/commits) | [![GitHub License](https://img.shields.io/github/license/joembedded/JesFs)]()

**Link** - [joembedded/JesFs: Jo's Embedded Serial File System (for Standard Serial NOR-Flash)](https://github.com/joembedded/JesFs)  
**Features** - A lightweight serial NOR flash file system designed for resource-constrained embedded systems. It is suitable for IoT use cases such as data collection, event logging, and firmware updates.  

#### Key Points

- Its basic feature is automatically mirroring embedded-system files to a server over the Internet and synchronizing the two ends;

---

### RanFs

[![License: Unlicense](https://img.shields.io/badge/license-Unlicense-lightgrey.svg)](https://unlicense.org)

**Link** - [RANFS - RFS](http://www.ranfs.com/cn/?RFS)  
**Features** - A portable, compact file system module providing POSIX-compatible file operations and emphasizing efficiency and data reliability.  

#### Key Points

---

### littlefs

[![GitHub Repo stars](https://img.shields.io/github/stars/littlefs-project/littlefs)](https://github.com/littlefs-project/littlefs/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/littlefs-project/littlefs)](https://github.com/littlefs-project/littlefs/commits) | [![GitHub License](https://img.shields.io/github/license/littlefs-project/littlefs)]()

**Link** - [littlefs-project/littlefs: A little fail-safe filesystem designed for microcontrollers](https://github.com/littlefs-project/littlefs)  
**Features** - A safe file system designed for microprocessors, with power-loss protection, wear leveling, low resource consumption, and other features.  

#### Key Points

---

### SPIFFS

[![GitHub Repo stars](https://img.shields.io/github/stars/pellepl/spiffs)](https://github.com/pellepl/spiffs/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/pellepl/spiffs)](https://github.com/pellepl/spiffs/commits) | [![GitHub License](https://img.shields.io/github/license/pellepl/spiffs)]()

**Link** - [pellepl/spiffs: Wear-leveled SPI flash file system for embedded devices](https://github.com/pellepl/spiffs)  
**Features** - A file system designed for low memory (<=128MB), using statically sized ram buffers and providing wear leveling and other functions.  

#### Key Points

- Directories are not yet supported, but a flat structure can be generated. That is, if SPIFFS is mounted under `/spiffs`, creating a file at `/spiffs/tmp/myfile.txt` generates a file named `/tmp/myfile.txt` in SPIFFS rather than a file named `myfile.txt` under `/spiffs/tmp`;
- Guide: [SPIFFS File System - ESP32 - — ESP-IDF Programming Guide latest documentation](https://docs.espressif.com/projects/esp-idf/zh_CN/latest/esp32/api-reference/storage/spiffs.html#)
  ESP wrapper layer: [esp-idf/components/spiffs at master · espressif/esp-idf](https://github.com/espressif/esp-idf/tree/master/components/spiffs), which can use the script [spiffsgen.py](https://github.com/espressif/esp-idf/blob/be06a6f5ffe36f9554cfc91fe2036e0fc85fea60/components/spiffs/spiffsgen.py) or [mkspiffs](https://github.com/igrr/mkspiffs) to generate a file image for flashing to the device;
- Three function interfaces must be implemented: `spiffs_read`, `spiffs_write`, and `spiffs_erase`
  When the `SPIFFS_HAL_CALLBACK_EXTRA` macro is enabled, the interface functions gain a parameter that receives the file system handle;
  The addresses in these functions are offset addresses; the actual address read is `addr + phys_addr`
- When using RTOS multithreading, two additional interfaces must be implemented: `SPIFFS_LOCK` and `SPIFFS_UNLOCK`
  These interfaces lock and unlock the mutex;
- Three initialization parameters are related to Flash hardware, and each can only use the following specified multiples:
  - `phys_erase_block` - Minimum erase unit;
  - `log_block_size` - Block unit;
  - `log_page_size` - Page unit;
- When mounting, pay attention to the working areas of the `*work`, `*fd_space`, and `*cache` parameters. For non-test programs, use non-reclaimable variable types (global or dynamic);
- “GC” refers to the garbage collection mechanism;
- When using the `spiffsgen.py` tool, note the following:
  - <image_size> - Enter a hexadecimal size;
  - <output_file> - The script has no suffix; add one yourself. A path can also be specified;
  - When using the generated binary file, note the following. For example, a file tree is 👇
    ```
    resource
    ├─icon
    │  ├─charge_num
    │  └─pwd_num
    └─pic
    ```
    With <base_dir> set to `./resource/`, the generated binary file does not include the “resource” path. Use the format `/icon/charge`, not ~~`resource/icon/charge`~~;

---
