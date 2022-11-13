# Rock-Paper-Scissors-Script

## Getting Started

1. Clone the repository
2. Join to the correct path of the clone
3. Use `python rockpaperscissors.py` to execute script

## Description

I made a web page that allows you to play the memory game. You have to find the even cards, to know which ones are even you have to search among the different foods, if you find two apples you add points and you add a pair. Once you finish playing and you have found all your pairs it will calculate the time it took you to finish.

## Technologies used

1. Python

## Libraries used

1. random

## Galery

![rock,paper,scissors](https://raw.githubusercontent.com/DiegoLibonati/DiegoLibonatiWeb/main/data/projects/Python/Imagenes/rcspython-0.jpg)

![rock,paper,scissors](https://raw.githubusercontent.com/DiegoLibonati/DiegoLibonatiWeb/main/data/projects/Python/Imagenes/rcspython-1.jpg)

![rock,paper,scissors](https://raw.githubusercontent.com/DiegoLibonati/DiegoLibonatiWeb/main/data/projects/Python/Imagenes/rcspython-2.jpg)

## Portfolio Link

`https://diegolibonati.github.io/DiegoLibonatiWeb/#/projects?q=Rock,%20Paper%20Or%20Scissors%20Script`

## Video

https://user-images.githubusercontent.com/99032604/199367605-83e5b8da-6470-4919-ad66-37cc6b6ba554.mp4

## Documentation

In `ia_choose` we will have an array with the possibilities that the ia will have to choose from such as `rock, paper and scissors`, then the round the game is going in `round`, `user_score` will tell us how many rounds the user won and finally `ia_score` will tell us how many rounds the computer won:

```
ia_choose = ["rock", "paper", "scissors"]
round = 1
user_score = 0
ia_score = 0
```

This `generate_random_number()` function will generate a random number:

```
def generate_random_number():
    return randint(0, len(ia_choose)-1)
```

This function `check_result_of_round()` is in charge of giving the final result of the current round, whether the user or the AI won:

```
def check_result_of_round(ia, user):

    global user_score
    global ia_score

    if ia == "rock" and user == 0 or ia == "paper" and user == 1 or ia =="scissors" and user == 2:
        return print(f"Tied round: IA: {ia} | User: {ia_choose[user]}")
    elif ia == "rock" and user == 1 or ia =="paper" and user == 2 or ia == "scissors" and user == 0:
        user_score += 1
        return print(f"User won the round: IA: {ia} | User: {ia_choose[user]}")
    elif ia =="rock" and user == 2 or ia == "paper" and user == 0 or ia == "scissors" and user == 1:
        ia_score += 1
        return print(f"IA won the round: IA: {ia} | User: {ia_choose[user]}")
```

Once the `round` reaches 3 the game is over and this function according to the scores will give a winner or a tie:

```
def check_final_result_scores():
    if user_score > ia_score:
        return print("¡USER WIN!")
    elif ia_score > user_score:
        return print("¡IA WIN!")
    elif ia_score == user_score:
        return print("¡ITS A TIED GAME!")
```

This code will be executed until `round` is less than or equal to 3. The user will be asked for an option, the computer will choose an option and the `check_result_of_round()` function will be executed:

```
while round <= 3:
    print(f"Ronda {round}")
    ia_chosen = ia_choose[generate_random_number()]
    user_chosen = int(input("Choose a number: 0. Rock / 1. Paper / 2. Scissors: "))

    if user_chosen < 0 or user_chosen > 2 or type(user_chosen) != int:
        raise Exception("Insert a correct value.")

    check_result_of_round(ia_chosen, user_chosen)
    round += 1
```
