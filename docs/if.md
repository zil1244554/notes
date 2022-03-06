# if语句
基本语法：  
```python
if 条件:  
    指令A  
else:  
    指令B    
```
用中英直译就是：  
**如果条件成立，就执行指令A。否则执行指令B**  
举个例子：
比如如何判断一个数是否大于0  
就可以这样写  
```python
a=int(input()) # 输入一个数
if a > 0:
    print("a大于0")
else:
    print("a不大于0")
```
来一行一行解释下  
第一行
```python
if a > 0:
    print("a大于0") 
# 判断a是否大于0,如果大于0就打印"a大于0"
```

第二行
```python
else:
    print("a大于0")
# 否则，打印"a大于0"
```