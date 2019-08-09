## Given a three-digit number. Find the sum of its digits.
```
Example input
123

Example output
6
```
```
# Read an integer:
a = int(input())
# Print a value:
sum=0
while(a>0):
  remainder=a%10
  sum = sum+remainder
  a=a//10
print(sum)
```
