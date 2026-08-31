## About the `union` Type

Reference: [Union declaration - cppreference.com](https://zh.cppreference.com/w/c/language/union)

The official documentation states: “<ins>A pointer to a union can be converted to a pointer to each of its members (if the union has a bit-field member, a pointer to the union can be converted to a pointer to the underlying type of the bit-field). Similarly, a pointer to any member of a structure can be converted to a pointer to the entire structure.</ins>” This explains how a union should be used.

Using the following code as an example: when a union contains both pointers and variables, declaring a variable directly with *test_union* makes it a non-pointer type (automatically matching a non-pointer member type). At this point, *test_union* has the same meaning as member *num*. Declaring a variable with *test_union** makes it a pointer type (automatically matching a pointer member type). At this point, *test_union* has the same meaning as member *str* or *p_num*.
```c
typedef union
{
    char* str;
    int num;
    int* p_num;
}test_union;
int data = 0xff;
```

- When a non-pointer member of a union is needed, there are two ways to use it:
  ```c
  test_union test_1 = (test_union)data;
  test_union test_2 = {
      .num = data,
      };
  printf("%d,", test_1);
  printf("%d", test_2.num);
  //Output: 255, 255 
  ```
- When a pointer member of a union is needed, there are two ways to use it:
  ```c
  test_union *test_1 = (test_union*)&data;
  test_union test_2 = {
      .p_num = &data,
      };
  test_union test_3 = {
      .str = (char*)&data,    //Any pointer member can receive it; (void*) can also be used later
      };
  printf("%d,", *test_1 );
  printf("%d,", *test_2.p_num);
  printf("%d", *test_3.p_num);
  //Output: 255,255,255 
  ```

---
