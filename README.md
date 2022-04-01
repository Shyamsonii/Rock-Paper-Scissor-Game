# Rock-Paper-Scissor-Game
<!-- This is a game. -->


import random

l = ["rock", "scissor", "paper"]
'''
rock vs paper-> paper wins
rock vs scissor-> rock wins
paper vs scissor-> scissor wins.

'''
while True:
    ccount = 0
    ucount = 0
    uc = int(input('''
Game Start....
1 Yes
2 No   
    '''))
    if uc == 1:
        for a in range(1, 6):
            ui = int(input('''
1 Rock
2 Scissor
3 Paper
            
            '''))
            if ui == 1:
                uchoice = "rock"
            elif ui == 2:
                uchoice = "scissor"
            elif ui == 3:
                uchoice = "paper"
            cchoice = random.choice(l)
            if cchoice == uchoice:
                print("computer value", cchoice)
                print("user vlaue", uchoice)
                print("Game draw")
                ucount = ucount + 1
                ccount = ccount + 1
            elif (uchoice == "rock" and cchoice == "scissor") or (uchoice == "paper" and cchoice == "rock") or (
                    uchoice == "scissor" and cchoice == "paper"):
                print("Computer value", cchoice)
                print("user value", uchoice)
                print("you win")
                ucount = ucount + 1
            else:
                print("Computer value", cchoice)
                print("user value", uchoice)
                print("Computer win")
                ccount = ccount + 1
        if ucount == ccount:
            print("Final game draw...")
            print("user score", ucount)
            print("computer score", ccount)
        elif ucount > ccount:
            print("Final you win the game...")
            print("user score", ucount)
            print("computer score", ccount)
        else:
            print("Final computer win the game...")
            print("user score", ucount)
            print("computer score", ccount)

    else:
        break
