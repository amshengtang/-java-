# 数组中的操作
## 1. for each用于遍历数组中的所有元素，算是一个语法糖
```JAVA
public class test
{
    public static void main(String[]args) 
    {
        int[]a=new int[5];
        for(int i=0;i<a.length;i++)
            a[i]=i;
        for(int b:a)
        {
            System.out.println(b);
        }
    }
}
```

## 2. 数组的深拷贝
```JAVA
import java.util.Arrays;
public class test
{
    public static void main(String[]args) 
    {
        int[]a=new int[5];
        for(int i=0;i<a.length;i++)
            a[i]=i;
        int[] b=Arrays.copyOf(a, a.length*2);//目标数组名=Arrays.copyOf(拷贝数组名，目标数组长度)
        for(int i:b)
            System.out.println(i);
    }
}
```

## 3.数组的排序
```JAVA
Arrays.sort(a)//a是待排序数组名
```