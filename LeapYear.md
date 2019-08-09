## Given the year number. You need to check if this year is a leap year. If it is, print LEAP, otherwise print COMMON.

The rules in Gregorian calendar are as follows:
* a year is a leap year if its number is exactly divisible by 4 and is not exactly divisible by 100
* a year is always a leap year if its number is exactly divisible by 400
```
Example input
2012

Example output
LEAP
```
```
# Read an integer:
year = int(input())

#checking the leap year
#Print a value:
if year%4 == 0 and year%100 != 0 or year%400 == 0:
  print ("LEAP")
else:
  print("COMMON")
```
