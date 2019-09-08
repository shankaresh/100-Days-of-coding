## fromlist
Write a python function fromlist that accepts a maximum of two lists - a list of keys and a list of values.
- if the list of values is not provided, use 0 as the value for all keys and return a dictionary object
- if both list of keys and list of values are provided, return a list containing tuples containing corresponding items from both lists. Use list comprehension to deliver the output.
```
Example
(['a', 'b'])         => dict( {'a':0}, {'b': 0})
(['a', 'b'], [1, 2]) => [('a',1), ('b', 2)]
```
## GUIDELINES FOR REFACTORING
0. Consider the use of default arguments
1. Consider the use of one of the methods of dict class for creation of dict object
2. Consider using zip to create a list of tuples 
```
def fromlist(key,value=0):
  if value==0:
    return dict.fromkeys(key,value)
  else:
    Zip = zip(key,value)
    return list(dict(Zip).items())
```
