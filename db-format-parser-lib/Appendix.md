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
