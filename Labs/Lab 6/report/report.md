---
## Front matter
title: "Отчёт по лабораторной работе №6"
subtitle: "Дисциплина: Администрирование локальных сетей"
author: "Исаев Булат Абубакарович НПИбд-01-22"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: Arial
romanfont: Arial
sansfont: Arial
monofont: Arial
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Настроить статическую маршрутизацию VLAN в сети.


# Выполнение лабораторной работы

Откроем проект с названием lab_PT-05.pkt и сохраним под названием lab_PT-06.pkt. После чего откроем его для дальнейшего редактирования  (рис. [-@fig:001])


![Открытие проекта lab_PT-06.pkt.](Images/1.png){ #fig:001 width=70% }


В логической области проекта разместим маршрутизатор Cisco 2811, подключим его к порту 24 коммутатора msk-donskaya-baisaev-sw-1 в соответствии с таблицей портов  (рис. [-@fig:002]) 


![Размещение маршрутизатора Cisco 2811 в логической области проекта и подключение его к порту 24 коммутатора msk-donskaya-baisaev-sw-1.](Images/2.png){ #fig:002 width=70% }


Используя приведённую последовательность команд в лабораторной работе по первоначальной настройке маршрутизатора, сконфигурируем маршрутизатор, задав на нём имя, пароль для доступа к консоли и настроим удалённое подключение к нему по ssh  (рис. [-@fig:003]) 



![Конфигурация маршрутизатора: имя, пароль для доступа к консоли и настройка удалённого подключение к нему по ssh.](Images/3.png){ #fig:003 width=70% }


Теперь настроим порт 24 коммутатора msk-donskaya-baisaev-sw-1 как trunk-порт  (рис. [-@fig:004]) 


![Настройка порта 24 коммутатора msk-donskaya-baisaev-sw-1 как trunk-порт.](Images/4.png){ #fig:004 width=70% }


![Изменение на схеме наименование маршрутизатора Cisco 2811. ](Images/5.png){ #fig:005 width=70% }


На интерфейсе f0/0 маршрутизатора msk-donskaya-baisaev-gw-1 настроим виртуальные интерфейсы, соответствующие номерам VLAN. Согласно таблице IP-адресов зададим соответствующие IP-адреса на виртуальных интерфейсах (рис. [-@fig:006]) 


![Настройка на интерфейсе f0/0 маршрутизатора msk-donskaya- baisaev-gw-1 виртуальных интерфейсов, соответствующих номерам VLAN. Настройка соответствующих IP-адресов на виртуальных интерфейсах согласно таблице IP-адресов.](Images/6.png){ #fig:006 width=70% }


После всех настроек проверим доступность оконечных устройств из разных VLAN (рис. [-@fig:007]) 


![Проверка доступности оконечных устройств из разных VLAN.](Images/7.png){ #fig:007 width=70% }


Используя режим симуляции в Packet Tracer, изучим процесс передвижения пакета ICMP по сети (У меня ICMP не появляется к сожалению):


# Вывод

В ходе выполнения лабораторной работы мы научились настраивать статическую маршрутизацию VLAN в сети.


##  Контрольные вопросы
1. Охарактеризуйте стандарт IEEE 802.1Q 
  
   **открытый стандарт, который описывает процедуру тегирования трафика для передачи информации о принадлежности к VLAN по сетям стандарта IEEE 802.3 Ethernet.**

2. Опишите формат кадра IEEE 802.1Q
  
   **добавляет 32-битное поле между MAC-адресом источника и полями EtherType исходного кадра. В соответствии с 802.1Q минимальный размер кадра остается 64 байта, но мост может увеличить минимальный размер кадра с 64 до 68 байтов при передаче IEEE 802.1Q.**


# Список литературы{.unnumbered}

::: {#refs}
::: 