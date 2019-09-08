This is a favourite interview question for the Skava Company, Coimbatore. Variants of the same coding challenge occurs frequently in other technical coding evalutions.

## Quick Compress
Write a Python function quick_compress for a crude compression where in a given input token string the function removes the consecutively repeating characters and replaces the count of the repeated characters in the string.

Return the compressed text from the function as a string.
```
Example
input: abbbcddef
output: ab3cd2ef

input: abbbcddef ghhhikkg
output: ab3cd2ef gh3ik2g
```
```
def quick_compress(characters):
  res = ""
  temp = ""
  Tcount = 0
  count = 1
  for character in characters:
    if (temp == character):
      count+=1
    elif (count >1):
      res += str(count)+character
      count =1
    else:
      res = res+character
      count =1
    temp = character
    if (Tcount==len(characters)-1 and count>1):
      res = res+str(count)
    else:
      Tcount+=1
  return res
  ```
