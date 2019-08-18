## It is possible to place 8 queens on an 8×8 chessboard so that no two queens threaten each other. Thus, it requires that no two queens share the same row, column, or diagonal.  

Given a placement of 8 queens on the chessboard. If there is a pair of queens that violates this rule, print YES, otherwise print NO. The input consists of eight coordinate pairs, one pair per line, with each pair giving the position of a queen on a standard chessboard with rows and columns numbered from 1 to 8.

```
Example input
1 5
2 3
3 1
4 7
5 2
6 8
7 6
8 4
(shown on the picture)

Example output
NO
```
```
n = 0
coord = {}
myList = []
x_co = []
y_co = []
Rule_vi = None
while n < 16:
    a = input()
    inList = list(map(int, a.split()))
    myList.append(inList[0])
    myList.append(inList[1])
    x_co.append(myList[n]) 
    y_co.append(myList[n+1]) 
    n = n+2
i = 0
for x in x_co:
    for i in range(0,8):
        if x == x_co[i] and x_co.index(x) != i:
            Rule_vi = True 
i = 0
for y in y_co:
    if Rule_vi == True:
      break
    for i in range(0,8):
        if y == y_co[i] and y_co.index(y) != i:
            Rule_vi = True 
            break
n = 0
i = 0
for n in range(0,8):
    if Rule_vi == True:
        break
    for i in range(0,8):
        if  abs(x_co[n] - x_co[i]) == abs(y_co[n] - y_co[i]) and i != n:
            Rule_vi = True
            break
if Rule_vi == True:
  print('YES')
else:
  print('NO')
```
