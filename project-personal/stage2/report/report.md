---
## Front matter
title: "Отчет по второму этапу реализации проекта"
subtitle: "Персональный сайт научного работкника"
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

Добавить к сайту данные о себе.

# Задание

Добавить к сайту данные о себе.

Список добавляемых данных.

Разместить фотографию владельца сайта.

Разместить краткое описание владельца сайта (Biography).

Добавить информацию об интересах (Interests).

Добавить информацию от образовании (Education).

Сделать пост по прошедшей неделе.

Добавить пост на тему по выбору:

Управление версиями. Git.

Непрерывная интеграция и непрерывное развертывание (CI/CD).


# Выполнение

1. Добавляем фотографию и дополняем биографию (рис. [-@fig:001])

![Редактируем](image/1.png){#fig:001 width=70%}

2. Пишем пост по прошедшей неделе и пост на тему по выбору (рис. [-@fig:002])

![Пишем посты](image/2.png){#fig:002 width=70%}

3. Размещаем на сайте обновленную информацию и посты (рис. [-@fig:003])

![Новая информация на нашем сайте](image/3.png){#fig:003 width=70%}

4. Загружаем файлы на github (рис. [-@fig:004])

![Загрузка файлов](image/4.png){#fig:004 width=70%}

5. Наблюдаем итог работы (рис. [-@fig:005])

![Мой персональный сайт](image/5.png){#fig:005 width=70%}

# Выводы

Мы научились добавлять к сайту информацию о себе и писать посты.

