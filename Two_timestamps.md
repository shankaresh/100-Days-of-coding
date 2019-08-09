## Given two timestamps of the same day: a number of hours, minutes and seconds for both of the timestamps. The moment of the first timestamp happened before the moment of the second one. Calculate how many seconds passed between them.
```
Example input #1
1
1
1
2
2
2

Example output #1
3661

Example input #2
1
2
30
1
3
20

Example output #2
50
```
```
hours1 = int(input())
min1 = int(input())
sec1 = int(input())
hours2 = int(input())
min2 = int(input())
sec2 = int(input())
print(((hours2-hours1)*60*60)+((min2-min1)*60)+(sec2-sec1))
```
