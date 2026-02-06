## Домашнее задание

Сборка RPM-пакета и создание репозитория

## Цель:
Научиться собирать RPM-пакеты.
Создавать собственный RPM-репозиторий.


## Описание/Пошаговая инструкция выполнения домашнего задания:

🎯 Что нужно сделать?

создать свой RPM (можно взять свое приложение, либо собрать к примеру Apache с определенными опциями);

cоздать свой репозиторий и разместить там ранее собранный RPM;

реализовать это все либо в Vagrant, либо развернуть у себя через Nginx и дать ссылку на репозиторий.

Решение


Подготовка, установка зависимостей и бла бла

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ7/1.png)

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ7/2.png)

Сборка модуля ngx_brotli

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ7/3.png)

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ7/4.png)

 Редактируем spec-файл Nginx 

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ7/5.png)

приступаем к сборке RPM пакета

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ7/6.png)

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ7/7.png)

Создаем свой репозиторий и размещаем там ранее собранный RPM

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ7/8.png)

меняем конфиг nginx, перезапускаем и проверяем наш локальный репозиторий

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ7/9.png)

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ7/10.png)

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ7/11.png)

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ7/12.png)

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ7/14.png)



