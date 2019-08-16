## Given a string in which the letter h occurs at least twice, reverse the sequence of characters enclosed between the first and last occurrences of it.
```
Example input
In the hole in the ground there lived a hobbit

Example output
In th a devil ereht dnuorg eht ni eloh ehobbit
```
```
# Read a string:
s = input()
# Print a string:
index1 = s.find('h')
index2 = s.rfind('h')
print(s[:index1] + s[index2:index1:-1] + s[index2:])
```
