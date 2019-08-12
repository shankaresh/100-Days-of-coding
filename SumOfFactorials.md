## In mathematics, the factorial of an integer n, denoted by n! is the following product:
n! = 1 × 2 × … × n

For the given integer n calculate the value 

1! + 2! + 3! + ... + n!

Try to discover the solution that uses only one for-loop. And don't use math module in this exercise.
```
Example input
4

Example output
33
```
```
# Read an integer:
N = int(input())
fact =1
fact_sum=0

for i in range (1,N+1):
  fact *= i
  fact_sum += fact
# Print a value:
print(fact_sum)
```
