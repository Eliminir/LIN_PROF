## Строим бонды и вланы

## Цель:

Научиться настраивать VLAN и LACP;


## Описание/Пошаговая инструкция выполнения домашнего задания:

Для выполнения домашнего задания используйте методичку


## Что нужно сделать?

в Office1 в тестовой подсети появляется сервера с доп интерфейсами и адресами

в internal сети testLAN:

testClient1 - 10.10.10.254

testClient2 - 10.10.10.254

testServer1- 10.10.10.1

testServer2- 10.10.10.1

## Равести вланами:

testClient1 <-> testServer1

testClient2 <-> testServer2

Между centralRouter и inetRouter "пробросить" 2 линка (общая inernal сеть) и объединить их в бонд, проверить работу c отключением интерфейсов

Настройка bonding на inetRouter

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ24/1.png)

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ24/2.png)

На centralRouter 

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ24/3.png)

VLAN изоляция: 

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ24/4.png)

Bonding статус

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ24/5.png)




