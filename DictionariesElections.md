## The first line contains the number of records. After that, each entry contains the name of the candidate and the number of votes they got in some state. Count the results of the elections: sum the number of votes for each candidate. Print candidates in the alphabetical order.
```
Example input
5
McCain 10
McCain 5
Obama 9
Obama 8
McCain 1

Example output
McCain 16
Obama 17
```
```
num_of_votes = {}
for _ in range(int(input())):
    candidate, votes = input().split()
    num_of_votes[candidate] = num_of_votes.get(candidate, 0) + int(votes)
for candidate, votes in sorted(num_of_votes.items()):
    print(candidate, votes)
```
