## Given a list of non-zero integers, find and print the first adjacent pair of elements that have the same sign. If there is no such pair, print 0.
```
Example input #1
-1 2 3 -1 -2

Example output #1
2 3

Example input #2
1 -3 4 -2 1

Example output #2
0
```
```
# Read a list of integers:
n = input()
list_n = list(map(int, n.split()))
i = 1
for i in range(1,len(list_n)):
  if list_n[i]*list_n[i-1]>0:
    print(str(list_n[i - 1])+' '+str(list_n[i]))
    break
  elif i == len(list_n)-1:
    print("0")
```
