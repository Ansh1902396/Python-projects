# Python-projects
import random
print("comp turn: snake(s),water(w),gun(g)")
def gameWin(comp,you):
    if comp==you:
        return None
    elif comp == 's':
        if you =='w':
            return False
        elif you=='g':
            return True
    elif comp == 'w':
        if you =='g':
            return False
        elif you=='s':
            return True
    elif comp == 'g':
        if you =='s':
            return False
        elif you=='w':
            return True


randNo =random.randint(1,3)
if randNo == 1:
    comp = 's'
elif randNo== 2:
    comp ='w'
elif randNo== 3:
    comp = 'g'

b= input("player_2:turn Snake(s) water(w) or gun(g)")

a = gameWin(comp, b)
print(f"computer chose \n {comp}")
print(f"you chose \n {b}")
if a == None:
    print("Its a tie")
elif a:
    print("you won!")
else:
    print("you lose!")
