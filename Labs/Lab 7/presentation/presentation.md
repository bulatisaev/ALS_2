---
## Front matter
lang: ru-RU
title: Лабораторная Работа №7. Учёт физических параметров сети
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

![Открытие проекта lab_PT-07.pkt.](Images/1.png){ #fig:001 width=70%}


## Физическая рабочая область

![Открытие физической рабочей области Packet Tracer и присвоение названия городу.](Images/2.png){ #fig:002 width=70% }


## Физическая рабочая область

![Присвоение зданию названия Donskaya и добавление здания для территории Pavlovskaya.](Images/3.png){ #fig:003 width=70% }


## Физическая рабочая область

![Перемещение изображения, обозначающее серверное помещение, внутрь здания.](Images/4.png){ #fig:004 width=70% }


## Физическая рабочая область

![Перемещение коммутатора msk-pavlovskaya-baisaev-sw-1 на территорию Pavlovskaya.](Images/5.png){ #fig:005 width=70% }


## Физическая рабочая область

![Перемещение двух оконечных устройств (dk-pavlovskaya-1 и other-pavlovskaya-1)  на территорию Pavlovskaya.](Images/6.png){ #fig:006 width=70% }


## Ping

![Пинг с коммутатора msk-donskaya-baisaev-sw-1 коммутатора msk-pavlovskaya-baisaev-sw-1 (проверка работоспособности соединения).](Images/7.png){ #fig:007 width=70% }


## Активация разрешения

![Активация разрешения на учёт физических характеристик среды передачи.](Images/8.png){ #fig:008 width=70% }


## Физическая рабочая область

![Размещение двух территорий на расстоянии более 100м друг от друга.](Images/9.png){ #fig:009 width=70% }


## Ping

![Пинг с коммутатора msk-donskaya-baisaev-sw-1 коммутатора msk-pavlovskaya-baisaev-sw-1 (проверка неработоспособности соединения).](Images/10.png){ #fig:010 width=70% }


## Логическая рабочая область

![Удаление соединения между msk-donskaya-baisaev-sw-1 и msk-pavlovskaya-baisaev-sw-1, добавление в логическую рабочую область двух повторителей и присвоение им названий (msk-donskaya-baisaev-mc-1 и msk-pavlovskaya-baisaev-mc-1).](Images/11.png){ #fig:011 width=70% }


## Логическая рабочая область

![Замена имеющихся модулей на PT-REPEATERNM-1FFE и PT-REPEATER-NM-1CFE для подключения оптоволокна и витой пары по технологии Fast Ethernet.](Images/12.png){ #fig:012 width=70% }


## Физическая рабочая область

![Перемещение msk-pavlovskaya-baisaev-mc-1 на территорию Pavlovskaya.](Images/13.png){ #fig:013 width=70% }


## Логическая рабочая область

![Подключение: коммутатора msk-donskaya-baisaev-sw-1 к msk-donskaya-baisaev-mc-1 по витой паре, msk-donskaya-baisaev-mc-1 и msk-pavlovskaya-baisaev-mc-1 — по оптоволокну, msk-pavlovskaya-baisaev-sw-1 к msk-pavlovskaya-baisaev-mc-1 — по витой паре.](Images/14.png){ #fig:014 width=70% }


## Логическая рабочая область

![Проверка работоспособности соединения между msk-donskaya-baisaev-sw-1 и msk-pavlovskaya-baisaev-sw-1.](Images/15.png){ #fig:015 width=70% }


## Вывод
В ходе выполнения лабораторной работы мы получили навыки работы с физической рабочей областью Packet Tracer, а также научились учитывать физические параметры сети.
