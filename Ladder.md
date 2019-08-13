## For given integer n ≤ 9 print a ladder of n steps. The k-th step consists of the integers from 1 to k without spaces between them.
To do that, you can use the sep and end arguments for the function print().
```
Example input
3

Example output
1
12
123
```
```
# Read an integer:
number = int(input())
x=0
# Print a value:
if(number<=9):
  for x in range (1,number+1):
    for i in range(1,x+1):
      print(i,end="")
    print("")
```
