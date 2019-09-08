# Rock_Paper_Scissor
## Description
Python can do literally anything with it. Python can also be used for game development. Here i create a simple command line Rock-Paper-Scissor game without using any external game libraries like PyGame.

In this game, gamer gets the first chance to pick the option among Rock, Paper and Scissor. After that computer selects from remaining two choices(randomly), then winner is decided as per the rules.randint() inbuilt function is used for generating random integer value within the given range.And the values of the choice are initialized using the dictionary used in function.

Rules :
Rock vs Paper-> Paper wins
Rock vs Scissor-> Rock wins
Paper vs Scissor-> Scissor wins
There is no same choice possibilities 

## Program
```
# import random module 
import random 
# def a function contains value for the choice 
def value_of_num(arg):
    switcher={1:"Rock",2:"Paper",3:"Scissor"}# dictionary is used
    return switcher.get(arg)
print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
print("Hello gamer , Welcome to Rock-Paper-Scissor game\n")
print("Rules : \n Rock vs Paper -> Paper wins \n Rock vs Scissor -> Rock wins \n Paper vs Scissor -> Scissor wins \n There is no same choice possibilities \n") 
print("GAME MOOD : Gamer vs Computer")
print("\ngame starts...")
g_count=c_count=0
while True:
    print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
    print("Vaild Choice :\n 1 - for ROCK\n 2 - for PAPER\n 3 - for SCISSOR")
    # take the input from user 
    choice=int(input("Gamer turn: "))
    # looping until gamer enter invalid input 
    while ((choice > 3)or(choice < 1)): 
        choice = int(input("Enter valid input (1,2,3 only available) : ")) 
    # initialize value of variable corresponding to the choice input 
    gamer_value = value_of_num(choice)
    # print gamer choice  
    print("\tGamer choice is : ",gamer_value) 
    print("\nNow its computer turn....\n") 
    # Computer chooses randomly any number among 1 , 2 and 3 Using randint method of random module 
    comp_choice = random.randint(1, 3)   
    # looping until comp_choice value is not equal to the choice value 
    while (comp_choice == choice): 
        comp_choice = random.randint(1, 3) 
    # initialize value of variable corresponding to the random input 
    comp_value = value_of_num(comp_choice)
    print("\tComputer choice is : ",comp_value)
    print("\n``````````````````````````````````````````````````")
    print("`\t<<<",gamer_value," vs ",comp_value,">>>  \t \t `") 
    # condition for result
    if ((choice == 1 and comp_choice == 2)or(choice == 2 and comp_choice ==1 )): 
        print("`    Paper wins => ", end = "") 
        result = "Paper"
    elif ((choice == 1 and comp_choice == 3)or(choice == 3 and comp_choice == 1)): 
        print("`    Rock wins => ", end = "") 
        result = "Rock"
    elif ((choice == 2 and comp_choice == 3)or(choice == 3 and comp_choice == 2)):
        print("`    Scissor wins => ", end = "") 
        result = "Scissor"
    # Printing either gamer or computer wins 
    if (result == gamer_value):
        print(" *** Gamer  wins *** \t \t `") 
        g_count+=1
    else: 
        print(" ***Computer wins*** \t \t `")
        c_count+=1
    print("``````````````````````````````````````````````````")      
    print("` Gamer Points: ",g_count,"\tComputer Points: ",c_count,"     `")
    print("``````````````````````````````````````````````````")
    print("\nDo you want to end the game? (press x or X)\n\t OR \nTo continue press any.... ") 
    ans = input()
    # if gamer input(s) n or N then condition is True and ends the game 
    if ((ans == 'x')or(ans == 'X')): 
        break
      
# after coming out of the game thanking them for playing
print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
print("\t       Thanks for playing                 ")
print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
```

## Output
```
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Hello gamer , Welcome to Rock-Paper-Scissor game

Rules : 
 Rock vs Paper -> Paper wins 
 Rock vs Scissor -> Rock wins 
 Paper vs Scissor -> Scissor wins 
 There is no same choice possibilities 

GAME MOOD : Gamer vs Computer

game starts...
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Vaild Choice :
 1 - for ROCK
 2 - for PAPER
 3 - for SCISSOR

Gamer turn: 1
        Gamer choice is :  Rock

Now its computer turn....

        Computer choice is :  Scissor

``````````````````````````````````````````````````
`       <<< Rock  vs  Scissor >>>                `
`    Rock wins =>  *** Gamer  wins ***           `
``````````````````````````````````````````````````
` Gamer Points:  1      Computer Points:  0      `
``````````````````````````````````````````````````

Do you want to end the game? (press x or X)
         OR 
To continue press any.... 

1
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Vaild Choice :
 1 - for ROCK
 2 - for PAPER
 3 - for SCISSOR

Gamer turn: 2
        Gamer choice is :  Paper

Now its computer turn....

        Computer choice is :  Rock

``````````````````````````````````````````````````
`       <<< Paper  vs  Rock >>>                  `
`    Paper wins =>  *** Gamer  wins ***                  `
``````````````````````````````````````````````````
` Gamer Points:  2      Computer Points:  0      `
``````````````````````````````````````````````````

Do you want to end the game? (press x or X)
         OR 
To continue press any.... 

2
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Vaild Choice :
 1 - for ROCK
 2 - for PAPER
 3 - for SCISSOR

Gamer turn: 3
        Gamer choice is :  Scissor

Now its computer turn....

        Computer choice is :  Rock

``````````````````````````````````````````````````
`       <<< Scissor  vs  Rock >>>                `
`    Rock wins =>  ***Computer wins***           `
``````````````````````````````````````````````````
` Gamer Points:  2      Computer Points:  1      `
``````````````````````````````````````````````````

Do you want to end the game? (press x or X)
         OR 
To continue press any.... 

x
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
               Thanks for playing                 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
```
