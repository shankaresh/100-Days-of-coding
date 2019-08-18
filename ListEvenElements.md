## Given a list of numbers, print all its even elements. Use a for-loop that iterates over the list itself and not over its indices. That is, don't use range()
```
Example input
1 2 2 3 3 3 4

Example output
2 2 4
```
```
# Read a list of integers:
a = [int(s) for s in input().split()]
# Print a value:
for elem in a:
    if elem % 2 == 0:
        print(elem,end=" ")
```
