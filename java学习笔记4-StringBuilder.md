# StringBuilder
## 使用范围：
在我们需要多次重复改变String的时候，使用String中自带的method效率会变得很低(每一次都会创建一个新的object)
这时候我们可以使用StringBuilder（由动态数组实现，效率较高）

## 使用方法：
### 1. 构造：
```JAVA
StringBuilder builder = new StringBuilder(); 
```

### 2. 常用method 
#### append---向尾部添加char或者string
#### toString()---转化为String