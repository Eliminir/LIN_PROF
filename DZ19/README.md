## Домашнее задание

## Сценарии iptables

## Цель:

Написать сценарии iptables.


Описание/Пошаговая инструкция выполнения домашнего задания:
Что нужно сделать?

реализовать knocking port

centralRouter может попасть на ssh inetrRouter через knock скрипт

пример в материалах.

добавить inetRouter2, который виден(маршрутизируется (host-only тип сети для виртуалки)) с хоста или форвардится порт через локалхост.

запустить nginx на centralServer.

пробросить 80й порт на inetRouter2 8080.

дефолт в инет оставить через inetRouter


### 1. Проброс порта работает
curl http://192.168.100.2:8080

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ19/1.png)


### 2. Без knock порт 22 закрыт
sudo ip netns exec centralRouter nc -zv 192.168.255.1 22

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ19/2.png)

### 3. Выполняем knock (стучим в порты)
sudo ip netns exec centralRouter bash -c "nc -w 1 -z 192.168.255.1 1234 && nc -w 1 -z 192.168.255.1 5678 && nc -w 1 -z 192.168.255.1 9012"

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ19/3.png)

### 4. После knock IP появляется в AUTH списке
sudo ip netns exec inetRouter cat /proc/net/xt_recent/AUTH

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ19/4.png)

### 5. HTTP сервер на centralServer работает
sudo ip netns exec centralServer curl localhost:80

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ19/5.png)
