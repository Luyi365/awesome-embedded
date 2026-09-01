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
