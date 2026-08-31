## MVC Pattern

References:
[The beauty of embedded software design: applying the MVC framework and state pattern in real projects (Part 1)](https://mp.weixin.qq.com/s/YPkJLZdZjgBG1S92qAi-xQ)  
[The beauty of embedded software design: applying the MVC framework and state pattern in real projects (Part 2)](https://mp.weixin.qq.com/s/UFKLqartZyLvDGKHy3zzrA)  

The MVC framework is a method for modular software design. It divides a software system into three major parts: <u>Model</u>, <u>View</u>, and <u>Controller</u>.

- **Model** - Responsible for implementing specific functions and business logic. It can be understood as processing; for example, sensor detection can be considered a model.
- **View** - Responsible for presenting and responding to results processed by other modules. It can be understood as output; lighting an LED and displaying a terminal are both views.
- **Controller** - Responsible for receiving user operations. It can be understood as input; a button press is a controller.

---
