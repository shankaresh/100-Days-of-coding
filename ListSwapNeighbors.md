## Given a list of numbers, swap adjacent elements in each pair (swap A[0] with A[1], A[2] with A[3], etc.). Print the resulting list. If a list has an odd number of elements, leave the last element intact.
```
Example input
1 2 3 4 5

Example output
2 1 4 3 5
```
```
# Read a list of integers:
x = input()
li = list(map(int, x.split()))
# Print a value:
for i in range(0, len(li), 2):
  popval = li.pop(i)
  li.insert(i+1, popval)
print(li)
```
