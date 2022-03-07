# 基础数据类型  
数据的类型大致分为3类  
+ int 代表的是整数，也就是整形  
+ float 代表的是小数，也就是浮点型  
+ str 代表的是字符串  
举个例子  
尝试下运行这两行代码  
```python
a = int(input())
b = int(input())
c = a + b
print(c)
```
```python
a = str(input())
b = str(input())
c = a + b
print(c)
```
看看结果有什么不同  
我们可以很直观的看到输出结果的不同  
![](https://note.youdao.com/yws/api/personal/file/WEB135f69fd3a2b3a660879bbc7fcc71927?method=download&shareKey=fa85608a6bf2a0d16375b87d8c59dc1c)  
![](https://note.youdao.com/yws/api/personal/file/WEBafba6890066fb724488a2c2795ba4812?method=download&shareKey=f7a1d86dfd4a58c3531f1d4287787e7c)  
这样一对比我们就可以看出  
**字符串只会将变量进行组合，而不会进行数学运算，整形则反之**  
float就是小数用整形类比就能知道了  
了解下基本的数据类型，没什么例题能做的。。