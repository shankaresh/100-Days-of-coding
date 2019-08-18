## Given a list of numbers, find and print all its elements that are greater than their left neighbor.
```
Example input
1 5 2 4 3

Example output
5 4
```
```
# Read a list of integers:
a = [int(s) for s in input().split()]
# Print a value:
i = 0
while i < len(a):
  if a[i] > a[i-1] and i > 0:
    print(a[i], end=" ")
  i += 1
```
