## The text is given in a single line. For each word of the text count the number of its occurrences before it.
```
Example input
one two one two three two four three

Example output
0 0 1 1 0 2 0 1
```
```
a=input()
def occurrence(a):
    counter = {}
    string = ''
    for word in a.split():
        counter[word] = counter.get(word, 0) + 1
        string += str(counter[word] - 1) +' '
    return string
print(occurrence(a))
```
