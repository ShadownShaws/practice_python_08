# practice_python_08

def is_it_123(num):

    if num == "1" or num == "2" or num == "3":

        return True

    return False


player1 = str

player2 = str

player1_good_input = False

print("\nROCK PAPER SCISSORS ULTIMATE SIMULATOR !\n")

rule = "Choose 1 for Rock, 2 for Paper and 3 for Scissors !\n" \
       "Hide the keypad and press enter the moment you click on the number !"

rematch = True

while rematch:

    print("\n\n\n\n\n\n\n" + rule)

    if not player1_good_input:

        player1 = input("Player 1, select your WEAPON !\n-> ")

    if is_it_123(player1):

        print("\n\n\n\n\n\n\n" + rule)

        player2 = input("Player 2, select your WEAPON !\n-> ")

        if is_it_123(player2):

            if player1 == "1" and player2 == "2":

                print("Player 2 WIN !")

            elif player1 == "2" and player2 == "3":

                print("player 2 WIN !")

            elif player1 == "3" and player2 == "1":

                print("Player 2 WIN !")

            elif player1 == player2:

                print("DRAW !")

            else:

                print("Player 1 WIN !")

            if input("Would you like to play again ?\n"
                     "Simply press Enter to restart or press any other key then Enter\n-> ") == "":

                print(rule)

            else:

                rematch = False

        else:

            print("Wrong input !")

    else:

        print("Wrong input !")

print("\n\n\nThank you for playing along this shitty game :D !")
