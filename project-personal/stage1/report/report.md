---
## Front matter
title: "Отчет по первому этапу реализации проекта"
subtitle: "Тестирование веб приложений"
author: "Кичигина Полина Евгеньевна"

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
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
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

Этап 1. Установка Kali Linux

    Установите дистрибутив Kali Linux в виртуальную машину.
    
    В качестве среды виртуализации предлагается использовать VirtualBox.
    
    Сайт Kali Linux: https://www.kali.org/
    
    Учётные данные по умолчанию:
        логин: root;
        пароль: toor.

# Выполнение первого этапа

1. Скачиваем iso образ диска (рис. [-@fig:001])

![Скачивание](image/1.png){#fig:001 width=70%}

2. Настраиваем операционную систему (рис. [-@fig:002])

![Настройка](image/2.png){#fig:002 width=70%}

3. Ждем загрузку (рис. [-@fig:003])

![Загрузка](image/3.png){#fig:003 width=70%}

4. Запускаем операционную систему (рис. [-@fig:004]).

![Запуск](image/4.png){#fig:004 width=70%}



# Выводы

Мы научились устанавливать дистрибутив Kali Linux в виртуальную машину.

