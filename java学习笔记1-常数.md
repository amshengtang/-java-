# java学习笔记1-常数
## 1.常数的定义
使用**final**标识符，表示这个变量仅能被赋值一次

demo:
```java
public class Constants 
{   
    public static void main(String[] args)   
    { 
        final double CM_PER_INCH = 2.54;      
        double paperWidth = 8.5;      
        double paperHeight = 11;      
        System.out.println("Paper size in centimeters: " + paperWidth * CM_PER_INCH + " by " + paperHeight * CM_PER_INCH);   
    } 
} 
```


demo:
```java
public class Constants2 
{    
    public static final double CM_PER_INCH = 2.54;
    public static void main(String[] args)    
    {
        double paperWidth = 8.5;       
        double paperHeight = 11;      
        System.out.println("Paper size in centimeters: " + paperWidth * CM_PER_INCH + " by " + paperHeight * CM_PER_INCH);    
    } 
}
```
这样的话定义在method的外面，所有其他的method都能访问这个常数
