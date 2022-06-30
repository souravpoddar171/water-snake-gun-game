# water-snake-gun-game
def gamewin(computer,you):
    if(computer==you):
        return
    elif(computer=='snake'):
        if(you=='water'):
            return False
    elif(you=='gun'):
        return True

    elif(computer=='water'):
        if(you=='gun'):
            return False
    elif(you=='snake'):
        return True
    elif(computer=='gun'):
        if(you=='snake'):
            return False
    elif(you=='water'):
        return True




#water snake gun game 
import random 
role_option = ["water",'snake',"gun"]
user_choice = input(" user_choice:(s),(w),(gun):")
if(user_choice == 'water'):
    you = 'water'
elif(user_choice == 'snake'):
    you = 'snake'

elif(user_choice == 'gun'):
    you = 'gun'
else:
        print('role is not availble')

print("user_choice:",you)

computer = ["water","snake","gun"]
computer_choice = random.choice(computer)

print(computer_choice)


if(computer_choice=='water'):
    computer = 'water'
elif(computer_choice=='gun'):
    computer = 'gun'
elif(computer_choice=='snake'):
    computer = 'snake'
else:
    print("not available")

print("computer_choice:",computer)

a = gamewin(computer,you)

if ( a==None):
    print("game tie")

elif a:
    print("you  win!")
else:
    print(" you  lose!!")
