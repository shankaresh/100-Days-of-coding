## Given a string in which the letter h occurs at least twice, replace every occurrence of the letter h by the letter H, except for the first and the last ones.
```
Example input
In the hole in the ground there lived a hobbit

Example output
In the Hole in tHe ground tHere lived a hobbit
```
```
# Read a string:
s = input()
# Print a string:
# print(s)
in1 = s.find('h')
in2 = s.rfind('h')

first = s[:in1+1]
middle = s[in1+1: in2].replace("h", "H")
last = s[in2:]

print(first + middle + last)
```
