---
## Front matter
title: "Отчет по Лабораторной работе №6"
subtitle: "Отчет"
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

Приобретение практических навыков взаимодействия пользователя с системой посредством командной строки.

# Выполнение лабораторной работы

1. Определите полное имя вашего домашнего каталога. Далее относительно этого каталога будут выполняться последующие упражнения.
Выполните следующие действия:
Перейдите в каталог /tmp.
Выведите на экран содержимое каталога /tmp. Для этого используйте команду ls
с различными опциями (рис. [-@fig:001])

![Выполняем команды pwd, cd, ls](image/1.png){#fig:001 width=70%}

2. Определите, есть ли в каталоге /var/spool подкаталог с именем cron? (рис. [-@fig:002])

![Подкаталог с именем cron](image/2.png){#fig:002 width=70%}

3. Выполните следующие действия:
В домашнем каталоге создайте новый каталог с именем newdir.
В каталоге ~/newdir создайте новый каталог с именем morefun.
В домашнем каталоге создайте одной командой три новых каталога с именами letters, memos, misk. Затем удалите эти каталоги одной командой.
Попробуйте удалить ранее созданный каталог ~/newdir командой rm. Проверьте, был ли каталог удалён.
Удалите каталог ~/newdir/morefun из домашнего каталога. Проверьте, был ли каталог удалён (рис. [-@fig:003])

![Выполняем команды](image/3.png){#fig:003 width=70%}

4. С помощью команды man определите, какую опцию команды ls нужно использовать для просмотра содержимое не только указанного каталога, но и подкаталогов, входящих в него (рис. [-@fig:004])

![Используем команду -tl](image/4.png){#fig:004 width=70%}

5. Используйте команду man для просмотра описания следующих команд: cd, pwd, mkdir, rmdir, rm (рис. [-@fig:005])

![Используем команду man](image/5.png){#fig:005 width=70%}

6. Используя информацию, полученную при помощи команды history, выполните модификацию и исполнение нескольких команд из буфера команд (рис. [-@fig:006])

![Выполняем модификацию команд](image/6.png){#fig:006 width=70%}

# Ответы на контрольные вопросы

1. Интерфейс для взаимодействия с ОС через текстовые команды.
2. pwd пример: pekichigina/home/
3. ls -l 
4. ls -a
5. rm для файла, rmdir для каталога. Одной командой нельзя.
6. С помощью команды history.
7. !номер_команды/старая/новая пример: !50:s/-l/-a
8. ls; pwd
9. Это отмена специального значения символа. Пример: echo "hello\"world\""
10. Подробная информация.
11. Это путь относительно текущего каталога. 
12. С помощью команды man
13. Tab


# Выводы

Мы приобрели практические навыки взаимодействия пользователя с системой посредством командной строки.


