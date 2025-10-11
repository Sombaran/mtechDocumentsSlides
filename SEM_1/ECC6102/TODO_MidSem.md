'''
#tup=(1,2,3)
for i in range(1, 5, 2):
    for j in range(i):
        print(j, end=" ") 
    print()


i=4
while i>1:
    print(i,end=" ")
    i-=1


x=-5
y=10
if x>0 or y>0:
    print ("1")
else:
    print("2")
 
d = {'a': 1, 'b' :2}
for key in d:
    print(key, d[key] * 2)
  
tup = (1,2,3)
for i in tup:
    print(i * 3, end=' ')
  
d={'a' : 1,'b' : 2}  
print (d.keys())



lst =[1,2,3]
for i in lst:
    if i % 2 != 0:
        print (i)
        


lst = [1,2,3]
if 4 in lst:
    print("1")
else:
    print("2")
    

for i in range (1,6):
    if i%2 == 0:
        continue
    print(i,end=" ")
    
    
i=1
while i<10:
    if i % 3 ==0:
        i+=2
    print(i, end=" ")
    i+=1


d={'a':1,'b':2}
for key in d:
    print (key,d[key])
    
    
d={'a':1,'b':2}
print(d.values())
    

tup=(1,2,3)
print (tup [1:3])
 
d={'a':1,'b':2}
d.update({'b':3})
print(d)

i=0
while i<4:
    print(i,end='')
    i+=1

lst=[1,2,3]
lst.insert(1,4)
print(lst)


x=5
while x>=0:
    x-=1
    if x==2:
        break
    print(x,end= " ")
else:
    print("loop completed")


for i in range (3):
    for j in range(3,i,-1):
        print("*", end= " ")
    print()


lst = [1,2,3]
for i in lst:
    print(i* 2, end=' ')

d={'a':1,'b':2}
print(d.get('c',3))
x=10
while x > 0:
    print(x, end = " ")
    x+=1
i=3
while i>0:
    print(i, end='' )
    i-= 1
'''
x=10
y=5
if x>0 and y<10:
    print ("1")
else:
    print("2")


    