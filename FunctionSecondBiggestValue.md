## Second Biggest Value
Write a function second_biggest_value which accepts three integers, and does the following:

- returns the second biggest value among the three

- returns “NA” if there are two or more equal values

Come up with a solution which does not use sorting!

## Example
```
(1, 2, 3) -> 2
(3, 1, -1) -> 1
(3, 5, -1) -> 3
(3, -1, -1) -> "NA"
```
```
def second_biggest_value(int1,int2,int3):
  if (int1<int2<int3) or (int3<int2<int1):
    return int2
  elif (int2<int1<int3) or (int3<int1<int2):
    return int1
  elif (int2<int3<int1) or (int1<int3<int2):
    return int3
  else:
    return ("NA")
```
