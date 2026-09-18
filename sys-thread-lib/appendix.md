## 什么是 POSIX

是（Portable Operating System Interface of UNIX）的缩写，意为「可移植操作系统接口」。由 IEEE 颁布，最初是用在 UNIX 系统的代码标准上，因为当时 UNIX 系统的普及率很大。后来 Linux 系统也开始遵循这个标准并使用至今，也就是说在 Linux 系统的基础上想要无缝使用其他第三方库，这个第三方库就需要支持 POSIX 接口标准了。

*目前嵌入式常用 OS 中支持 POSIX 接口的有：Linux，QNX，SylixOS，eCos，VxWorks，RT-Linux，RTEMS，NuttX...*

---

## 何为 MMU

参考：
[《深入理解计算机系统》读书笔记 —— 第九章、虚拟内存 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/91172524)
[MMU 原理 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/354142930)
[什么是 mmu？为什么要用 mmu？_胡涂涂~的博客-CSDN 博客](https://blog.csdn.net/KUNPLAYBOY/article/details/121157550)

是（memory management unit）的缩写，意为「内存管理单元」，是很多现代 CPU 架构中不可或缺的一部分。主要包含的功能有 虚实地址翻译、访问权限控制、内存管理、进程的地址空间隔离 等。
是很多 RTOS 的会重点区分的一点。

在 [RTOS 任务属于线程、进程、还是协程？](https://mp.weixin.qq.com/s/Ao1UM93gPnznv3_jvB7ZHw?poc_token=HIpuTGWjT_pKYYz_PJ51hN4rWC25t_PdCf6MI8V2)中写道：MCU 带有 MMU 才能更好的从线程上升到进程的管理。

---
