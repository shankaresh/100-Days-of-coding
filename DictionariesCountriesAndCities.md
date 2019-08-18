## Given a list of countries and cities of each country, then given the names of the cities. For each city print the country in which it is located.
```
Example input
2
USA Boston Pittsburgh Washington Seattle
UK London Edinburgh Cardiff Belfast
3
Cardiff
Seattle
London

Example output
UK
USA
UK
```
```
# Read a string:
n = int(input())
Location ={}
# Print a value:
for i in range (n):
    a = list(input().split())
    Location[a[0]] = a[1:]
m = int(input())
for t in range (m):
    b = input()
    for country, city in Location.items():
        if b in city:
            print(country)
```
