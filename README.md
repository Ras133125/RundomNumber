# RundomNumber
Запустите код на исполнение в редакторе. Это простоя игра на угадывание числа.

import random
computer_random = random.randint(1, 50)
count_of_tries = 6
#print(computer_random)
print('Я загадал число от 1 до 50. Отгадай его за 6 попыток!')

while count_of_tries > 0:
    human_random = int(input(f'Введите число. Количество попыток {count_of_tries} - '))
    if human_random == computer_random:
        print('Ты угадал!')
        break
    elif human_random < computer_random:
        print('Ваше число меньше, чем загадал компьютер :(')
    elif human_random > computer_random:
        print('Ваше число больше, чем загадал компьютер :(')
    count_of_tries -= 1
if count_of_tries == 0:
    print(f'У вас не осталось попыток. Моё число было {computer_random}')
if human_random == computer_random:
    print('Игра окончена в Вашу пользу!')
