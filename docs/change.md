# 赋值语句  
基本语法:
```python
变量名 = 表达式（或者一个数值）
举例
a = 0 # a的值为零
a = int(input()) # 把输入的正整数的值赋值给a
```
**赋值语句是从右往左赋值的**   
把右边的值赋值给左边的变量  

下面的可以后面回过头来看  
***
因为赋值语句的东西比较少，讲一些零散的知识点  
有的人会很奇怪，为什么for和if那边，print前面有一个长长的空格
```python
if a = b:
	print("1")
else:
	print("2")
```
这个空格的名字叫做缩进，长度是按一下tab键，也就相当于是四个空格  
缩进表示下面的代码是属于if这个分支里面的  
比如上面的
```python
if a = b:
	print("1")
```
这时就表示print("1")是属于if这个分支里面的，当if成立时才运行print  
这有点像古代的身份高低，顶格的代表身份最高，一个缩进的代表身份低一等，两个的代表再低一等，以此类推，当最高身份的人条件达成时，才能够让下面的代码人运行，只有当上级成立时，下级才能够运行。  
这边举几个具体的例子  
![](https://note.youdao.com/yws/api/personal/file/WEB5f5d2640816d1b413c9bb7dfed444e81?method=download&shareKey=b486a53bcc536aa4bd3b060df5ceca7d)  
对比一下就能很清楚的知道了  
![](https://note.youdao.com/yws/api/personal/file/WEBb4f87c757b56e47e484bb29cffc469f7?method=download&shareKey=b27bb7bf7de4d4601e1c2b38095ff353)

在使用for语句的时候有的人可能会把print放在for循环下面，我们可以试着运行试试
```python
n = int(input())
sum = 0
for i in range(1,n+1):
	sum = sum + i
	print(sum)
```
我们试着运行下，发现结果不只一个，sum输出了他每次的值  
![](https://note.youdao.com/yws/api/personal/file/WEB2bbf9a9dd9649fac4ac07ab68f7ddd7a?method=download&shareKey=c6a6a8438ed3230efb3673630a84d19d)  
我们再来对比下  
![](https://note.youdao.com/yws/api/personal/file/WEB808f71aca7777793ec0bf94fb3944955?method=download&shareKey=a24492e68515ddc5bf7804db7dd9322e)  
这是因为for语句这个循环会运行很多次用来计算总和，而print(sum)前面有一个缩进，被误判为是for语句里面的，所以for语句运行几次，他也就输出几次sum的值
而我们只要输出一个值，也就是sum最后的值  
* 注：实在不懂看题目，如果输出只有一个就放外面，多个放里面（不过具体还是得看题目，土办法只能应对大多数情况）