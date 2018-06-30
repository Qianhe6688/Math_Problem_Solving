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
        

                
                
