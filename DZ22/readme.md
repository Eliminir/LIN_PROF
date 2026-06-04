
## Настраиваем split-dns

## Цель:
Создать домашнюю сетевую лабораторию;

Изучить основы DNS;

Научиться работать с технологией Split-DNS в Linux-based системах.


## Описание/Пошаговая инструкция выполнения домашнего задания:

Для выполнения домашнего задания используйте методичку


## Что нужно сделать?


web1 - смотрит на клиент1

web2 смотрит на клиент2

завести еще одну зону newdns.lab

завести в ней запись

www - смотрит на обоих клиентов

настроить split-dns

клиент1 - видит обе зоны, но в зоне dns.lab только web1

клиент2 видит только dns.lab


ns01

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ22/1.png)

APX

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ22/2.png)

klient 01\02

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ22/3.png)
