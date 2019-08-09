## Write a program that receives a number on the input.

  - If the number is a multiple of 3, or it contains digit 3, it prints "Jugs". 
  - If the number is a multiple of 5, or it contains digit 5, it prints "Mugs".
  - If the number is a multiple of 7, or it contains digit 7, it prints "Pugs".
Otherwise, it prints the number.

## SPECIAL REQUIREMENT: 
Try and limit the number of conditional statements to not more than 4. 
And use only one print statement.

```
INPUT 
73 
OUTPUT
JugsPugs

INPUT 
51  

OUTPUT
JugsMugs


INPUT 
105

OUTPUT 
JugsMugsPugs
```
```
number =  input()
digit = int(number)
if (digit%3==0)or(digit%5==0)or(digit%7==0)or('3' in number)or('5' in number)or('7' in number):
  a =""
  if (digit%3==0) or ('3' in number):
    a ="Jugs"
  if (digit%5==0) or ('5' in number):
    a = a+"Mugs"
  if (digit%7==0) or ('7' in number) :
    a =a+"Pugs" 
print(a)
```
