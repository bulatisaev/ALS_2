---
## Front matter
lang: ru-RU
title: Лабораторная Работа №9. Использование протокола STP. Агрегирование каналов.
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

![Открытие проекта lab_PT-09.pkt.](Images/1.png){ #fig:001 width=70% }


## Резервное соединение 

![Формирование резервного соединения между коммутаторами msk-donskaya-baisaev-sw-1 и msk-donskaya-baisaev-sw-3 (замена соединения между коммутаторами).](Images/2.png){ #fig:002 width=70% }


## Настройка порта

![Настройка порта на интерфейсе Gig0/2 коммутатора msk-donskaya-baisaev-sw-3 как транковый.](Images/3.png){ #fig:003 width=70% }


## Соединение

![Соединение между коммутаторами msk-donskaya-baisaev-sw-1 и msk-donskaya-baisaev-sw-4 через интерфейсы Fa0/23. ](Images/4.png){ #fig:004 width=70% }


## Активация (транковый режим)

![Активация в транковом режиме интерфейса Fa0/23 на коммутаторе msk-donskaya-baisaev-sw-1.](Images/5.png){ #fig:005 width=70% }


## Активация (транковый режим)

![Активация в транковом режиме интерфейса Fa0/23 на коммутаторе msk-donskaya-baisaev-sw-4. ](Images/6.png){ #fig:006 width=70% }


## Ping mail и web

![Проверка командой ping серверов mail и web с оконечного устройства dk-donskaya-1.](Images/7.png){ #fig:007 width=70% }


## Отслеживание пакетов ICMP (DHCP)

![Отслеживание пакетов ICMP (DHCP) в режиме симуляции (web) (движение пакетов происходит через коммутатор msk-donskaya-baisaev-sw-2).](Images/8.png){ #fig:008 width=70% }


## Отслеживание пакетов ICMP

![Отслеживание пакетов ICMP в режиме симуляции (mail) (движение пакетов происходит через коммутатор msk-donskaya-baisaev-sw-2). ](Images/9.png){ #fig:009 width=70% }


## Просмотр состояния STP

![Просмотр на коммутаторе msk-donskaya-baisaev-sw-2 состояния протокола STP для vlan 3 (указывается, что данное устройство является корневым (This bridge is the root)).](Images/10.png){ #fig:010 width=70% }


## Настройка корневого коммутатора STP

![Настройка в качестве корневого коммутатора STP коммутатора msk-donskaya-baisaev-sw-1.](Images/11.png){ #fig:011 width=70% }


## Настройка режима Portfast

![Настройка режима Portfast на интерфейсах коммутатора msk-donskaya-baisaev-sw-2.](Images/12.png){ #fig:012 width=70% }


## Настройка режима Portfast

![Настройка режима Portfast на интерфейсах коммутатора msk-donskaya-baisaev-sw-3.](Images/13.png){ #fig:013 width=70% }


## Изучение отказоустойчивости

![Изучение отказоустойчивости протокола STP и времени восстановления соединения при переключении на резервное соединение.](Images/14.png){ #fig:014 width=70% }


## Изучение отказоустойчивости

![Изучение отказоустойчивости протокола STP и времени восстановления соединения при переключении на резервное соединение.](Images/15.png){ #fig:015 width=70% }


## Переключение в Rapid PVST+

![Переключение коммутаторов в режим работы по протоколу Rapid PVST+ (на примере msk-donskaya-baisaev-sw-1).](Images/16.png){ #fig:016 width=70% }


## Изучение отказоустойчивости

![Изучение отказоустойчивости протокола Rapid PVST+ и времени восстановления соединения при переключении на резервное соединение.](Images/17.png){ #fig:017 width=70% }


## Изучение отказоустойчивости

![Изучение отказоустойчивости протокола Rapid PVST+ и времени восстановления соединения при переключении на резервное соединение.](Images/18.png){ #fig:018 width=70% }


## Агрегированное соединение

![Формирование агрегированного соединение интерфейсов Fa0/20 – Fa0/23 между коммутаторами msk-donskaya-baisaev-sw-1 и msk-donskaya-baisaev-sw-4.](Images/19.png){ #fig:019 width=70% }


## Агрегированное соединение

![Формирование агрегированного соединение интерфейсов Fa0/20 – Fa0/23 между коммутаторами msk-donskaya-baisaev-sw-1 и msk-donskaya-baisaev-sw-4.](Images/20.png){ #fig:020 width=70% }


## Агрегированное соединение

![Формирование агрегированного соединение интерфейсов Fa0/20 – Fa0/23 между коммутаторами msk-donskaya-baisaev-sw-1 и msk-donskaya-baisaev-sw-4.](Images/21.png){ #fig:021 width=70% }


## Вывод
В ходе выполнения лабораторной работы мы изучили возможности протокола STP и его модификаций по обеспечению отказоустойчивости сети, агрегированию интерфейсов и перераспределению нагрузки между ними.
