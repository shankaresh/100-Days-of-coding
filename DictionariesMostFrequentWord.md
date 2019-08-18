## Given the text: the first line contains the number of lines, then given the lines of words. Print the word in the text that occurs most often. If there are many such words, print the one that is less in the alphabetical order.
```
Example input
2
apple orange banana
banana orange

Example output
banana
```
```
# Read a string:
n = int(input())
words ={}
myList = []
# Print a value:
for i in range(n):
    a = list(input().split())
    for t in range(len(a)):  
        if a[t] not in words:
            words[a[t]] = 0
        words[a[t]] += 1
for k,v in words.items():
    if v >= max(words.values()):
        myList.append(k)
print(sorted(myList)[0])
```
