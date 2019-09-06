## Optimize Tile Size with Constraint
Imagine you want to tile a rectangle floor. You approach a tile manufacturer to produce tiles for you.
- The tile manufacturer can produce only square tiles
- He is willing to custom make them for you, but you can pick only one size
- The bigger they are, the less expensive they will be

- For example, if you order 5x5 tiles, they will be lot less expensive than 1x1 tiles
- You want to ensure every part of the floor is covered  (i.e. there are no holes or gaps)
- You want to select tiles of dimension such that there is no need for breaking them

Write a function tile_solve to calculate the optimum tile dimension, which accept a 3rd parameter, which when not provided, defaults to value of 1. 

Use RECURSION to simplify the code logic.
```
Example
tile_solve(10, 5)     -> 5 
tile_solve(6, 4)      -> 2 
tile_solve(1071, 462) -> 21 
```
## ADDITIONAL CONSTRAINT
A third argument, when provided, specifies the minimum dimension below which the manufacturer cannot produce tiles. If and when that constraint is specified, the solution must return the next best optimum size of the tile accordingly. 
```
Example
tile_solve(1071, 462, 25)  -> 147 
tile_solve(90000, 190)     -> 10
tile_solve(90000, 190, 20) -> 60
```
Of course, when settling for the next best optimum size, you will have to resort to breaking the tiles to ensure that the floor is covered without gaps.


```
def tile_solve(length, breadth, min_dim=0):
  # your code goes below 
  if (breadth == 0):
    return (length)
  elif (length%breadth) < min_dim:
    return (breadth)
  else:
    return tile_solve(breadth,length%breadth,min_dim)
```
