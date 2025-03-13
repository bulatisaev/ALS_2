---
## Front matter
lang: ru-RU
title: Лабораторная Работа №5. Конфигурирование VLAN
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

![Открытие проекта lab_PT-05.pkt.](Images/1.png){#fig:001 width=70%}


## Настройка Trunk-портов

![Настройка Trunk-портов на коммутаторе msk-donskaya-baisaev-sw-1.](Images/2.png){#fig:002 width=70%}


## Настройка Trunk-портов

![Настройка Trunk-портов на коммутаторе msk-donskaya-baisaev-sw-2.](Images/3.png){#fig:003 width=70%}


## Настройка Trunk-портов

![Настройка Trunk-портов на коммутаторе msk-donskaya-baisaev-sw-3.](Images/4.png){#fig:004 width=70%}


## Настройка Trunk-портов

![Настройка Trunk-портов на коммутаторе msk-donskaya-baisaev-sw-4.](Images/5.png){#fig:005 width=70%}


## Настройка Trunk-портов

![Настройка Trunk-портов на коммутаторе msk-pavlovskaya-baisaev-sw-1.](Images/6.png){#fig:006 width=70%}


## Настройка Trunk-портов

![Настройка коммутатора msk-donskaya-baisaev-sw-1 как VTP-сервера, добавление номеров и названий VLAN.](Images/7.png){#fig:007 width=70%}


## Настройка Trunk-портов

![Настройка коммутатора msk-donskaya-baisaev-sw-2 как VTP-клиента и указание принадлежности к VLAN.](Images/8.png){#fig:008 width=70%}


## Настройка Trunk-портов

![Настройка коммутатора msk-donskaya-baisaev-sw-3 как VTP-клиента и указание принадлежности к VLAN.](Images/9.png){#fig:009 width=70%}


## Настройка Trunk-портов

![Настройка коммутатора msk-donskaya-baisaev-sw-4 как VTP-клиента и указание принадлежности к VLAN.](Images/10.png){#fig:010 width=70%}

## Настройка Trunk-портов

![Настройка коммутатора msk-pavlovskaya-baisaev-sw-1 как VTP-клиента и указание принадлежности к VLAN.](Images/11.png){#fig:011 width=70%}


## Указание статических IP-адресов

![Пример указания статического IP-адреса на оконечном устройстве (Default Gateway).](Images/12.png){#fig:012 width=70%}


## Указание статических IP-адресов

![Проверка доступности устройств, принадлежащих одному VLAN, и недоступность устройств, принадлежащих разным VLAN.](Images/13.png){#fig:013 width=70%}


## Ping (доступность/недоступность)

![Проверка доступности устройств, принадлежащих одному VLAN, и недоступность устройств, принадлежащих разным VLAN.)](Images/14.png){#fig:014 width=70%}


## Режим симуляции в Packet Tracer, пакет ICMP

![Изучение процесса передвижения пакета ICMP (STP) по сети в режиме симуляции в Packet Tracer.](Images/15.png){#fig:015 width=70%}


## Вывод
В ходе выполнения лабораторной работы мы получили основные навыки по настройке VLAN на коммутаторах сети.
