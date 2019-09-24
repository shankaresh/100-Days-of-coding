## Convert Nested Lists to Matrix
Write a function that accepts a nested list as an argument. 
It must return a well formed matrix using the nested list. 

The nested list may have lists that contain varied number of elements.
Balance out the rows in the matrix so that all rows are equal to the longest 
row in the nested list. Use fillvalue 0 to populate the rows accordingly. 

> ***Example*** 
```
convert_to_matrix([[1, 2]])    -> [[1, 2]]
convert_to_matrix([[1], [2, 3]]) -> [[1, 0], [2, 3]]
convert_to_matrix([[1], [2, 3], [4, 5, 6]]) -> 
  [[1, 0, 0], 
   [2, 3, 0],
   [4, 5, 6]]
```
> ***Where is the bug?***
The code for the function is already provided. But it does not work properly. 
Fix it. 

> ***CLUE:*** You only have to change one line, and the logic will get corrected. 

```python
def convert_to_matrix(alist):
  
  len_of_max_list = len(max(alist,key=len)) if alist else None
  
  for row in alist:
    row.extend([0]*(len_of_max_list - len(row)))

  print(alist)
  return alist
```
