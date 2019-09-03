## String Rotator
Write a Python function string_rotate to generate the desired pattern. The function should accept an integer as its single argument. 

Input and Output Format:
Input consists of a single integer that corresponds to n.
Assume that 0 < n <= 26. 
Refer sample output for output formatting specifications.
```
Sample Input1 : 5
Sample Output1:
ABCDE
BCDEA
CDEAB
DEABC
EABCD

Sample Input2 : 6
Sample Output2:
ABCDEF
BCDEFA
CDEFAB
DEFABC
EFABCD
FABCDE
```
```
def string_rotate(limi): 
  alp=("ABCDEFGHIJKLMNOPQRSTUVWXYZ")
  alpp=alp[0:limi]
  lines=''
  lines+=alpp+' '
  for lim in range(1,len(alpp)):
      Lfirst=alpp[0 : lim]
      Lsecond=alpp[lim :]
      lines+=(Lsecond + Lfirst)+' '
  return lines.strip()
```
