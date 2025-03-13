---
## Front matter
lang: ru-RU
title: Лабораторная Работа №2. Предварительная настройка оборудования Cisco
subtitle: Администрирование локальных сетей
author:
  - Исаев Б.А.
institute:
  - Российский университет дружбы народов им. Патриса Лумумбы, Москва, Россия

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'

## Fonts
mainfont: Arial
romanfont: Arial
sansfont: Arial
monofont: Arial
---


## Докладчик


  * Исаев Булат Абубакарович
  * НПИбд-01-22
  * Российский университет дружбы народов
  * [1132227131@pfur.ru]


## Создание проекта

![Создание нового проекта.](Images/1.png){ #fig:001 width=70% }


## Конфигурирование оборудования Cisco

![AAAAAAAAAAAAРазмещение коммутатора, маршрутизатора и двух оконечных устройств. Последующие соединение.AAAAAAAAAAA](Images/2.png){ #fig:002 width=70% }


## Конфигурирование оборудования Cisco

![Присвоение статического IP-адреса и маски подсети.](Images/3.png){ #fig:003 width=70% }


## Конфигурирование оборудования Cisco

![Проведение настройки маршрутизатора.](Images/4.png){ #fig:004 width=70% }


## Конфигурирование оборудования Cisco

![Проведение настройки коммутатора.](Images/5.png){ #fig:005 width=70% }


## Конфигурирование оборудования Cisco

![Проверка работоспособности соединения PC0-baisaev -> msk-baisaev-gw-1. ](Images/6.png){ #fig:006 width=70% }


## Конфигурирование оборудования Cisco

![Проверка работоспособности соединения PC1-baisaev -> msk-baisaev-sw-1.](Images/7.png){ #fig:007 width=70% }


## Конфигурирование оборудования Cisco

![Попытка подключения к маршрутизатору разными способами: с помощью консольного кабеля, по протоколу удалённого доступа (telnet, ssh).](Images/8.png){ #fig:008 width=70% }


## Конфигурирование оборудования Cisco

![Попытка подключения к коммутатору разными способами: с помощью консольного кабеля, по протоколу удалённого доступа (telnet, ssh). ](Images/9.png){ #fig:009 width=70% }


## Вывод

В ходе выполнения лабораторной работы были получены основные навыки по начальному конфигурированию оборудования Cisco.