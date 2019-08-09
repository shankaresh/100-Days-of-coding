## Write a program to calculate the distance between two points:
To find the distance between two points (x1,y1) and (x2,y2), all that you need to do is use the coordinates of these ordered pairs and apply some common sense. Begin with the most simplest formula and then incrementally arrive at the correct formula as you solve the test cases.
```
Example 

INPUT 
4
0
0
0

OUTPUT
4

INPUT 
0
0
4
3

OUTPUT
5
```
```
import math;
# get the x coordinate of Point 1
x1 = int(input())  
# get the y coordinate of Point 2
y1 = int(input())  
# get the x coordinate of Point 2
x2 = int(input())
# get the y coordinate of Point 2
y2 = int(input())

# Write the code to calculate distance between 
# the two points 
print(math.sqrt(math.pow(x2 - x1, 2) + math.pow(y2 - y1, 2)))
```
