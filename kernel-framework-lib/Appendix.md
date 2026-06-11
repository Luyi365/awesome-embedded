## 关于 union 联合体

参考：[联合体声明 - cppreference.com](https://zh.cppreference.com/w/c/language/union)

官方有这样的一句话“<ins>可以将指向联合体的指针转型为指向它每个成员的指针（若联合体拥有位域成员，则能转型指向联合体的指针为指向位域底层类型的指针）。类似地，指向结构体任何成员的指针都能被转型为指向整个结构体的指针。</ins>”这句话说明了联合体该如果使用。

以该代码为例，当联合类型里既有指针又有变量时，若用 *test_union* 直接声明变量，则自身就是无指针类型（自动匹配无指针的成员类型），这时 *test_union* 意义就和成员 *num* 一样了；若用 *test_union**  来声明变量，则自身就是有指针类型（自动匹配有指针的成员类型），这时 *test_union* 意义就和成员 *str* 或 *p_num* 一样了。

```c
typedef union
{
    char* str;
    int num;
    int* p_num;
}test_union;
int data = 0xff;
```

- 当需要使用 union 内非指针成员时，有以下两种使用方法：

  ```c
  test_union test_1 = (test_union)data;
  test_union test_2 = {
      .num = data,
      };
  printf("%d,", test_1);
  printf("%d", test_2.num);
  //输出：255，255 
  ```
- 当需要使用 union 内指针成员时，有以下两种使用方法：

  ```c
  test_union *test_1 = (test_union*)&data;
  test_union test_2 = {
      .p_num = &data,
      };
  test_union test_3 = {
      .str = (char*)&data,    //用任何一个指针成员去接收都可以，后面用(void*)也可以
      };
  printf("%d,", *test_1 );
  printf("%d,", *test_2.p_num);
  printf("%d", *test_3.p_num);
  //输出：255,255,255 
  ```

---

## CGI

是（Common Gateway Interface）的缩写，意为「通用网关接口」，是一种早期的 Web 服务器与外部程序（如脚本或应用程序）进行交互的标准协议。它允许 Web 服务器将客户端请求传递给外部程序处理，并将处理结果返回给客户端。其实它有点像 cli<sup>命令行界面 (CLI) ：使用文本命令进行交互的用户界面</sup>，只不过它的处理是调用外部程序，且是对接 Web 的，而 cli 是调用内部代码。

#### 特点

- **简单易用**：CGI 的实现非常简单，只需要编写一个脚本或程序，并通过标准输入（stdin）和标准输出（stdout）与 Web 服务器通信。
- **语言无关**：CGI 可以用任何编程语言实现，只要该语言能够处理标准输入输出。
- **独立进程**：每次请求都会启动一个新的 CGI 进程，处理完请求后进程退出。这种设计使得 CGI 程序与 Web 服务器完全隔离，提高了安全性。

### FastCGI

是一种用于改进传统 CGI 性能的协议，它旨在解决 CGI 在处理每个请求时都需要启动一个新的进程所带来的性能瓶颈问题。其原理是 FastCGI 使用持久连接来处理多个请求。这意味着服务器进程在启动后不会立即退出，而是保持运行状态，等待新的请求，这样可以避免频繁启动和关闭进程的开销。

---