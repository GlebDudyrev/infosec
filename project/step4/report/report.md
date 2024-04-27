---
## Front matter
title: "Отчёт по индивидуальному проекту №4"
subtitle: "Дисциплина: Основы информационной безопасности"
author: "Дудырев Глеб Андреевич НПИбд-01-22"

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

Знакомство с базовым сканером безопасности nikto, его применение.

# Выполнение лабораторной работы

1. Вывожу справку об утилите nikto командой *nikto -h* (рис. [-@fig:001])

![nikto -h](image/1.png){ #fig:001 width=70% }

2. Сканирую веб-сайт youtube.ru на наличие уязвимостей с помощью команды *nikto -h youtube.ru*. Утилита показала отсутствие некоторых важных для безопасности заголовков (рис. [-@fig:002])

![Сканирование сайта gosuslugi.ru](image/4.png){ #fig:002 width=70% }

3. Сканирую локальный хост на наличие уязвимостей с помощью команды *nikto -h 127.0.0.1* (рис. [-@fig:003])

![Сканирование локалхоста](image/2.png){ #fig:003 width=70% }

4. Сканирую приложение DVWA с помощью команды *nikto -h http://127.0.0.1/DVWA*. nikto также указывает на отсутствие важных заголовков и выводит информацию о различных доступных эндпоинтах (рис. [-@fig:004])

![Сканирование DVWA](image/3.png){ #fig:004 width=70% }

# Выводы

Я познакомился с nikto, научился его применять на практике для проверки уязвимостей различных сайтов
