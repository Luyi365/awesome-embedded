## What Is POSIX

POSIX is an abbreviation of Portable Operating System Interface of UNIX. Issued by IEEE, it was originally a code standard for UNIX systems because UNIX was widely used at the time. Linux later began following this standard and continues to do so. In other words, to use a third-party library seamlessly on Linux, that library needs to support the POSIX interface standard.

*Common embedded OSs that support the POSIX interface include Linux, QNX, SylixOS, eCos, VxWorks, RT-Linux, RTEMS, NuttX...*

---

## What Is MMU

References:
[Reading Notes on "Computer Systems: A Programmer's Perspective" — Chapter 9, Virtual Memory - Zhihu (zhihu.com)](https://zhuanlan.zhihu.com/p/91172524)
[MMU Principles - Zhihu (zhihu.com)](https://zhuanlan.zhihu.com/p/354142930)
[What is an MMU? Why use an MMU?_Hutuutu's Blog-CSDN Blog](https://blog.csdn.net/KUNPLAYBOY/article/details/121157550)

MMU is an abbreviation of memory management unit. It is an indispensable part of many modern CPU architectures. Its main functions include virtual-to-physical address translation, access permission control, memory management, and address-space isolation between processes.
It is a key point that many RTOSs distinguish carefully.

In [Do RTOS tasks belong to threads, processes, or coroutines?](https://mp.weixin.qq.com/s/Ao1UM93gPnznv3_jvB7ZHw?poc_token=HIpuTGWjT_pKYYz_PJ51hN4rWC25t_PdCf6MI8V2), it is written that an MCU needs an MMU to better move up from thread management to process management.

---
