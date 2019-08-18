## Given a list of numbers, determine and print the number of elements that are greater than both of their neighbors.
```
The first and the last items of the list shouldn't be considered because they don't have two neighbors.

Example input
1 5 1 5 1

Example output
2

```
```
# Read a list of integers:
# a = [int(s) for s in input().split()]
# Print a value:
x = input()
list_x = list(map(int, x.split()))
tally = 0
for n in range(1,len(list_x)-1):
  if list_x[n-1] < list_x[n] and list_x[n] > list_x[n+1]:
    tally = tally + 1
print(tally)
```
