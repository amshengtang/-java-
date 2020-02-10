# 输入输出
## 1.输入
对于输入，我们首先需要import一个package
```java
import java.util.*;
```

其次我们需要构造一个对象，用Scanner类来进行构造
```java
Scanner in=new Scanner(System.in);//现在不知道为什么要将System.in作为参数
```

对象构造完成后，我们就可以利用这个对象来读取信息了
```java
int a=in.nextInt();
double b=in.nextDouble();
```

当然还有一些判断函数
```JAVA
in.hasNext();
in.hasNextInt();
in.hasNextDouble();
```

## 2.输出
输出比较简单要么是
```java
System.out.print()//无格式
System.out.printf()//有格式，同C语言
```
值得一提的是**String.format**可以用来构造格式化的String
```java
String message = String.format("Hello, %s. Next year, you'll be %d", name, age);
```
