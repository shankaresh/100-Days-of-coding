## 'abc' in the Centre?
Given a sequence of characters, does "abc" appear in the CENTRE of the string? 

To define CENTRE, we'll say that the number of characters to the left and right 
of the "abc" must differ by at most one. 

If it is in the CENTRE, return True. Otherwise, return False.

This problem looks simple, but it might not be easy. 

### EXAMPLE:
```
abc_centre("AAabcBB")  → True
abc_centre("AabcBB")   → True
abc_centre("AabcBBB")  → False
```

### Program:
```
def abc_centre(string):
  abc = "abc"
  tot=round(len(string)/2)
  st=tot-3
  ed=tot+3
  if abc not in string:
    return False
  elif abc in string:
    str1=len(string[:string.find("abc",st,ed)])
    str2=len(string[string.find("abc",st,ed)+3:])
    if ((str1==str2)or(str1+1==str2)or(str1==str2+1)):
      return True
    else:
      return False
```
