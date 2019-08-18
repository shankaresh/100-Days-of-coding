## Given a list of numbers with all elements sorted in ascending order, determine and print the number of distinct elements in it.
```
Example input
1 2 2 3 3 3

Example output
3

```
```
# Read a list of integers:
# a = [int(s) for s in input().split()]
# Print a value:
x = input()
lst = list(map(int, x.split()))
total = 1
for i in range(1, len(lst)):
  if lst[i-1] != lst[i]:
    total += 1
print(total)
```
