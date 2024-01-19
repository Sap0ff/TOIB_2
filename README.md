# TOIB_2
# Отчет по ПР-2 "Идентификация и аутентификация" Сапова А.Д.


## Шаги выполнения


# Шаг 1


Срздаем суперпользователя Super-Sapov.A.D
 sudo useradd Super-Sapov.A.D
 
 sudo usermod -a -G sudo Super-Sapov.A.D
 
 passwd Super-Sapov.A.D
 
![1](https://github.com/Sap0ff/TOIB_2/assets/146374157/4bfaedf3-f672-416d-83d8-11bfbda344bd)


# Шаг 2

Создаем группу group-BBMO-02-23.

sudo groupadd BBMO-02-23

sudo usermod -aG BBMO-02-23 Super-Sapov.A.D


![2](https://github.com/Sap0ff/TOIB_2/assets/146374157/3acd7a8f-d28b-460e-9ce7-08263a51ec88)


# Шаг 3

Создаем обычного пользователя User-Sapov.A.D и и добавляем его в ранее созданную группу.

sudo useradd -U -m -s /bin/bash -G BBMO-02-23 User-Sapov.A.D

passwd User-Sapov.A.D

![3](https://github.com/Sap0ff/TOIB_2/assets/146374157/d147775c-e434-4cf8-9d8c-f01a0128a284)


# Шаг 4
Проверяем наличие пользователя User-Sapov.A.D и суперпользователя Super-Sapov.A.D в группе group-BBMO-02-23.

groups User-Sapov.A.D

groups Super-Sapov.A.D

![4](https://github.com/Sap0ff/TOIB_2/assets/146374157/15a8433e-a4ce-473a-8e56-f3cbd3996c8c)


# Шаг 5
Наделяем полномочиями пользователя User-Sapov.A.D

sudo chmod 770 ~

sudo chown Super-Sapov.A.D:BBMO-02-23 ~


# Шаг 7
Проверка механизмов разграничения доступа.

mkdir 1.txt

touch 1.txt

rm 1.txt
Practice_2
