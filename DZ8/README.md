
## Systemd - создание unit-файла

## Цель:

Научиться редактировать существующие и создавать новые unit-файлы;


## Описание/Пошаговая инструкция выполнения домашнего задания:


Выполнить следующие задания и подготовить развёртывание результата выполнения с использованием Vagrant и Vagrant shell provisioner (или Ansible, на Ваше усмотрение):

Написать service, который будет раз в 30 секунд мониторить лог на предмет наличия ключевого слова (файл лога и ключевое слово должны задаваться в /etc/default).


Установить spawn-fcgi и создать unit-файл (spawn-fcgi.sevice) с помощью переделки init-скрипта (https://gist.github.com/cea2k/1318020).


Доработать unit-файл Nginx (nginx.service) для запуска нескольких инстансов сервера с разными конфигурационными файлами одновременно.

## Решение

Создание файла конфигурации в /etc/default

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ8/1.png)

Создание тестового лог-файла

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ8/2.png)

Создание скрипта для мониторинга

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ8/3.png)

Создание юнита для сервиса/таймера

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ8/4.png)

проверка

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ8/5.png)

## Часть 2

Создание конфигурации \ unit-файла

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ8/6.png)

запуск сервиса 


![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ8/7.png)

## Часть 3

Манипуляции с nginx/создаем шаблонный unit-файл

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ8/8.png)

Создаем базовую конфигу

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ8/9.png)

Создаем конфиги для первого и второго инстанса

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ8/10.png)

перезапускаем сервисы и проверяем работу статус, порты и бла бла

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ8/11.png)

Добавляем в атозагрузку, проверяем процессы 

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ8/12.png)
