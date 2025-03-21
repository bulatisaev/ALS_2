---
## Front matter
title: "Отчёт по лабораторной работе №15"
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
Настроить динамическую маршрутизацию между территориями организации.



# Выполнение лабораторной работы
Теперь откроем проект с названием lab_PT-14.pkt и сохраним под названием lab_PT-15.pkt. После чего откроем его для дальнейшего редактирования (рис. [-@fig:001]) 


![Открытие проекта lab_PT-15.pkt.](Images/1.png){ #fig:001 width=70% }


Для начала настроим OSPF на маршрутизаторе msk-donskaya-baisaev-gw-1. Включение OSPF на маршрутизаторе предполагает, во-первых, включение процесса OSPF командой router ospf, во-вторых — назначение областей (зон) интерфейсам с помощью команды network area  (рис. [-@fig:002]) 
Идентификатор процесса OSPF (process-id) по сути идентифицирует маршрутизатор в автономной системе, и, вообще говоря, он не должен совпадать с идентификаторами процессов на других маршрутизаторах. 
Значение идентификатора области (area-id) может быть целым числом от 0 до 4294967295 или может быть представлено в виде IP-адреса: A.B.C.D. Область 0 называется магистралью, области с другими идентификаторами должны подключаться к магистрали.


![Настройка OSPF на маршрутизаторе msk-donskaya-baisaev-gw-1 (включение процесса OSPF, назначение областей интерфейсам).](Images/2.png){ #fig:002 width=70% }


Проверим состояние протокола OSPF на маршрутизаторе msk-donskaya-baisaev-gw-1. Маршрутизаторы с общим сегментом являются соседями в этом сегменте. Соседи выбираются с помощью протокола Hello. Команда show ip ospf neighbor показывает статус всех соседей в заданном сегменте. Команда show ip ospf route (или show ip route) выводит информацию из таблицы маршрутизации  (рис. [-@fig:003]) 


![Проверка состояния протокола OSPF на маршрутизаторе msk-donskaya-baisaev-gw-1 (просмотр статуса всех соседей в заданном сегменте, вывод информации из таблицы маршрутизации).](Images/3.png){ #fig:003 width=70% }


Далее приступим к настройке: маршрутизатора msk-q42-gw-1, маршрутизирующего коммутатора msk-hostel-gw-1, маршрутизатора sch-sochi-gw-1 (рис. [-@fig:004]), (рис. [-@fig:005]), (рис. [-@fig:006])


![Настройка маршрутизатора msk-q42-gw-1.](Images/4.png){ #fig:004 width=70% }


![Настройка маршрутизирующего коммутатора msk-hostel-gw-1.](Images/5.png){ #fig:005 width=70% }


![Настройка маршрутизатора sch-sochi-gw-1.](Images/6.png){ #fig:006 width=70% }


Теперь проверим состояние протокола OSPF на всех маршрутизаторах  (рис. [-@fig:007]), (рис. [-@fig:008]), (рис. [-@fig:009]) 


![Проверка состояния протокола OSPF на маршрутизаторе msk-q42-gw-1.](Images/7.png){ #fig:007 width=70% }


![Проверка состояния протокола OSPF на маршрутизирующем коммутаторе msk-hostel-gw-1.](Images/8.png){ #fig:008 width=70% }


![Проверка состояния протокола OSPF на маршрутизаторе sch-sochi-gw-1.](Images/9.png){ #fig:009 width=70% }


Следующим шагом настроим линк 42-й квартал–Сочи (рис. [-@fig:010]), (рис. [-@fig:011]), (рис. [-@fig:012]), (рис. [-@fig:013])


![Настройка интерфейсов коммутатора provider-baisaev-sw-1.](Images/10.png){ #fig:010 width=70% }


![Настройка маршрутизатора msk-q42-gw-1.](Images/11.png){ #fig:011 width=70% }


![Настройка коммутатора sch-sochi-sw-1..](Images/12.png){ #fig:012 width=70% }


![Настройка маршрутизатора sch-sochi-gw-1.](Images/13.png){ #fig:013 width=70% }

В режиме симуляции отследим движение пакета ICMP с ноутбука администратора сети на Донской в Москве (admin-donskaya-baisaev) до компьютера пользователя в филиале в г. Сочи pc-sochi-1 (рис. [-@fig:014]), (рис. [-@fig:015])


![Ping по адресу 10.130.0.200.](Images/14.png){ #fig:014 width=70% }


![Отслеживание в режиме симуляции движения пакета ICMP (OSPF) с ноутбука администратора сети на Донской в Москве до компьютера пользователя в филиале в г. Сочи.](Images/15.png){ #fig:015 width=70% }


Следующим шагом на коммутаторе провайдера отключим временно vlan 6 и в режиме симуляции убедимся в изменении маршрута прохождения пакета ICMP с ноутбука администратора сети на Донской в Москве до компьютера пользователя в филиале в г. Сочи (рис. [-@fig:016]), (рис. [-@fig:017]) 


![Временное отключение на коммутаторе провайдера vlan 6.](Images/16.png){ #fig:016 width=70% }


![Проверка изменения маршрута прохождения пакета ICMP в режиме симуляции с ноутбука администратора сети на Донской в Москве до компьютера пользователя в филиале в г. Сочи.](Images/17.png){ #fig:017 width=70% }


На коммутаторе провайдера восстановим vlan 6 и в режиме симуляции вновь убедимся в изменении маршрута прохождения пакета ICMP (рис. [-@fig:018]), (рис. [-@fig:019]), (рис. [-@fig:020])


![Потеря пакетов.](Images/18.png){ #fig:018 width=70% }


![Восстановление на коммутаторе провайдера vlan 6.](Images/19.png){ #fig:019 width=70% }


![Проверка изменения маршрута прохождения пакета ICMP в режиме симуляции с ноутбука администратора сети на Донской в Москве до компьютера пользователя в филиале в г. Сочи.](Images/20.png){ #fig:020 width=70% }


# Вывод

В ходе выполнения лабораторной работы мы настроили динамическую маршрутизацию между территориями организации.


##  Контрольные вопросы

1. Какие протоколы относятся к протоколам динамической маршрутизации?  - 
  
   **OSPF, RIP, EIGRP.**

2. Охарактеризуйте принципы работы протоколов динамической маршрутизации.  - 
  
   **Маршрутизаторы по протоколу делятся между собой информацией из своих таблиц маршрутизации и корректируют их в соответствии с остальными.**

3. Опишите процесс обращения устройства из одной подсети к устройству из другой подсети по протоколу динамической маршрутизации. - 
  
    **Вектор-Расстояние — маршрутизатор рассылает список адресов со сборным параметром расстояния (кол-во маршрутизаторов, производительность и т. д.) из доступных сетей. Состояние канала — маршрутизаторы обмениваются топологической (связи маршрутизаторов) информацией.**

4. Опишите выводимую информацию при просмотре таблицы маршрутизации. - 
  
    **Протокол Тип маршрута Адрес удаленной сети [Административная дистанция источника/Метрика маршрута] Следующий маршрутизатор Время последнего обновления маршрута Интерфейс.**
