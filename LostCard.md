## There was a set of cards with numbers from 1 to N. One of the card is now lost. Determine the number on that lost card given the numbers for the remaining cards.

Given a number N, followed by N − 1 integers representing the numbers on the remaining cards (distinct integers in the range from 1 to N). Find and print the number on the lost card.
```
Example input
5
3
5
2
1

Example output
4
```
```
# Read an integer:
number = int(input())
li=[]
for i in range(1,number):
  li.append(int(input()))
for j in range(1,number+1):
  if (j not in li):
    print(j)
```
