---
## Front matter
lang: ru-RU
title: Лабораторная Работа №16. Настройка VPN.
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


## Открытие проекта

![Открытие проекта lab_PT-16.pkt.](Images/1.png){ #fig:001 width=70% }


## Размещение оборудования

![Размещение оборудования в рабочей области проекта.](Images/2.png){ #fig:002 width=70% }


## Замена модулей

![Замена модулей на Repeater-PT.](Images/3.png){ #fig:003 width=70% }


## Подключение

![Подключение оборудования.](Images/4.png){ #fig:004 width=70% }


## Создание города

![Создание города Пиза в физической рабочей области.](Images/5.png){ #fig:005 width=70% }


## Перемещение оборудования

![Перемещение оборудования.](Images/6.png){ #fig:006 width=70% }


## Первоначальная настройка

![Первоначальная настройка маршрутизатора pisa-unipi-baisaev-gw-1.](Images/7.png){ #fig:007 width=70% }


## Первоначальная настройка

![Первоначальная настройка коммутатора pisa-unipi-baisaev-sw-1.](Images/8.png){ #fig:008 width=70% }


## Настройка интерфейсов

![Настройка интерфейсов маршрутизатора pisa-unipi-baisaev-gw-1. ](Images/9.png){ #fig:009 width=70% }


## Настройка интерфейсов

![Настройка интерфейсов коммутатора pisa-unipi-baisaev-sw-1.](Images/10.png){ #fig:010 width=70% }


## Присвоение адресов

![Присвоение адресов оконечному устройству.](Images/11.png){ #fig:011 width=70% }


## Ping

![Пинг адреса 10.131.0.1..](Images/12.png){ #fig:012 width=70% }


## Настройка VPN на основе GRE 

![Настройка маршрутизатора msk-donskaya-baisaev-gw-1.](Images/13.png){ #fig:013 width=70% }


## Настройка VPN на основе GRE 

![Настройка маршрутизатора pisa-unipi-baisaev-gw-1.](Images/14.png){ #fig:014 width=70% }


## Проверка

![Проверка доступности узлов сети Университета г. Пиза с ноутбука администратора сети «Донская».](Images/15.png){ #fig:015 width=70% }


## Вывод

В ходе выполнения лабораторной работы мы получили навыки настройки VPN-туннеля через незащищённое Интернет-соединение.
