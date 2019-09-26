# Friends of friends
We can create a dictionary mapping people to sets of their friends. For example, we might say:

```
d["fred"] =  set(["wilma", "betty", "barney", "bam-bam"])  
d["wilma"] = set(["fred", "betty", "dino"])
```

With this in mind, write a function friend_of_friends that takes such a dictionary mapping of people to sets of friends and returns a new dictionary mapping all the same people to sets of their friends of friends.

For example, since wilma is a friend of fred, and dino is a friend of wilma, 

> dino is a friend-of-friend of fred.

This set should exclude any direct friends, so even though betty is also a friend of wilma, betty does not count as a friend-of-friend of fred (since she is simply a friend of fred).

Thus, in this example, fred’s ‘friends-of-friends’ is a set containing just dino and 
wilma’s ‘friends-of-friends’ is a set containing both barney and bam-bam.

Also, do not include anyone either in their own set of friends or their own 
set of friends-of-friends. 

You may assume that everyone listed in any of the friend sets also is included 
as a key in the dictionary.


# TAMIL DESCRIPTION
friends-of-friends function-ற்க்கு இரண்டு நபர்களின் friends பட்டியலை (as set ) input ஆக கொடுக்கும் போது, அது மறைமுக நண்பர்களை (friends-of-friends) output ஆக கொடுக்க வேண்டும்.

Example :  fred and wilma -வின் friends list -ஐ எடுத்து கொள்வோம் 
```                   
d ["fred "] = set (["wilma", "betty", "barney", "bam-bam"])
d ["wilma"] = set (["fred", "betty", "dino"])
```   
* fred -ன் friend wilma 
* wilma -க்கு மட்டும் friend "dino" 
* therefore friends-of-friends["fred"] = set (["dino"])

Similarly 
* wilma -ன் friend fred 
* fred -க்கு மட்டும் friends "barney" and "betty"
* therefore friends-of-friends["wilma"] = set(["barney", "bam-bam"])

**Hint:**
* Exclude direct friends *[ex :"betty" is friend of both fred and wilma]*
* Exclude the persons themselves *[i.e. exclude fred and wilma]*

## Program :
```python
def friend_of_friends(dic):
  frdlist={}
  for name in dic:
    frdoffrds = dic[name]
    frdlist[name]={f for frd in frdoffrds for f in dic[frd].difference(frdoffrds) if f is not name}
  return frdlist
```
