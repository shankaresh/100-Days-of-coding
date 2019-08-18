## Given a list of distinct numbers, swap the minimum and the maximum and print the resulting list.
```
Example input
3 4 5 2 1

Example output
3 4 1 2 5
```
```
# Read a list of integers:
li = list([int(s) for s in input().split()])
# Print a value:
maxi, mini = li.index(max(li)), li.index(min(li))
li[maxi], li[mini] = li[mini], li[maxi]
print(li)
```
