# INTERVIEW GRADE PROBLEM
## JugsMugsPugs Special
## SPECIAL REQUIREMENT: 
Try and limit the number of conditional statements to not more than two. 
This requires some advanced Python language knowledge. I don't expect everyone  
to be able to complete this.

Write a program that receives a number on the input and prints values from 1 to that number subjected to the conditions below. 
It also should receive another boolean value 'rev' on the input. 

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
False
OUTPUT
1
2
Jugs
4
Mugs


INPUT 
15
True
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
rev = bool(input())
for i in range(1,num+1):
  if rev: 
    string = 'Jugs' * bool(i%3==0 or '3' in str(i))
    string = 'Mugs' * bool(i%5==0 or '5' in str(i)) + string 
    string = 'Pugs' * bool(i%7==0 or '7' in str(i)) + string 
    print( string or i) 
  else: 
    print("Jugs" * (i%3==0 or '3' in str(i)) + "Mugs" * (i%5==0 or '5' in str(i)) + "Pugs" * (i%7==0 or '7' in str(i)))
```
