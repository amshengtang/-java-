# 文件的输入输出

## 1.输入
实例代码
```JAVA
Scanner in=new Scanner(Paths.get("Mytext.txt"),"UTF-8");
```
注意Path.get不能漏，指定编码不能漏
之后就可以像标准读取一样使用它

**还有很重要的一点：使用Paths.get的时候一定要import一个头文件**
```JAVA
import java.nio.file.Paths;
```

**一个完整的读取代码**
```JAVA
import java.util.*;
import java.io.IOException; 
import java.nio.file.Paths;
public class test
{
    public static void main(String[]args)  throws IOException//这个是告诉编译器你意识到了会有发生IOException的可能性
    {
        Scanner in=new Scanner(Paths.get("a.txt"),"UTF-8");
        int a=in.nextInt();
        int b=in.nextInt();
        System.out.print(a+" ");
        System.out.print(b);
    }
}
```

## 2.输出
和输入一样我们也需要定义一个对象
```java
PrintWriter out=new PrintWriter("文件名");
```
之后我们就可以像system.out那样向文件输出信息
另外还需注意一点，文件写入完后必须关闭，否则内容读不进去
```java
out.close()
```
```JAVA
import java.io.PrintWriter;
import java.io.FileNotFoundException;

public class test
{
    public static void main(String[]args) throws FileNotFoundException
    {
        PrintWriter out=new PrintWriter("a.txt");//不能encode?
        out.print(1000);
        out.close();//必须关闭
    }
}
```
