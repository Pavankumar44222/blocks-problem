# blocks-problem
A problem on blocks in Python in Hackerrank.
for _ in range(int(input())):
    n=int(input())
    l=list(map(int,input().split()))
    k,m=l.copy(),l.copy()
    m.sort()
    m.reverse()
    k.sort()
    b=1
    if(k==l):
        print("Yes")
    elif(m==l):
        print("Yes")
    else:
        for i in range(len(l)):
            if(l[i]>=l[i+1]):
                b+=1
            else:
                break
        # print(i)
        for a in range(i,len(l)-1):
            if(l[a]<=l[a+1]):
                b+=1
        if(b==len(l)):
            print("Yes")
        else:
            print("No")
        
