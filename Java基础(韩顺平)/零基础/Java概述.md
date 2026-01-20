##### 1. Java重要特点

* Java语言是面向对象的语言(OOP)

* Java语言是健壮的。Java的强类型机制、异常处理、垃圾的自动收集等是Java程序健壮性的重要保证。

*  Java语言是跨平台性的。即一个编译好的.class 文件可以在多个系统下运行。

  整个Java执行流程：先编写Test.java程序，编译形成Test.class文件，Test.class文件可以被不同的操作系统执行。

  <img src="../notes-images/202311092319712.png" alt="image-20231109231940641" style="zoom:80%;" />

* Java语言是解释性语言。

  解释性语言：JavaScript，PHP，Java   编译性语言：C/C++

  区别是：解释性语言，编译后的代码，不能直接被机器执行，需要解释器来执行，编译性语言，编译后的代码，可以直接被机器执行。

  编译后得到的.class 文件，需要一个底层的解释器对文件进行执行。



##### 2. Java运行机制及运行过程

* Java语言的特点：跨平台性

<img src="../notes-images/202311100945793.png" alt="image-20231110094520548" style="zoom: 50%;" />

* Java核心机制-Java虚拟机

  * JVM是一个虚拟的计算机，具有指令集并使用不同的存储区域，负责执行指令，管理数据、内存、寄存器，包含在JDK中。

  * 对于不同的平台，有不同的虚拟机。

  * Java虚拟机机制屏蔽了底层运行平台的差别，实现了”一次编译，到处运行“。

    <img src="../notes-images/202311100959517.png" alt="image-20231110095911412" style="zoom:67%;" />

##### 3. 什么是JDK，JRE

![image-20231111110046912](../notes-images/202311111100085.png)

​		Java开发工具包：bin目录下面

![image-20231111110222958](../notes-images/202311111102019.png)

![image-20231111110350895](../notes-images/202311111103946.png)

##### 4. 配置环境变量path

​	为什么要配置环境变量path？

![image-20231111110638917](../notes-images/202311111106060.png)

##### 5. helloworld

* public class Hello 表示Hello是一个public公有的类

  pubilic static void main(Stirng[] args) 表示一个主方法，即程序的执行入口。

* .class文件（字节码文件）用java这个指令运行的本质就是将.class文件装载到对应的虚拟机里运行

* ![image-20231111114911217](../notes-images/202311111149394.png)

* java Hello运行(不是java hello.class)

  本身运行的确实是class文件，但不能带.class，因为java hello指的是找到hello这个主类来执行，准确的讲运行的是hello这个类，没必要加上.class，加上之后认为运行的是“hello.class”这个类。

##### 6. Java开发注意事项

* <img src="../notes-images/202311120051625.png" alt="image-20231112005110562" style="zoom:67%;" />

* 如果源文件包含一个public类，则文件名必须按该类名命名。

![image-20231112004818703](../notes-images/202311120048748.png)

* 一个源文件中最多只能有一个public类，其他类的个数不限，也可以将main方法写在非public类中，然后指定运行非public类，这样入口方法就是非public的main方法。

<img src="../notes-images/202311120049766.png" alt="image-20231112004929714" style="zoom:67%;" />

##### 7. 文档注释

注释内容可以被JDK提供的工具javadoc所解析，生成一套以网页文件形式体现的该程序的说明文档，一般写在类。

基本格式：javadoc -d 文件夹名 -xx -yy zz.java

![image-20231112010022149](../notes-images/202311120100216.png)

![image-20231112010051852](../notes-images/202311120100903.png)

![image-20231112010125027](../notes-images/202311120101076.png)

![image-20231112010155040](../notes-images/202311120101091.png)

常用Javadoc标签

@author

@version

@see

@return等

##### 8. Java代码规范

![image-20231112010532623](../notes-images/202311120105807.png)

##### 9. 数据类型

* ![image-20231112010931702](../notes-images/202311120109814.png)

* 关于浮点数在机器中存放的形式：浮点数=符号位+指数位+尾数位

  尾数位部分可能丢失，造成精度损失，小数都是近似值。

  ![image-20231112011239346](../notes-images/202311120112389.png)

* ![image-20231112011340713](../notes-images/202311120113756.png)

​		输出：

​		2.1234567851

​		2.1234567

* ![image-20231112011519588](../notes-images/202311120115645.png)

​		输出：

​		2.6999999999999997

​		原因：计算机在存储8.1时以精度的形式，认为8.1后面还有（认为可能是8.1000001），所以在计算时以		精度的形式返回。





* ![image-20231112011628946](../notes-images/202311120116000.png)

* ![image-20231112011729366](../notes-images/202311120117487.png)

* ![image-20231112011805556](../notes-images/202311120118677.png)

![image-20231112011836274](../notes-images/202311120118340.png)

![image-20231112011944072](../notes-images/202311120119187.png)

![image-20231112012025229](../notes-images/202311120120304.png)

![image-20231112012051041](../notes-images/202311120120103.png)

##### 10. Java API文档

![image-20231113003504971](../notes-images/202311130035221.png)

##### 11. 运算符

* ![image-20231114002835850](../notes-images/202311140028041.png)

* ![image-20231114002937365](../notes-images/202311140029495.png)

* ![image-20231127103436060](../notes-images/202311271034172.png) 

* ![image-20231127105219774](../notes-images/202311271052872.png)

* ![image-20231127110039384](../notes-images/202311271100447.png)

* ![image-20231114003025535](../notes-images/202311140030610.png)

* ![image-20231114003107967](../notes-images/202311140031219.png)

* ![image-20231114003139974](../notes-images/202311140031139.png)

* ![image-20231114003218175](../notes-images/202311140032328.png)

* ![image-20231114003243718](../notes-images/202311140032787.png)

##### 12. 程序控制结构

* 用next()输入字符串，相当于C语言中的scanf()，对输入有效字符之前遇到的空格键、Tab键或Enter键等结束符，next（）方法会自动将其去掉，只有在输入有效字符之后，next（）方法才将其后输入的空格键、Tab键或Enter键等视为分隔符或结束符，所以next方法不能得到带空格的字符串。

  scanner.next()返回字符串

  ![image-20231114003434381](../notes-images/202311140034437.png)

* 错误：不兼容的数据类型：string无法转化成char

  ![image-20231114003553750](../notes-images/202311140035797.png)

* ![image-20231114003626240](../notes-images/202311140036299.png)

* ![image-20231114003659332](../notes-images/202311140036383.png)

* ![image-20231114003725363](../notes-images/202311140037414.png)

* ![image-20231114003746648](../notes-images/202311140037724.png)

* ![image-20231114003815176](../notes-images/202311140038296.png)

##### 13. 数组、排序和查找

![image-20231114003950653](../notes-images/202311140039741.png)

![image-20231114004013438](../notes-images/202311140040509.png)

![image-20231114004049391](../notes-images/202311140040461.png)

![image-20231114004104167](../notes-images/202311140041224.png)

![image-20231114004118515](../notes-images/202311140041592.png)
