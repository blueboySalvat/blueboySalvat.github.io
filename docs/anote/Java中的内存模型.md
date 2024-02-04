---
创建日期: 2024.01.21 星期日 8点38分28秒 晚上<br>
最后修改: 2024.02.3 星期六 5点09分52秒 下午<br>
---
## 栈内存空间
>基本数据类型
引用（数组名、类名、接口名）

- 先进后出，后进先出  
- 存取速度比堆要快，仅次于寄存器，栈数据可以共享，但缺点是，存在栈中的数据大小与生存必须是确定的，缺乏灵活性


## 堆内存空间
> `new` 出来的内容（数组、对象）

- 先进先出，后进后出
- 堆可以动态地分配内存大小，生存期也不必事先告诉编译器，因为它是在运行时动态分配内存的，但缺点是，由于要在运行时动态分配内存，存取速度较慢。

# 图解 JVM 内存模型：
![](../img/JVM_RAM_Structure.png)
![](../img/JVM_RAM_Structure2.png)
![](../img/JVM_RAM_Structure3.png)

# 参考资料 ：
- [带你认识java中jvm虚拟机栈]( https://www.bilibili.com/video/BV1ET4y1Z711/ )
- [白话 JVM 内存结构，死也忘不了]( https://www.bilibili.com/video/BV1Q64y1h7PT )
- [jvm内存模型全面解析哔哩哔哩](https://www.bilibili.com/video/BV12t411u726/) 