## INTERVIEW GRADE
This is a frequently asked problem in technical interviews. It is also asked of 
senior software developers to gauge their ability to think and write clean code. 

## JugsMugsPugsPlusReverse Range
- Write a program that receives a number on the input and prints values from 1 to   
that number subjected to the conditions below. 
- It also should receive another boolean value 'rev' on the input. 

For every number in the given range, 
  - If the number is a multiple of 3, or it contains digit 3, it prints "Jugs". 
  - If the number is a multiple of 5, or it contains digit 5, it prints "Mugs".
  - If the number is a multiple of 7, or it contains digit 7, it prints "Pugs".

  - If the number is a multiple of both 3 and 5, it prints "JugsMugs".
        - also if number contains 3 and 5, it prints "JugsMugs"
  - If the number is a multiple of both 3 and 7, it prints "JugsPugs".
        - also if number contains 3 and 7, it prints "JugsPugs"
  - If the number is a multiple of 3, 5 and 7, it prints "JugsMugsPugs".
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
5
0
OUTPUT
1
2
Jugs
4
Mugs


INPUT 
15
1
OUTPUT
1
2
Jugs
4
Mugs
Jugs
Pugs
8
Jugs
Mugs
11
Jugs
Jugs
Pugs
MugsJugs
```
```
num = int(input())
rev = int(input())

for i in range(1,num+1):
  ans = ""
  lis = ["","",""]
  if '3' in str(i) or i%3 == 0:
    lis[0] = "Jugs" 
  if '5' in str(i) or i%5 == 0:
    lis[1] = "Mugs"
  if '7' in str(i) or i%7 == 0:
    lis[2] = "Pugs"
  if(rev==1):
    lis.reverse()
  for j in lis:
    ans = ans+j
  print( ans or i)
  ```
