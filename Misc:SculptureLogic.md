## Sculpture Moves

In a particular museum, a section of the building containing N rooms has been allotted for placing all the important bronze sculptures. The movers who brought the sculptures randomly dropped them off into different rooms. 

The curator of the museum now wants each of the N rooms to have the same number of items. That way, crowd management of the visitors will be better. 

* Any one and only one of the rooms may have sculptures less or more than what is available in the other rooms.
* It can be assumed that the total number of sculptures is equal to or more than the total number of rooms. 
* Every room must have at least one sculpture.

Write a function that will accept one argument: 
  -a list containing the number of sculptures in each of the rooms
  
The output of the function must be the count of number of moves (or transfers) that are required to optimally distribute the sculptures in the rooms. 

That is, one sculpture transferred from one room to another counts as one move/transfer. 

### Sample Input / Output:
~~~
input     -> [3, 3, 2, 4]
output   -> 1

input    -> [6, 5, 4, 1, 2, 7, 5]
output  -> 5
~~~

## சிற்பம் தர்க்கம்
ஒரு குறிப்பிட்ட அருங்காட்சியகத்தில், அனைத்து முக்கியமான வெண்கல சிற்பங்களையும் வைக்க N அறைகள் கொண்ட கட்டிடத்தின் ஒரு பகுதி ஒதுக்கப்பட்டுள்ளது. சிற்பங்களை கொண்டு வந்த மூவர்ஸ் தோராயமாக அவற்றை வெவ்வேறு அறைகளில் இறக்கிவிட்டார்.

அருங்காட்சியகத்தின் கண்காணிப்பாளர் இப்போது ஒவ்வொரு N அறைகளிலும் ஒரே எண்ணிக்கையிலான பொருட்களைக் கொண்டிருக்க விரும்புகிறார். அந்த வகையில், பார்வையாளர்களின் கூட்ட மேலாண்மை சிறப்பாக இருக்கும்.

* Any one and only one of the rooms may have sculptures less or more than what is available in the other rooms.
* மொத்த சிற்பங்களின் எண்ணிக்கை மொத்த அறைகளின் எண்ணிக்கையை விட சமமாகவோ அல்லது அதிகமாகவோ இருக்கும் என்று கருதலாம்.
* ஒவ்வொரு அறையிலும் குறைந்தது ஒரு சிற்பம் இருக்க வேண்டும்

Write a function (செயல்பாட்டின்) that will accept one argument:   
   - a list containing the number of sculptures in each of the rooms 

செயல்பாட்டின்  வெளியீடு (function output) அறைகளில் உள்ள சிற்பங்களை சமப்படுத்த தேவையான நகர்வுகளின் எண்ணிக்கையை (அல்லது இடமாற்றங்களை) கொண்டிருக்க வேண்டும். 

அதாவது, ஒரு சிற்பம் ஒரு அறையிலிருந்து இன்னொரு அறைக்கு மாற்றப்படுவது ஒரு நகர்வு / பரிமாற்றமாகக் கருதப்படுகிறது.

### Sample Input / Output:
```
input     -> [3, 3, 2, 4] output   -> 1
input    -> [6, 5, 4, 1, 2, 7, 5] output  -> 5
````

### Program:
```python
def sculpture_moves(arr):
  avg = int(sum(arr)/len(arr))
  rem = int(sum(arr)%len(arr))
  moves = 0
  for i in arr:
    if i > avg:
      moves += i - avg
  if rem:
    moves -= rem
  return moves
```
