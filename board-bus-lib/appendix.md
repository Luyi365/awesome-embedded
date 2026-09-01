## MVC 模式

参考：
[嵌入式软件设计之美-以实际项目应用 MVC 框架与状态模式(上)](https://mp.weixin.qq.com/s/YPkJLZdZjgBG1S92qAi-xQ)  
[嵌入式软件设计之美-以实际项目应用 MVC 框架与状态模式(下)](https://mp.weixin.qq.com/s/UFKLqartZyLvDGKHy3zzrA)  

MVC 框架，是软件系统模块化设计的一种方法，它给软件系统划分为三个大的部分，分别是 <u>Model（模型）</u>、<u>View（视图）</u>、<u>Controller（控制器）</u>。

- **Model（模型）** ：负责具体功能、业务逻辑实现的，可以理解为处理。例如传感器的检测过程可以认为是一个模型；
- **View（视图）** ：负责展示、响应其它模块处理结果的，可以理解为输出。例如 LED 点亮、终端显示等都是视图；
- **Controller（控制器）** ：负责来接收用户操作的，可以理解为输入。例如按键点击就是控制器；

---
