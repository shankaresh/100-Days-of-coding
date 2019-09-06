## Cycling Among Values
Suppose a variable x can have only three possible different values a, b and c, and you wish to assign to x the value other than its current one, and you wish your code to be independent of the values of a, b and c.What is the most efficient way to cycle among three values? Write a function cycle_values so that it satisfies
```
 cycle_values(a) = b
 cycle_values(b) = c
 cycle_values(c) = a
```
## EXAMPLE
```
 cycle_values(10, a=10, b=20, c=100) -> 20
 cycle_values(20, a=10, b=20, c=100) -> 100
 cycle_values(100, a=10, b=20, c=100) -> 10

 cycle_values(3, { a:3, b:4, c:5 } ) => 4
```
## Other extensions
To pass all test cases, you will have to change the signature of the function and  
and that is encouraged for this particular exercise. 

If the key literals are not in sequence, then you must flag an error. For example, a, b, d is not a valid set of keyword arguments.
What if there are more than 3 alternating values? How will your code change? Imagine you were to support up to a maximum of 26 alternating values.
The literal sequence could also start from any letter, and may even wrap around. For example,
```
cycle_values(100, {'y':56, 'z':100, 'a':2, 'b':3}) -> 2 
```

```
def cycle_values(search, **data ):
  if search not in data.values():
    return None
  for key in data.keys():
    if (data[key]==search):
      if (key== max(data.keys())):
        result=data[min(data.keys())]
        return result
      result=data[chr(ord(key)+1)] #order is change to arg by chr 
      return result
```
