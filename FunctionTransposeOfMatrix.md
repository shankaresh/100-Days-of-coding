## Transpose a Matrix
Perform a transpose of the matrix given. 
If the input matrix is **ill-formed**, use 0 for the fill value. 

For example,
```
[[1], 
 [2, 3, 4], 
 [5, 6]
] => 

[[1, 0, 0], 
 [2, 3, 4], 
 [5, 6, 0]
]
```

### EXAMPLE 
~~~
transpose_matrix([[1, 2], [3, 4]]) -> [[1, 3], [2, 4]]

transpose_matrix([[1, 2], [3]) -> [[1, 3], [2, 0]]

transpose_matrix([[1, 2, 3], 
                 [4, 5, 6], 
                 [7, 8, 9]]) -> 

[[1, 4, 7],[2, 5, 8], [4, 6, 9]]
~~~

### SOLUTION GUIDELINE
Provide a solution that does in-place transpose of the input matrix. 
Do not return a new nested list.

### PROGRAM
```python
import itertools
def transpose_matrix(uneven):
  copy= [list(i) for i in itertools.zip_longest(*uneven,fillvalue=0)]
  rows = len(copy)
  cols = len(copy[0]) if rows else 0
  for i in range(rows):
    for j in range(cols):
      try:
        uneven[i][j] = copy[i][j]
      except:
        if i > len(uneven)-1:
          uneven.append([copy[i][j]])
        else:
          uneven[i].append(copy[i][j])
    uneven[i][:] = uneven[i][:cols]#set cols limit len
  uneven[:] = uneven[:rows]#set rows limit len
  return uneven
```
