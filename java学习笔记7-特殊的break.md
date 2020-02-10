# 跳出多重循环的break
举个小例子就ok了
```Java
public class test
{
    public static void main(String[]args) 
    {
        break_point://必须在多重循环前面且以":"结尾
        while(true)
        {
            while(true)
            {
                int n=-1;
                if(n<0)
                break break_point;//跳出双重循环
            }
        }
    }
}
```