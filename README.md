# assignment-1-13-05-2022
import math
n=int(input('enter n value:'))
seive=[]
for i in range(n+1):
    seive.append(True)
seive[0]=seive[1]=False
x=int(math.sqrt(n))
for i in range(2,x+1):
    if seive[i]:
        for j in range(i*i,n+1,i):
            seive[j]=False
for i in range(n+1):
    if seive[i]:
        print(i)
