## Optimize Tile Size
Imagine you want to tile a rectangle floor. You approach a tile manufacturer to produce tiles for you.
- The tile manufacturer can produce only square tiles
- He is willing to custom make them for you, but you can pick only one size
- The bigger they are, the less expensive they will be

- For example, if you order 5x5 tiles, they will be lot less expensive than 1x1 tiles
- You want to ensure every part of the floor is covered  (i.e. there are no holes or gaps)
- You want to select tiles of dimension such that there is no need for breaking them

Write a function tile_solve to calculate the optimum tile dimension.

Use RECURSION to simplify the code logic.
```
Example
tile_solve(10, 5)     -> 5 
tile_solve(6, 4)      -> 2 
tile_solve(1071, 462) -> 21 
```
```
def tile_solve(length, breadth):
  # your code goes below
  if length> breadth:
    s=breadth
  else:
    s= length
  for i in range(1,s+1):
    if (length%i==0) and (breadth%i==0):
      count=i
  return count
```
