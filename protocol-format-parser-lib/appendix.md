## CGI

是（Common Gateway Interface）的缩写，意为「通用网关接口」，是一种早期的 Web 服务器与外部程序（如脚本或应用程序）进行交互的标准协议。它允许 Web 服务器将客户端请求传递给外部程序处理，并将处理结果返回给客户端。其实它有点像 cli<sup>命令行界面 (CLI) ：使用文本命令进行交互的用户界面</sup>，只不过它的处理是调用外部程序，且是对接 Web 的，而 cli 是调用内部代码。

#### 特点

- **简单易用**：CGI 的实现非常简单，只需要编写一个脚本或程序，并通过标准输入（stdin）和标准输出（stdout）与 Web 服务器通信。
- **语言无关**：CGI 可以用任何编程语言实现，只要该语言能够处理标准输入输出。
- **独立进程**：每次请求都会启动一个新的 CGI 进程，处理完请求后进程退出。这种设计使得 CGI 程序与 Web 服务器完全隔离，提高了安全性。

### FastCGI

是一种用于改进传统 CGI 性能的协议，它旨在解决 CGI 在处理每个请求时都需要启动一个新的进程所带来的性能瓶颈问题。其原理是 FastCGI 使用持久连接来处理多个请求。这意味着服务器进程在启动后不会立即退出，而是保持运行状态，等待新的请求，这样可以避免频繁启动和关闭进程的开销。

---

## 什么是 cURL 命令

参考：[curl](https://curl.se)

是一个利用 URL 规则在命令行下工作的文件传输工具，只需要在命令行中输入相应的命令和参数，就可以实现文件的上传和下载等操作。

---

## INI

### 简介

INI 文件（Initialization File） 是一种无固定标准格式的配置文件。它以简单的文字与简单的结构组成，常常使用在 Windows 操作系统上，许多程序也会采用 INI 文件做为配置文件之用。Windows 操作系统后来以注册表的形式取代掉 INI 档。INI 文件的命名来源，是取自英文“初始（Initial）”的首字缩写，正与它的用途——初始化程序相应。有时候，INI 文件也会以不同的扩展名，如`.CFG`、`.CONF`、或是`.TXT`代替。

### 格式

INI 文件由节、键、值组成。

- **节**：\[section\]
- **键值**：name=value
- **注释**：; comment text

### 示例

```ini
; last modified 1 April 2001 by John Doe
[owner]
name=John Doe
organization=Acme Products

[database]
server=192.0.2.42     ; use IP address in case network name resolution is not working
port=143
file="acme payroll.dat"
```

---

## TLV

参考：[嵌入式自定义协议都按TLV格式封装吧~](https://mp.weixin.qq.com/s/XQNOnu7XpLTyfUMa5-wxbw)

### 简介

最常用最简单的自定义协议，使用数据自描述原理。拥有极简的结构，扩展性、兼容性强。  
适合高效、灵活但裸奔的场景。

### 格式

![TLV-format](./TLV-format.png)

- **Type（类型）** 
  标识数据的类型（如电压、温度、湿度等），通常用1-2字节表示。
- **Length（长度）** 
  表示Value字段的字节数，可固定或变长编码。例如，1字节（0-255）或变长整数（节省空间）。
- **Value（值）** 
  实际数据内容，长度由Length字段定义，如温度值3.11V，放大1000倍编码为整形两个字节0x0C 0x1C。

---
