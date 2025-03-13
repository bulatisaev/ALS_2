---
## Front matter
title: "Отчёт по лабораторной работе №14"
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
Настроить взаимодействие через сеть провайдера посредством статической маршрутизации локальной сети организации с сетью основного здания, расположенного в 42-м квартале в Москве, и сетью филиала, расположенного в г. Сочи.


# Выполнение лабораторной работы
Теперь откроем проект с названием lab_PT-13.pkt и сохраним под названием lab_PT-14.pkt. После чего откроем его для дальнейшего редактирования (рис. [-@fig:001]) 


![Открытие проекта lab_PT-14.pkt.](Images/1.png){ #fig:001 width=70% }


Первым делом нам нужно настроить линку между площадками. Для этого настроим интерфейсы у коммутатора provider-baisaev-sw-1, маршрутизатора msk-donskaya-baisaev-gw-1, маршрутизатора msk-q42-gw-1, коммутатора sch-sochi-sw-1 и маршрутизатора sch-sochi -gw-1  (рис. [-@fig:002]), (рис. [-@fig:003]), (рис. [-@fig:004]), (рис. [-@fig:005]), (рис. [-@fig:006]), (рис. [-@fig:007]), (рис. [-@fig:008])


![Настройка интерфейсов коммутатора provider-baisaev-sw-1.](Images/2.png){ #fig:002 width=70% }


![Настройка интерфейсов маршрутизатора msk-donskaya-baisaev-gw-1.](Images/3.png){ #fig:003 width=70% }


![Настройка интерфейсов маршрутизатора msk-q42-gw-1.](Images/4.png){ #fig:004 width=70% }


![Настройка интерфейсов коммутатора sch-sochi-sw-1.](Images/5.png){ #fig:005 width=70% }


![Настройка интерфейсов маршрутизатора sch-sochi-gw-1.](Images/6.png){ #fig:006 width=70% }


Следующим шагом настроим площадку 42-го квартала. Для этого настроим интерфейсы у маршрутизатора msk-q42-gw-1, коммутатора msk-q42-sw-1, маршрутизирующего коммутатора msk-hostel-gw-1 и коммутатора msk-hostel-sw-1 (рис. [-@fig:009]), (рис. [-@fig:010]), (рис. [-@fig:011]), (рис. [-@fig:012]), (рис. [-@fig:013]), (рис. [-@fig:014]), (рис. [-@fig:015]), (рис. [-@fig:016]), (рис. [-@fig:017])


![Настройка интерфейсов маршрутизатора msk-q42-gw-1.](Images/7.png){ #fig:007 width=70% }


![Настройка интерфейсов коммутатора msk-q42-sw-1.](Images/8.png){ #fig:008 width=70% }


![Присвоение адресов оконечному устройству pc-q42-1.](Images/9.png){ #fig:009 width=70% }


![Выполнение проверки.](Images/10.png){ #fig:010 width=70% }


![Настройка интерфейсов маршрутизирующего коммутатора msk-hostel-gw-1.](Images/11.png){ #fig:011 width=70% }


![Выполнение проверки.](Images/12.png){ #fig:012 width=70% }


![Настройка интерфейсов коммутатора msk-hostel-sw-1.](Images/13.png){ #fig:013 width=70% }


![Присвоение адресов оконечному устройству pc-hostel-1.](Images/14.png){ #fig:014 width=70% }


![Выполнение проверки.](Images/15.png){ #fig:015 width=70% }


Далее настроим площадку в Сочи. Настроим интерфейсы у маршрутизатора sch-sochi-gw-1 и у коммутатора sch-sochi-sw-1 (рис. [-@fig:018]), (рис. [-@fig:019]), (рис. [-@fig:020])


![Первоначальная настройка маршрутизатора sch-sochi-gw-1.](Images/16.png){ #fig:016 width=70% }


![Первоначальная настройка коммутатора sch-sochi-sw-1.](Images/17.png){ #fig:017 width=70% }


![Присвоение адресов оконечному устройству pc-sochi-1.](Images/18.png){ #fig:018 width=70% }


Затем настроим маршрутизацию между площадками. Настроим маршрутизатор msk-donskaya-baisaev-gw-1, маршрутизатор msk-q42-gw-1 и маршрутизатор sch-sochi-gw-1 (рис. [-@fig:021]), (рис. [-@fig:022]), (рис. [-@fig:023]), (рис. [-@fig:024]), (рис. [-@fig:025])


![Настройка маршрутизатора msk-donskaya-baisaev-gw-1.](Images/19.png){ #fig:019 width=70% }


![Выполнение проверки.](Images/20.png){ #fig:020 width=70% }


![Настройка маршрутизатора msk-q42-gw-1.](Images/21.png){ #fig:021 width=70% }


![Выполнение проверки.](Images/22.png){ #fig:022 width=70% }


![Настройка маршрутизатора sch-sochi-gw-1.](Images/23.png){ #fig:023 width=70% }


Предпоследним шагом настроим маршрутизацию на 42 квартале. Для этого настроим маршрутизатор msk-q42-gw-1 (рис. [-@fig:025]) и маршрутизирующий коммутатор msk-hostel-gw-1 (рис. [-@fig:025])


![Настройка маршрутизатора msk-q42-gw-1.](Images/24.png){ #fig:024 width=70% }


![Настройка интерфейсов маршрутизирующего коммутатора msk-hostel-gw-1.](Images/25.png){ #fig:025 width=70% }


И наконец последним шагом настроим NAT на маршрутизаторе msk-donskaya-baisaev-gw-1 (рис. [-@fig:026]) и выполним контрольную проверку (рис. [-@fig:027])


![Настройка NAT на маршрутизаторе msk-donskaya-baisaev-gw-1.](Images/26.png){ #fig:026 width=70% }


![Контрольная проверка.](Images/27.png){ #fig:027 width=70% }


# Вывод

В ходе выполнения лабораторной работы мы настроили взаимодействие через сеть провайдера посредством статической маршрутизации локальной сети организации с сетью основного здания, расположенного в 42-м квартале в Москве, и сетью филиала, расположенного в г. Сочи.


##  Контрольные вопросы

1. Приведите пример настройки статической маршрутизации между двумя подсетями организации - 
  
   **Необходимо задать IP шлюзов на интерфейсах, настроить sub-интерфейсы с тегированием кадром VLAN'ами и своими IP, затем настроить статические маршруты между сетями.**

2. Опишите процесс обращения устройства из одного VLAN к устройству из другого VLAN. - 
  
   **1 устройство посылает фрейм на маршрутизатор, тот меняет MAC исходника на свой и перенаправляет фрейм 2 устройству.**

3. Как проверить работоспособность маршрута?  - 
  
    **AAping на диаметрально противоположных устройствах друг к другу.AAAAAAAAAAAAAAAAAAAAA**

4. Как посмотреть таблицу маршрутизации?  - 
  
    **show ip route**
