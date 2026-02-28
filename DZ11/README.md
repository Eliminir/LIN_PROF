Практика с SELinux



Цель

Диагностировать проблемы и модифицировать политики SELinux для корректной работы приложений.

Смотрим порты nginx, и то что он "поломан"

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ11/1.png)

Способ 1: Использование setsebool

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ11/2.png)

Способ 2: Добавление порта в тип http_port_t

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ11/3.png)
