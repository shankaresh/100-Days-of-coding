## Given the integer N - the number of seconds that is passed since midnight - how many full hours and full minutes are passed since midnight?The program should print two numbers: the number of hours (between 0 and 23) and the number of minutes (between 0 and 1339).
```
Example input
3900

Example output
1 65
```
```
# Read an integer:
a = int(input())
# Print a value:
print((a//60)//60,a//60)
```
