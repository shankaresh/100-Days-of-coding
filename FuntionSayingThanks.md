## Introducing Functions
One of the core principles of any programming language is, "Don't Repeat Yourself". If you have an action that should occur many times, you can define that action once and then call that code whenever you need to carry out that action.

We are already repeating ourselves in our code, so this is a good time to introduce simple functions. Functions mean less work for us as programmers, and effective use of functions results in code that is less error-prone.

## Define a thank_you function 
Define a function thank_you so that it prints the equivalent of two lines of compliments. 
The function must accept an argument name which can be used within the function. 

## Example
```
thank_you('Adriana') -> 
You are doing good work, Adriana!
Thank you very much for your efforts on this project.

thank_you('Billy') -> 
You are doing good work, Billy!
Thank you very much for your efforts on this project.
```
```
print("You are doing good work, Adriana!")
print("Thank you very much for your efforts on this project.")

print("\nYou are doing good work, Billy!")
print("Thank you very much for your efforts on this project.")

print("\nYou are doing good work, Caroline!")
print("Thank you very much for your efforts on this project.")


def thank_you(name):
  # write your code below 
  if name=="Adriana":
    pass
    print("You are doing good work, Adriana!")
    print("Thank you very much for your efforts on this project.")
  else:
    print("\nYou are doing good work,",name,"!")
    print("Thank you very much for your efforts on this project.")


###### DO NOT EDIT ##############
n = int(input())
for _ in range(n): 
  thank_you(input())
###### DO NOT EDIT ##############
```
