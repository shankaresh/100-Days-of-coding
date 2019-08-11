## Write a program that receives a number on the input. It also should receive another boolean value 'rev' on the input. 
  - If the number is a multiple of 3, or it contains digit 3, it prints "Jugs". 
  - If the number is a multiple of 5, or it contains digit 5, it prints "Mugs".
  - If the number is a multiple of 7, or it contains digit 7, it prints "Pugs".

  - If the number is a multiple of both 3 and 5, it prints "JugsMugs".
        - also if number contains 3 and 5, it prints "JugsMugs"
  - If the number is a multiple of both 3 and 7, it prints "JugsPugs".
        - also if number contains 3 and 7, it prints "JugsPugs"
  - If the number is a multiple of 3, 5 and 7, it prints "JugsMugPugs".
        - also if number contains 3, 5 and 7, it prints "JugsMugsPugs"
Otherwise, it prints the number.

## REVERSE REQUIREMENT:
If the boolean 'rev' is True, then reverse the order of printing. 
  - "PugsJugsMugs" for multiples of 3, 5 and 7
  - "PugsMugs" for multiple of 5 and 7
  - "MugsJugs" for multiple of 3 and 5 
  - "PugsJugs" for multiple of 3 and 7
```
INPUT 
73 
False  # contains 3 and 7

OUTPUT
JugsPugs

INPUT 
73 
True  # contains 7 and 3, print reverse order

OUTPUT
PugsJugs

INPUT 
51  # multiple of 3 and contains 5

OUTPUT
JugsMugs


INPUT 
105

OUTPUT 
JugsMugsPugs
```
~~~
num = int(input())
rev = int(input())
ans = ""
lis = ["","",""]
if '3' in str(num) or num%3 == 0:
  lis[0] = "Jugs" 
if '5' in str(num) or num%5 == 0:
  lis[1] = "Mugs"
if '7' in str(num) or num%7 == 0:
  lis[2] = "Pugs"
if rev:
  lis.reverse()
for j in lis:
  ans = ans+j
print( ans or num)
~~~
