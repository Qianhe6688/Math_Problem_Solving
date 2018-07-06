
# math problem solving
# 问题 1：求解1,2,3,4四个数字可以组成多少个互不相同且无重复数字的三位数？

for i in range(1,5):
    for j in range(1,5):
        for k in range(1,5):
            if (i != k) and (i != j) and (j != k):
                print (i,j,k)
                
                
# 问题 2：关于数轴/长整型编程练习
i = int(input('净利润：'))
arr = [1000000,600000,400000,200000,100000,0]
rat = [0.01,0.015,0.03,0.05,0.075,0.1]
r = 0
for idx in range(0,6):
    if i > arr[idx]:
        r += (i - arr[idx])*rat[idx]
        print ((i-arr[idx])*rat[idx])
        i = arr[idx]
print (r)

# 问题 3：一个整数加上100和加上268都是完全平方数，求解该数字

import math

for i in range(10000):
    # 转化为整型值
    x = int(math.sqrt(i + 100))

    y = int(math.sqrt(i + 268))

    if (x*x == i + 100) and (y*y == i + 268):
    
        print (i)
        
 # 问题 4：输入年月日，判断输入日期是当年中的第几天

year = int(input('year:\n'))

month = int(input('month:\n'))

day = int(input('day:\n'))

months = (0,31,59,90,120,151,181,212,243,273,304,334)

if 0 < month <= 12:
    
    sum = months[month -1]
    
else:
    
    print ('data erroe')
    
sum += day

leap = 0 # www.iplaypy.com

if (year % 400 == 0) or ((year % 4 == 0) and (year % 100 != 0)):
    
    leap = 1
    
if (leap == 1) and (month > 2):
    
    sum += 1
    
print ('it is the %dth day.' % sum)


# 问题 5：任意三个整数排序

l = []


for i in range(3):
    
    x = int(input('integer:\n'))
    
    l.append(x)
    
l.sort() #sort()函数默认的是从小到大排序

print(l)

# 问题 6：斐波那契数列

# method.1
def recur_fibo(n):
    
    """递归函数
    输出斐波那契数列"""
   
    if n <= 1:
        
        return n
    
    else:
        
        return(recur_fibo(n-1) + recur_fibo(n-2))
        
# 获取用户输入

nterms = int(input("您要输出几项？"))

# 检查输入的数字是否正确

if nterms <= 0:
    
    print ("输入正数")
    
else:
    
    print ("斐波那契数列")
    
    for i in range(nterms):
        
        print (recur_fibo(i))

        
# 问题 7：列表数据复制

x = [1,2,3]

y = x[:]

print (y)
                
 
# 问题 8：乘法口诀计算，输出9*9乘法表

for i in range(1,10):
    
    for j in range(1,i + 1):
        
        print ("{} x {} = {}\t".format(i,j,i*j),end = "")         


# 问题 9：time.sleep方法的使用，让Python暂停预定时间后再运行

import time

myD = {1:'a',2:'b'}

for key,value in dict.items(myD):
    
    print (key,value)
    
    time.sleep(5) # 5为暂停时间的秒数


# 问题 10：python时间格式化

import time

print (time.strftime('%Y-%m-%d %H:%M:%S',time.localtime(time.time())))

#暂停一秒

time.sleep(1)

print (time.strftime('%Y-%m-%d %H:%M:%S',time.localtime(time.time())))



#问题11 ：兔子生兔子算法问题（斐波那契数列）

a1 = 1

b2 = 1

for i in range(1,21):
    
    print ('%12ld %12ld' % (a1,b2))
    
    if (i % 3) == 0:
        
        print ('')
        
    a1 = a1 + b2
    
    b2 = a1 + b2


























