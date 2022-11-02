# Rock-Paper-Scissors-Script

## Getting Started

1. Clone the repository
2. Join to the correct path of the clone
3. Use `python rockpaperscissors.py` to execute script

## Description

I made a web page that allows you to play the memory game. You have to find the even cards, to know which ones are even you have to search among the different foods, if you find two apples you add points and you add a pair. Once you finish playing and you have found all your pairs it will calculate the time it took you to finish.

## Feel free to edit my code

Possible options for the IA

```
ia_choose = ["rock", "paper", "scissors"]
```

Check result of one round

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

Check final result

```
def check_final_result_scores():
    if user_score > ia_score:
        return print("¡USER WIN!")
    elif ia_score > user_score:
        return print("¡IA WIN!")
    elif ia_score == user_score:
        return print("¡ITS A TIED GAME!")
```

## Technologies used

1. Python

## Libraries used

1. random

## Galery

![rock,paper,scissors](https://raw.githubusercontent.com/DiegoLibonati/DiegoLibonatiWeb/main/data/projects/Python/Imagenes/rcspython-0.jpg)

![rock,paper,scissors](https://raw.githubusercontent.com/DiegoLibonati/DiegoLibonatiWeb/main/data/projects/Python/Imagenes/rcspython-1.jpg)

![rock,paper,scissors](https://raw.githubusercontent.com/DiegoLibonati/DiegoLibonatiWeb/main/data/projects/Python/Imagenes/rcspython-2.jpg)

## Portfolio Link

`https://diegolibonati.github.io/DiegoLibonatiWeb/#/projects?q=Rock,%20paper%20or%20scissors%20script`

## Video
