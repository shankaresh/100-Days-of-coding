## Make Ladoos
For this year Diwali, we need to assemble a parcel of goal kilos of ladoos. There are small ladoos (2 kilos each) and big ladoos (5 kilos each). 

Write a function that returns the number of small ladoos to use, assuming we always use big ladoos before small ladoos. Return -1 if it can't be done.

> {make_ladoos(small, big, goal) 
small -> number of small ladoos available
big -> number of big ladoos available
goal -> the desired weight of the final package}

***Bonus points for coming with a solution that has no for-loops or while-loops.***

### Example:
```
make_ladoos (4, 1, 13)    ->  4
make_ladoos (4, 1, 14)    -> -1
make_ladoos (2, 1, 7)     ->  1
```

### program:
```
import sys
sys.setrecursionlimit(1010)
def make_ladoos(small, big, goal):
  s_l=small*2
  b_l=big*5
  total=b_l+s_l
  if(goal>total):
    return -1
  
  if(b_l==goal):
    return 0
  elif(b_l>goal):
    return make_ladoos(small,big-1,goal)
  elif(total==goal):
    return small
      
  return make_ladoos(small-1,big,goal)
```
