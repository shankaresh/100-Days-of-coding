## Print score-based Mark List 
When announcing the scores for an internal test,  it is normal to print something like the following (in alphabetical order)
```
Adam 90
Bosch 72
Candy 44
Damon 44
Ebony 88
Frederick 100
George 99
Harry 99
Insha 80
John 22
King 44
```
However, given such list, write a program that prints the score details that is sorted based on the actual score, as given in the format below: 
```
[(100, 'Frederick'),
(99, ['George', 'Harry']),
(90, 'Adam'),
(88, 'Ebony'),
(80, 'Insha'),
(72, 'Bosch'),
(44, ['Candy', 'Damon', 'King']),
(22, 'John')]
```
If a particular score has been scored by more than one student, then the list containing multiple student names must be sorted in ascending order. 
## Form a scoreDictionary:

Step 1. The code for importing the test data into a dictionary is already provided (do not modify this).  

Step 2. You must process the inputDict and generate another dictionary to store details of the input scores appropriately. 

Step 3. Subsequently, print the contents of the scoreDict dictionary. The scaffolding code  has  already been provided and this must not be modified.
```
########################
# Step 1 
# Build the input data dictionary 
# -- DO NOT EDIT--- 
########################
#
# Read the input 
n = int(input()) 
inputDict = {}
for _ in range(n): 
  tr = tuple(input().split()) 
  inputDict[tr[0]] = int(tr[1])

########################
# Step 2
# Build the scoreDict object
########################
# Generate the scoreDict dictionary 
# as you deem fit
scoreDict = {}

for key,value in sorted(inputDict.items()):
  if value not in scoreDict.keys():
    scoreDict[value] = key
  else:
    try:
      scoreDict[marks].append(names)
    except:
      scoreDict[marks] = [scoreDict[marks]]
      scoreDict[marks].append(names)



##############################################
# Step 3 
# Printing the contents of scoreDict 
# -- DO NOT EDIT--- 
##############################################
from pprint import pprint 
pprint(sorted(scoreDict.items(), reverse=True))
########### DO NOT ADD ANYTHING BELOW #######
#############################################

```
