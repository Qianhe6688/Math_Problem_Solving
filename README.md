# 问题 1：求解1,2,3,4四个数字可以组成多少个互不相同且无重复数字的三位数？

for i in range(1,5):
    for j in range(1,5):
        for k in range(1,5):
            if (i != k) and (i != j) and (j != k):
                print (i,j,k)
                
                
                
