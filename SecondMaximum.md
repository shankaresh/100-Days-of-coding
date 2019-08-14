## Given a sequence of distinct non-negative integers, where each number is written in a separate line. The sequence ends with 0. Print the second largest element in this sequence. It is guaranteed that the sequence has at least two elements.
```
Example input
1
7
9
0

Example output
7
```
```
li=[]
while True:
  temp=int(input())# Read an integer:
  li.append(temp)
  if temp==0:
    li.sort(reverse=True)
    print(li[1])# Print a value:
    break
```
