# 校验、安全与引导、升级库

> 一般校验和加密都是使用了类似的安全算法，而 DFU 又是间接的和安全相关，

## 校验和安全

### crc-lib-c

**链接**：[GitHub - whik/crc-lib-c: 基于 C 语言的 CRC 校验库，包括常用的 21 个 CRC 参数模型实现](https://github.com/whik/crc-lib-c)
**特征**：极简的 CRC 库，包括常用的 21 个 CRC 参数模型实现，无扩展功能。

#### 要点

- 通过参数模型的特征选择适合的参数。

---

### tiny-AES-c

**链接**：[kokke/tiny-AES-c: Small portable AES128/192/256 in C (github.com)](https://github.com/kokke/tiny-AES-c)
**特征**：小巧易移植的 AES 算法库，提供 ECB、CTR 和 CBC 三种加密模式。

#### 要点

- 提供 C 和 C++ 两种方案；
- 参考：[aes 加密解密，含 128、192、256 位，cbc、cfb、ecb、ofb、pcbc 模式 - 简书 (jianshu.com)](https://www.jianshu.com/p/e8969d8bb6d7)；
- 不同的位数代表加密密钥的 bit 数位，128-16Byte、182-24Byte、256-32Byte；

---

### key

**链接**：[极简网络密钥加密算法 - 代码片段 AES- Gitee.com](https://gitee.com/Luyi365/codes/07ltyn2pkv5m394dgiuf849)
**特征**：极简的加密算法，配合密钥使用，功能单一但实用，适合网络加密等领域。

#### 要点

- 使用介绍：[用c语言实现一个简单的数据加解密算法](https://mp.weixin.qq.com/s/caLGRtseWHMNONCcRZlm4A)

---

### wolfssl

**链接**：[wolfSSL – Embedded SSL/TLS Library](https://www.wolfssl.com/)
**特征**：是一个轻量级的、可移植的、基于C语言的SSL/TLS库，它主要针对IoT、嵌入式和RTOS环境。

#### 要点

---

### Mbed TLS

**链接**：[Mbed TLS](https://www.trustedfirmware.org/projects/mbed-tls/)
**特征**：可信旗下的项目，业内流行的SSL/TLS库。

#### 要点

---


## 引导和升级

### Tiny Bootloader

**链接**：[jaz303/tiny_bootloader: Tiny bootloader for embedded devices, optimised for ease of porting](https://github.com/jaz303/tiny_bootloader)
**特征**：适用于 8 位和 32 位微控制器的简单引导程序，消耗极少的资源，支持多种总线通讯方式。

#### 要点

---

### OpenBLT

**链接**：[homepage [OpenBLT Bootloader\] (feaser.com)](https://www.feaser.com/openblt/doku.php)
**特征**：著名的微控制器的引导加载程序库，支持 8、16、32 位微控制器。

#### 要点

---

### wolfBoot

**链接**：[wolfSSL/wolfBoot: wolfBoot is a portable, OS-agnostic, secure bootloader for microcontrollers, supporting firmware authentication and firmware update mechanisms. (github.com)](https://github.com/wolfSSL/wolfBoot)
**特征**：适用于 32 位微控制器的安全引导加载程序解决方案，支持固件身份验证和固件更新机制。

#### 要点

- 跟 OpenBLT 相比更注重安全，但只支持 32 位微控制器；

---

### mOTA

**链接**：[mOTA: 一款专为 32 位 MCU 开发的 OTA 组件 (gitee.com)](https://gitee.com/DinoHaw/mOTA)
**特征**：专为 32 位 MCU 开发的升级组件，通过 YModem-1K 协议传输。

#### 要点

- 这里虽然叫作 OTA，但是案例采用的却是 UART 的 YModem-1K 协议；
- 使用介绍：[一款专为 32 位 MCU 开发的 OTA 组件](https://mp.weixin.qq.com/s/WsTIIvYN4E520asFaHupfQ)

---

### MicorBoot

**链接**：[MicroBoot](https://microboot.readthedocs.io/zh-cn/latest/)
**特征**：引导加载模块，专为嵌入式单片机设备的升级而优化，提供断电保护、断点续传等功能。

#### 要点

---

### MCUboot

**链接**：[MCUboot](https://www.trustedfirmware.org/projects/mcuboot)
**特征**：可信的旗下的项目，通用的 32 位微控制器的安全引导加载程序，不依赖于特定的系统和硬件。

#### 要点

---