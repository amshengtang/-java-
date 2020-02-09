# 初探String
## 1.提取substring  
方法：使用substring函数  
```java
String greeting = "Hello"; 
String s = greeting.substring(0, 3); 
```
注:substring(a,b)是前闭后开

## 2.string的concatenate
方法：使用“+”
```java
String expletive = "Expletive"; 
String PG13 = "deleted"; 
String message = expletive + PG13;
```

## 3.升级版的concatenate
方法:使用String.join("分隔符","String1","String2"...)
```java
public class test
{
    public static void main(String[]args)
    {
        System.out.println(String.join("  分隔符  ", "I","like","code"));
    }
}
```
结果: I  分隔符  like  分隔符  code. 

## 4.String是immutable的
### 具体含义：
不能修改一个变量指向的String的具体内容
例如
```java
String s="String is immutable";
```
我们不能直接修改成
```java
String s="String is not immutable";
```
我们只能改变s所指向的String对象，但我们不能改变String对象的具体内容，"String is immutable"是不能改变的
我们只能通过substring和"+"再造一个String，从而让s指向它
#### 好处:
编译器可以让一个String对象被多个String变量所指向，不用担心一个变量改变了String对象的具体内容导致其他变量所指向的
String对象内容都改变
#### 坏处:
效率较低，想要改变一个String变量所指向的内容就得造一个新的String对象

## 4.测试String是否相等
采用String.equals
```java
s.equals(t);
```
不分大小写的话:
```JAVa
"Hello".equalsIgnoreCase("hello")
```
注意：不能用“==”来判断是否相等
这里的“==”只能判断两个字符串的内存位置是否相等
有时我们会创建多个内容一样但内存位置不同的string

## 5.获取string中的编码值 (code point)
```JAVA
public class test
{
    public static void main(String[]args)
    {
        String greeting = "Hello";
        int i=3;
        int cp = greeting.codePointAt(i);
        System.out.print(cp);
    }
}
```
结果 108
