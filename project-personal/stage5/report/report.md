---
## Front matter
title: "Отчет по пятому этапу реализации проекта"
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

Burp Suite представляет собой набор мощных инструментов безопасности веб-приложений, которые демонстрируют реальные возможности злоумышленника, проникающего в веб-приложения. 


# Выполнение 

Запускаем Burp Suite в терминале (рис. [-@fig:001]).

![Запускаем](image/1.png){#fig:001 width=70%}
     
Включаем intercept в Burp Suite. Пишем логин и неверный пароль на сайте DVWA (рис. [-@fig:002]).

![Пишем](image/2.png){#fig:002 width=70%}

Перехватываем запрос с неверным паролем (рис. [-@fig:003])

![пароль](image/3.png){#fig:003 width=70%}

Модификация параметра password в Burp Suite (рис. [-@fig:004]).

![Модификация](image/4.png){#fig:004 width=70%}

Успешный вход в DVWA после модификации запроса (рис. [-@fig:003])

![сайт DVWA](image/5.png){#fig:005 width=70%}


# Выводы

Мы научились пользоваться Burp Suite.

