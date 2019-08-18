## Given a list of numbers, find and print all its elements with even indices (i.e. A[0], A[2], A[4], ...).
```
Example input
5 6 7 8 9

Example output
5 7 9
```
```
# Read a list of integers:
a = [int(s) for s in input().split()]
# Print a value:
print(a[0::2])
```
