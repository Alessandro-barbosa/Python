import random
from time import sleep


def readInt(msg):
    ok = False
    valor = 0
    while True:
        n = str(input(msg))
        if n.isnumeric():
            valor = int(n)
            ok = True
        else:
            print("\033[0;31mERROR! Enter a valid number!\033[m")
        if ok:
            break
    return valor


print("Guess the number i'm thinking of!\n"
      "Tip: the number is between 1 and 100\n"
      "")
n = random.randint(1, 100)

print("You have 6 attempts to discover the number!\n")
number = 101
attempt = 1
range = 0
while number != n:
    print(f"\nAttempt {attempt}: ", end="")
    number = readInt("")
    range = number - n
    if attempt == 6:
        if number != n:
            sleep(0.5)
            print("\nYou lose!\n")
            sleep(0.5)
            print(f"The number is {n}   :|")
            sleep(0.5)
            break
    if number == n:
        sleep(0.5)
        print("You win!\n"
              "\nCongratulations!!! :)\n")
        number = n
        sleep(0.5)
        break
    if range < 0:
        range *= -1
    if 10 >= range >= 5:
        sleep(0.5)
        print("\nIt's close!")
    if range < 5:
        sleep(0.5)
        print("\nOMG VERY CLOSE!!")
    if number < n:
        sleep(0.5)
        print("\nIt needs to be higher")
    if number > n:
        sleep(0.5)
        print("\nIt needs to be lower")

    attempt += 1
