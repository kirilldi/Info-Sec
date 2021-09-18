---
# Front matter
lang: ru-RU
title: "Лабораторная работа №1"
subtitle: "Информационная безопасность"
author: "Дидусь Кирилл Валерьевич"

# Formatting
toc-title: "Содержание"
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4paper
documentclass: scrreprt
polyglossia-lang: russian
polyglossia-otherlangs: english
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase
indent: true
pdf-engine: lualatex
header-includes:
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=700 # the penalty for breaking a line at a binary operator
  - \relpenalty=500 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=100 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

# Задание

- Создать виртуальную машину
- Установить на неё CentOS
- Провести первоначальную настройку CentOS
- Подготовить системный диск ко множественному использованию

# Выполнение лабораторной работы

## Создание и настройка виртуальной машины 

**Для создания новой виртуальной машины выполним следующие шаги: **

- В VirtualBox выбрать "Машина" -> "Создать". 
- Указать имя виртуальной машины — Base, тип операционной системы — Linux, RedHat. 
- Указать размер основной памяти виртуальной машины — 4096 МБ.
-  Задать конфигурацию жёсткого диска — загрузочный, VDI (VirtualBox Disk Image), динамический виртуальный диск. Размер диска должен быть  не менее 15 ГБ.

Запустим виртуальную машину Base, выберем образ для установки системы. 

## Установка CentOS 

**В ходе установки CentOS сконфигурируем систему следующим образом:** 

- Установим русский язык.
- Установим дату и время. 
- Выберем жёсткий диск для установки. 
- Выберем вариант установки "Рабочая станция". Дополнительно загрузим инструменты для разработки.
- Зададим имя узла.
- Зададим пароль для root. 
- Зададим имя пользователя и пароль, сделаем пользователя администратором. 

## Первоначальная настройка CentOS

Зайдём в терминал, выдадим права root с помощью команды **su** и обновим программы с помощью команды **yum update**. 
Установим файловый менеджер Midnight Commander с помощью команды **yum install mc**. 

## Подготовка системного диска ко множественному использованию

Для того чтобы подготовить диск Base.vdi к использованию на других виртуальных машинах, требуется:

1. В настройках виртуальной машины выбрать диск Base.vdi и освободить его.
2. В атрибутах выбрать *с множественным подключением*.

# Выводы

Приобрел практические навыки установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.