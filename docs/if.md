## if语句
基本语法：  
```python
if 条件:  
    指令A  
else:  
    指令B    
```
用中英直译就是：  
**如果条件成立，就执行指令A。否则执行指令B**  
注:if和else下面那个空格不能省略  
而且else后面没有跟条件  
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

再举几个例题  
```bash
输入两个正整数a,b。判断a的值是否大于b,如果大于就输出大于，否则就输出不大于
样例
输入
5
3
输出
大于

输入
4
6
输出
不大于
```
捋一下做题的思路  
1.它让我们输入两个正整数a,b所以我们就可以直接先写  
```python
a = int(input())
b = int(input())
```
2.然后他让我们判断a>b，我们就可以用到判断语句if
```python
if a > b:
    print("大于")
else:
    print("不大于")
# 注解：if和else最后面要冒号，否则就会报错
```
3.因为a大于b和不大于只有两种情况，所以我们可以直接if和else  

全部合起来我们就可以这样写
```python
a = int(input())
b = int(input())
if a > b:
    print("大于")
    # 判断a是否大于b，是就输出
else:
    print("不大于")
```

运行一下看看结果  
![](https://note.youdao.com/yws/api/personal/file/WEB58e47d80710e74c4bf095605a1c66e0f?method=download&shareKey=f2038e5086a73b3d2413319c8980b88b)  
![](https://note.youdao.com/yws/api/personal/file/WEB3d25bf7b8230e9166dd0375c018121f3?method=download&shareKey=adbce944857846cac70e5739937d66ae)  

补充几道练习题  
```bash
输入代码，判断输入的数是否是偶数，如果是，输出“偶数”，否则“输出奇数”
输入
10
输出
偶数
```  


***  
# 多分支的if语句  
基本语法:
```python
if 条件A:
	指令A
elif 条件B:
	指令B
elif 条件C:
	指令C
elif 条件D:
	指令D
```  
中英直译:  
**如果条件A成立，就执行指令A，如果条件B成立，就执行指令B，如果条件C成立，就执行指令C，如果条件D成立就执行指令D**  
以此类推  
举几个例题  
```bash
小明输入一个正整数代表自己的成绩，判断小明成绩的档次  
(85<A<100, 75<B<85, 60<C<75, D<60)
输入
99
输出
A
```
```bash
编写代码，实现：判断a是否能被b整除，如果能够被整除，则输出a除以b的值，若不能，则输出a取模b的值
输入
5
3
输出
2

输入
12
4
输出  
3
```  
第一题在学校里已经做过了，这边还是再做一遍  
1.先输入一个正整数
```python
n = int(input())
```
2.判断小明成绩的档次，因为有多个分支（多种情况），所以要用多分支的if语句  
```python
n = int(input())
if n>85:
    print("A")
    # 判断n(小明的成绩)是否在A的范围，如果是就输出A
elif 75 < n < 85:
    print("B")
    # 判断n(小明的成绩)是否在B的范围，如果是就输出B
elif 60 < n < 75:
    print("C")
    # 判断n(小明的成绩)是否在C的范围，如果是就输出C
elif n < 60:
    print("D")
    # 判断n(小明的成绩)是否在D的范围，如果是就输出D
```

***
### 答案  
### if分支:第一题  
```python
a = int(input())
if a % 2 == 0:
    print("偶数")
else:
    print("奇数")
```
注:答案不唯一，只要能得出样例输出就行，答案仅供参考  
