## N numbers are given in the input. Read them and print their sum.
The first line of input contains the integer N, which is the number of integers to follow. Each of the next N lines contains one integer. Print the sum of these N integers.
```
Example input
10
1
2
1
1
1
1
3
1
1
1

Example output
13
```
```
# Read an integer:
N = int(input())
number=0
# Print a value:
for i in range(0,N):
  number += int(input())
print(number)
```
