# pythonprogram
#It is a game . Game name is "SNAKE WATER AND GUN". 
print(''' welcome ! 

      "SNAKE WATER AND GUN "

about game :-
In this game you have 3 choices . You have to chose from snake 
water and gun .

rules :-

1) if your choice is sanke and computer choose water then you win or if computer choose 
   gun you lose.
2)if your choice is water and computer choose gun then you win or if computer choose 
   snake you lose.
3)if your choice is gun and computer choose snake then you win or if computer choose 
   water you lose.''')

print("**************START***************")


import random

randno = random.randint(1,3)

if randno==1:
    comp="s"
elif randno==2:
    comp="w"
elif randno==3:
    comp="g"

def game(comp,you):
    if comp==you:
        return None 
    elif comp=="s":
        if you=="w":
          return False 
        elif you=="g":
          return True
    elif  comp=="w":
        if you=="g":
          return False 
        elif you=="s":
          return True
    elif  comp=="g":
        if you=="s":
          return False 
        elif you=="w":
          return True    



you = input('''Your turn :
s for snake
w for water 
g for gun: 

enter : ''')

print("computer's turn ")
print(f"computer chose : {comp}")

a=game(comp,you)
if a==None:
   print("oops it is a tie! ")
elif a==True:
   print("congratulations ! you win ")
elif a==False :
   print("oops you lost , let's try again ")
print("thank you , hope you enjoyed this game ")   

