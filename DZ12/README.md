## Первые шаги с Ansible

## Цель:
написать первые шаги с Ansible;


## Описание/Пошаговая инструкция выполнения домашнего задания:

## 🎯 Что нужно сделать?

Подготовить стенд на Vagrant как минимум с одним сервером. На этом сервере, используя Ansible, необходимо развернуть nginx со следующими условиями:

необходимо использовать модуль yum/apt;

конфигурационные файлы должны быть взяты из шаблона jinja2 с переменными;

после установки nginx должен быть в режиме enabled в systemd;

должен быть использован notify для старта nginx после установки;

сайт должен слушать на нестандартном порту — 8080, для этого использовать переменные в Ansible.


установка Ansible

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ12/1.png)

Создаем tasks/main.yml; handlers/main.yml; vars/main.yml с портом 8080; шаблон конфигурации nginx; плейбук.


![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ12/2.png)

тыкаем в ранее созданный плейбук, проверяем что nginx завелся как нам надо 

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ12/3.png)
