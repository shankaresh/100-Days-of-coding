## For the given integer N calculate the following sum:
1³ + 2³ + ... + N³
```
Example input
3

Example output
36
```
```
# Read an integer:
cube_sum =0
# Print a value:
for i in range (1,int(input())+1):
  cube_sum += i*i*i 
print(cube_sum)
```
