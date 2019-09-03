## Second Largest
Write a function second_is_second_largest that will return True if the 2nd largest value is in the 2nd position. Otherwise, return False.

The function should accept three arguments. 

## Example 
```
second_is_second_largest(1, 2, 3) -> True 
second_is_second_largest(11, 10, 9) -> True
second_is_second_largest(3, 3, 0) -> False 
second_is_second_largest(3, 2, 2) -> False 
```
```
def second_is_second_largest(F_arg,S_arg,T_arg):
  if ((S_arg>F_arg and S_arg<T_arg) or (S_arg<F_arg and S_arg>T_arg)):
    return True
  else:
    return False
    
    
"""
def second_is_second_largest(args):
  listnew=args.copy()
  listnew.sort(reverse=True)
  if (listnew[1]==args[1]):
    return True
  else:
    return False
#args=list(map(int,input().split()))
"""
#F_arg=int(input())
#S_arg=int(input())
#T_arg=int(input())
#print(second_is_second_largest(F_arg,S_arg,T_arg))
```
