## for语句  
基本语法:  
```python
for 变量名A in 循环体A:
    命令A
```
中英直译:  
**声明一个变量A,A的循环范围在循环体A中，执行命令A直到循环体循环结束**  
循环体一般都是用range  
举个例子:  
输入一个变量n，求1到n之间所有基数的和  
我们就可以这样写  
```python
n = int(input())
sum = 0
for i in range(1,n+1,2):
	sum = sum + i
print(sum)
```
插入一下range的意思:
举几个例子对照一下很快就知道了  
```bash
range(1,5)		1,2,3,4
range(4,10) 	4,5,6,7,8,9
range(1,10) 	1,2,3,4,5,6,7,8,9
range(2) 		0,1,2
range(5) 		0,1,2,3,4
```
range的步长  
range()的括号里面可以有三个数据，而第三个数据代表的是步长，这里举几个例子
```bash
range(1,5,2)	1,3
range(1,10,2)	1,3,5,7,9
range(1,20,2)	1,3,5,7,9,11,13,15,17,19
range(1,10,3)	1,4,7
range(0,10,2)	0,2,4,6,8
```  
总结一下:
**range的第一二个数据构成一个闭开区间，第三个数据代表步长，也就是从第一个数据开始每次加几**  
注：每个人都有自己的理解，按照自己的理解来就行了  

然后我们来一行一行解释下什么意思  
```python
n = int(input())
# 输入一个变量n，为正整数
sum = 0
# 初始化变量n
for i in range(1,n+1,2):
	sum = sum + i
# 声明一个变量i，变量i的值是在1到n之间的奇数
# 注：因为range是一个左闭右开的区间，所以右边的数要加上1，因为我们要求得是奇数，所以步长设置为2
print(sum)
# 输出sum的值
```  

如果实在理解不了步长我们也可以用取模运算  
```python
n = int(input())
sum = 0
for i in range(1,n+1):
	if i % 2 == 1:
		sum = sum + i
print(sum)
```

相信大家肯定还没有理解，所以再举几道例题:
```python
输入一个正整数n，求1到n之间的偶数的总和
输入
10
输出
24
```
捋一下思路:
1.因为他让我们输入一个正整数，所以我们可以直接把n的赋值语句写下去
```python
n = int(input())
```
2.求1到n之间的数的和时就可以用到for语句。又题目要求要求总和，所以先初始化一下变量sum，用来保存总和
```python
n = int(input())
for i in range(0, n+1, 2):
	sum = sum + i
# 因为是偶数，所以我们把range的第一个数据往前移一个数，这样输出的就都是偶数了
```
3.输出最后的结果
```python
n = int(input())
for i in range(0, n+1, 2):
	sum = sum + i
print(sum)
```

运行一下发现结果正确  
接下来给出几道例题，可以自己试做一下  


```bash
输入一个正整数n，求1到n之间奇数的个数
样例：
输入
10
输出
5
```
```bash
输入一个正整数n,求1到n之间3的倍数的个数
样例：
输入
10
输入
3
```
```bash
求出1到n之间能够同时被3和5整除的数的总和
样例：
输入
40
输出
45
```
```bash
求出1到n之间能够被4整除的数的个数
样例：
输入
20
输出
5
```

题目讲解3月11日发


## 最最最无脑版  
直接背公式  
```python
for i in range(字母1,字母2,字母3):
	sum = sum + i
如果题目是说什么到什么之间的数的和或者个数，直接上for循环  
直接背公式
如果是从1开始，把字母1改成1，如果是2开始，把字母1改成2
字母2改成结尾的数加1  
字母3不用管
如果理解不来步长就用取模大法  
if n % 2 == 0:
	sum = sum + i
```  
  
## for语句课后习题讲解  
### 第一题  
1.首先题目让我们输入一个正整数,我们就可以先写
```python
n = int(input())
```
2.然后让我们求1到n之间的奇数和，求一个区间内的数据，所以要用到for语句，然后是要求奇数,最后是要求个数，所以我们要先初始化一个变量来保存个数。
```python
n = int(input())
geshu = 0
for i in range(1,n+1):
	if i % 2 == 1:			#取i除以2的余数，判断i是否为奇数
		geshu = geshu + 1	#如果是，就把geshu这个变量加上1
```
3.最后在输出geshu这个变量的数
```python
n = int(input())
geshu = 0
for i in range(1,n+1):
	if i % 2 == 1:
		geshu = geshu + 1
print(geshu)
```
### 第二题  
1.跟大部分一样，让输入一个正整数
```python
n = int(input())
# 基本可以当公式记
```
2.有一个区间，所以用for语句，用取余3，判断是否能被3整除，是的话个数加1
```python
n = int(input())
geshu = 0
# 记得先初始化变量
for i in range(1, n+1):
	if i % 3 == 0:
		geshu = geshu + 1
```
3.最后输出结果
```python
n = int(input())
geshu = 0
for i in range(1, n+1):
	if i % 3 == 0:
		geshu = geshu + 1
print(geshu)
```
注释：记得在最前面初始化一个变量来统计个数  
### 第三题  
1.先输入一个正整数n
```python
n = int(input())
```
2.先求出1到n之间能同时被3和5整除的数
```python
n = int(input())
for i in range(1, n+1):
	if i % 15 == 0:
# 因为能被3和5同时整除的数都是15的倍数，所以我们可以直接判断是否能被15整除
```
另外还有两种写法  
第一种  
```python
for i in range(1, n+1):
	if i % 3 == 0:
		if i % 5 == 0:
# 这里先判断i是否是3的倍数，如果是就再判断i是否是5的倍数
```
第二种
```python
for i in range(1, n+1):
	if i % 3 == 0 and i % 5 == 0:
# 这里用到了逻辑运算符and，当两边同时成立时，才执行属于if的指令
```
3.初始化一个变量来保存个数的值
```python
n = int(input())
geshu = 0
for i in range(1, n+1):
	if i % 15 == 0:
		geshu = geshu + 1
```
4.输出结果
```python
n = int(input())
geshu = 0
for i in range(1, n+1):
	if i % 15 == 0:
		geshu = geshu + 1
print(geshu)
```
### 第四题  
1.先输入一个正整数n  
```python
n = int(input())
```  
2.求1到n之间能被4整除的个数  
> 因为是1到n之间（一个区间），所以可以用for语句  
> 因为求能被4整除  
> 个数  
```python
n = int(input())
geshu = 0 # 先初始化变量geshu，用来统计个数
for i in range(1, n+1):
	if i % 4 == 0:
		geshu = geshu + 1
```
3.最后再输出结果
```python
n = int(input())
geshu = 0
for i in range(1, n+1):
	if i % 4 == 0:
		geshu = geshu + 1
print(geshu)
```  

总结：for语句要注意range的使用，range是一个左闭右开的区间。看好是求总和还是求个数