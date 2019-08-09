## Write a program that receives a number on the input. If the number is a multiple of 3, it prints "Jugs". If the number is a multiple of 5, it prints "Mugs". If the number is a multiple of both 3 and 5, it prints "JugsMugs".Otherwise, it prints the number.
```
INPUT 
3 
OUTPUT
Jugs

INPUT 
15
OUTPUT
Mugs


INPUT 
112
OUTPUT 112
```
```
number=int(input())
if number%3 == 0 and number%5 == 0:
	print("JugsMugs")
elif number%5 == 0:
  print("Mugs")
elif number%3 == 0:
	print("Jugs")
else:
  print(number)
```
