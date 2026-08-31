# Validation, Security, Boot, and Update Library
<!-- i18n:language-selector:start -->
[中文](README.md) | **English**
<!-- i18n:language-selector:end -->

> Validation and encryption generally use similar security algorithms, while DFU is indirectly security-related.  

## Validation and Security

### crc-lib-c

[![GitHub Repo stars](https://img.shields.io/github/stars/whik/crc-lib-c)](https://github.com/whik/crc-lib-c/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/whik/crc-lib-c)](https://github.com/whik/crc-lib-c/commits) | [![GitHub License](https://img.shields.io/github/license/whik/crc-lib-c)]()

**Link** - [GitHub - whik/crc-lib-c: A C-language CRC validation library with implementations of 21 commonly used CRC parameter models](https://github.com/whik/crc-lib-c)  
**Features** - A minimalist CRC library implementing 21 commonly used CRC parameter models, with no extensions.  

#### Key Points

- Choose suitable parameters based on the characteristics of the parameter model.

---

### tiny-AES-c

[![GitHub Repo stars](https://img.shields.io/github/stars/kokke/tiny-AES-c)](https://github.com/kokke/tiny-AES-c/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/kokke/tiny-AES-c)](https://github.com/kokke/tiny-AES-c/commits) | [![GitHub License](https://img.shields.io/github/license/kokke/tiny-AES-c)]()

**Link** - [kokke/tiny-AES-c: Small portable AES128/192/256 in C](https://github.com/kokke/tiny-AES-c)  
**Features** - A compact, portable AES library providing ECB, CTR, and CBC encryption modes.  

#### Key Points

- Provides both C and C++ implementations;
- Reference: [AES Encryption and Decryption in C, Including 128-, 192-, and 256-bit CBC, CFB, ECB, OFB, and PCBC Modes](https://www.jianshu.com/p/e8969d8bb6d7)；
- Different widths represent the bit count of the encryption key: 128-16Byte, 182-24Byte, 256-32Byte;

---

### key

**Link** - [Minimalist Network Key Encryption Algorithm - AES Code Snippet - Gitee.com](https://gitee.com/Luyi365/codes/07ltyn2pkv5m394dgiuf849)  
**Features** - A minimalist encryption algorithm used with keys. It is single-purpose but practical, and suitable for network encryption and similar applications.  

#### Key Points

- Introduction: [Implementing a Simple Data Encryption and Decryption Algorithm in C](https://mp.weixin.qq.com/s/caLGRtseWHMNONCcRZlm4A)

---

### wolfCrypt

[![GitHub Repo stars](https://img.shields.io/github/stars/wolfSSL/wolfssl)](https://github.com/wolfSSL/wolfssl/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/wolfSSL/wolfssl/wolfcrypt)](https://github.com/wolfSSL/wolfssl/commits) | [![GitHub License](https://img.shields.io/github/license/wolfSSL/wolfssl)]()

**Link** - [wolfCrypt Embedded Crypto Engine | Products - wolfSSL](https://www.wolfssl.com/products/wolfcrypt-2)  
**FIPS-certified version** - [wolfCrypt FIPS FIPS 140-3 | Licensing - wolfSSL](https://www.wolfssl.com/license/fips)  
**Features** - A lightweight cryptographic library from wolfSSL that supports many popular algorithms and ciphers, suitable for enterprise projects.  

#### Key Points

- This library is included in [wolfSSL](#wolfssl);

---

### wolfSSL

[![GitHub Repo stars](https://img.shields.io/github/stars/wolfSSL/wolfssl)](https://github.com/wolfSSL/wolfssl/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/wolfSSL/wolfssl)](https://github.com/wolfSSL/wolfssl/commits) | [![GitHub License](https://img.shields.io/github/license/wolfSSL/wolfssl)]()

**Link** - [wolfSSL - Embedded SSL/TLS Library](https://www.wolfssl.com/)  
**Features** - A lightweight, portable SSL/TLS library powered by the [wolfCrypt](#wolfcrypt) cryptography library, aimed at IoT, embedded, and RTOS environments.

#### Key Points

- [Supports RTCA DO-178C DAL A certification](https://www.wolfssl.com/wolfssl-support-178-dal)；

---

### Mbed TLS

[![GitHub Repo stars](https://img.shields.io/github/stars/Mbed-TLS/mbedtls)](https://github.com/Mbed-TLS/mbedtls/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/Mbed-TLS/mbedtls)](https://github.com/Mbed-TLS/mbedtls/commits) | [![GitHub License](https://img.shields.io/github/license/Mbed-TLS/mbedtls)]()

**Link** - [Mbed TLS](https://www.trustedfirmware.org/projects/mbed-tls/)  
**Features** - A TrustedFirmware project and a widely used SSL/TLS library in the industry.  

#### Key Points

---

### wolfHSM

[![GitHub Repo stars](https://img.shields.io/github/stars/wolfSSL/wolfHSM)](https://github.com/wolfSSL/wolfHSM/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/wolfSSL/wolfHSM)](https://github.com/wolfSSL/wolfHSM/commits) | [![GitHub License](https://img.shields.io/github/license/wolfSSL/wolfHSM)]()

**Link** - [wolfHSM | Products - wolfSSL](https://www.wolfssl.com/products/wolfhsm)  
**Features** - A client-server framework for hardware cryptography, nonvolatile memory, and secure processing. Originally an HSM core for automotive applications, it now suits any trusted environment.

#### Key Points

- Encryption and decryption require porting [wolfCrypt](#wolfcrypt) or using [hardware support](https://www.wolfssl.com/docs/hardware-crypto-support)；

---

### wolfTPM

[![GitHub Repo stars](https://img.shields.io/github/stars/wolfSSL/wolfTPM)](https://github.com/wolfSSL/wolfTPM/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/wolfSSL/wolfTPM)](https://github.com/wolfSSL/wolfTPM/commits) | [![GitHub License](https://img.shields.io/github/license/wolfSSL/wolfTPM)]()

**Link** - [wolfTPM | Products - wolfSSL](https://www.wolfssl.com/products/wolftpm)  
**Features** - A portable TPM stack that provides wrapper interfaces to simplify key operations and supports bare metal, RTOS, Linux, Windows, and other platforms.

#### Key Points

- Includes an [fTPM](https://www.wolfssl.com/announcing-wolftpm-firmware-tpm-ftpm-support) implementation for embedded devices without TPM hardware;

---

### wolfSentry

[![GitHub Repo stars](https://img.shields.io/github/stars/wolfSSL/wolfsentry)](https://github.com/wolfSSL/wolfsentry/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/wolfSSL/wolfsentry)](https://github.com/wolfSSL/wolfsentry/commits) | [![GitHub License](https://img.shields.io/github/license/wolfSSL/wolfsentry)]()

**Link** - [wolfSentry | Products - wolfSSL](https://www.wolfssl.com/products/wolfsentry/)  
**Features** - A dynamic intrusion detection and prevention system (IDPS): an embedded-ready firewall engine centered on monitoring, logging, pattern matching, and notification.

#### Key Points

---

## Boot and Update

### Tiny Bootloader

[![GitHub Repo stars](https://img.shields.io/github/stars/jaz303/tiny_bootloader)](https://github.com/jaz303/tiny_bootloader/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/jaz303/tiny_bootloader)](https://github.com/jaz303/tiny_bootloader/commits) | [![GitHub License](https://img.shields.io/github/license/jaz303/tiny_bootloader)]()

**Link** - [jaz303/tiny_bootloader: Tiny bootloader for embedded devices, optimised for ease of porting](https://github.com/jaz303/tiny_bootloader)  
**Features** - A simple bootloader for 8-bit and 32-bit microcontrollers that uses very few resources and supports multiple bus communication methods.  

#### Key Points

---

### OpenBLT

[![GitHub Repo stars](https://img.shields.io/github/stars/feaser/openblt)](https://github.com/feaser/openblt/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/feaser/openblt)](https://github.com/feaser/openblt/commits) | [![GitHub License](https://img.shields.io/github/license/feaser/openblt)]()

**Link** - [homepage [OpenBLT Bootloader]](https://www.feaser.com/openblt/doku.php)  
**Features** - A well-known microcontroller bootloader library supporting 8-, 16-, and 32-bit microcontrollers.  

#### Key Points

---

### wolfBoot

[![GitHub Repo stars](https://img.shields.io/github/stars/wolfSSL/wolfBoot)](https://github.com/wolfSSL/wolfBoot/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/wolfSSL/wolfBoot)](https://github.com/wolfSSL/wolfBoot/commits) | [![GitHub License](https://img.shields.io/github/license/wolfSSL/wolfBoot)]()

**Link** - [wolfBoot Secure Bootloader | Products - wolfSSL](https://www.wolfssl.com/products/wolfboot/)  
**Features** - A secure bootloader solution for 32-bit microcontrollers, supporting firmware authentication and firmware update mechanisms.  

#### Key Points

- Compared with OpenBLT, it focuses more on security but supports only 32-bit microcontrollers;

---

### mOTA

[![Gitee Repo stars](https://gitee.com/DinoHaw/mOTA/badge/star.svg?theme=gvp)](https://gitee.com/DinoHaw/mOTA/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/DinoHaw/mOTA&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/DinoHaw/mOTA&query=$.license&label=license)]()

**Link** - [mOTA: An OTA component designed for 32-bit MCU development](https://gitee.com/DinoHaw/mOTA)  
**Features** - An update component designed for 32-bit MCUs, transferred through the YModem-1K protocol.  

#### Key Points

- Although it is called OTA here, the example uses the UART YModem-1K protocol;
- Introduction: [An OTA Component Designed for 32-bit MCU Development](https://mp.weixin.qq.com/s/WsTIIvYN4E520asFaHupfQ)

---

### MicorBoot

[![GitHub Repo stars](https://img.shields.io/github/stars/Aladdin-Wang/MicroBootRom)](https://github.com/Aladdin-Wang/MicroBootRom/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/Aladdin-Wang/MicroBootRom)](https://github.com/Aladdin-Wang/MicroBootRom/commits) | [![GitHub License](https://img.shields.io/github/license/Aladdin-Wang/MicroBootRom)]()

**Link** - [MicroBoot](https://microboot.readthedocs.io/zh-cn/latest/)  
**Features** - A bootloader module optimized for embedded microcontroller-device updates, providing power-failure protection, resumable transfers, and more.  

#### Key Points

---

### MCUboot

[![GitHub Repo stars](https://img.shields.io/github/stars/mcu-tools/mcuboot)](https://github.com/mcu-tools/mcuboot/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/mcu-tools/mcuboot)](https://github.com/mcu-tools/mcuboot/commits) | [![GitHub License](https://img.shields.io/github/license/mcu-tools/mcuboot)]()

**Link** - [MCUboot](https://www.trustedfirmware.org/projects/mcuboot)  
**Features** - A TrustedFirmware project: a general secure bootloader for 32-bit microcontrollers that is independent of specific systems and hardware.  

#### Key Points

---
