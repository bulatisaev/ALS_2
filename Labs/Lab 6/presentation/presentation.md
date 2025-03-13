---
## Front matter
lang: ru-RU
title: Лабораторная Работа №6. Статическая маршрутизация VLAN 
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


## Новый проект

![Открытие проекта lab_PT-06.pkt.](Images/1.png){ #fig:001 width=70%}


## Настройка Trunk-портов

![Размещение маршрутизатора Cisco 2811 в логической области проекта и подключение его к порту 24 коммутатора msk-donskaya-baisaev-sw-1.](Images/2.png){ #fig:002 width=70% }


## Настройка Trunk-портов

![Конфигурация маршрутизатора: имя, пароль для доступа к консоли и настройка удалённого подключение к нему по ssh.](Images/3.png){ #fig:003 width=70% }


## Настройка Trunk-портов

![Настройка порта 24 коммутатора msk-donskaya-baisaev-sw-1 как trunk-порт.](Images/4.png){ #fig:004 width=70% }


## Настройка Trunk-портов

![Изменение на схеме наименование маршрутизатора Cisco 2811. ](Images/5.png){ #fig:005 width=70% }


## Настройка Trunk-портов

![Настройка на интерфейсе f0/0 маршрутизатора msk-donskaya- baisaev-gw-1 виртуальных интерфейсов, соответствующих номерам VLAN. Настройка соответствующих IP-адресов на виртуальных интерфейсах согласно таблице IP-адресов.](Images/6.png){ #fig:006 width=70% }


## Настройка Trunk-портов

![Проверка доступности оконечных устройств из разных VLAN.](Images/7.png){ #fig:007 width=70% }


## Вывод
В ходе выполнения лабораторной работы мы научились настраивать статическую маршрутизацию VLAN в сети.
