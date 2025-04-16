---
## Front matter
title: "Отчёт по лабораторной работе №10"
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

Познакомиться с операционной системой Linux. Получить практические навыки работы с редактором vi, установленным по умолчанию практически во всех дистрибутивах.


# Выполнение лабораторной работы. Задание 1

1. Создайте каталог с именем ~/work/os/lab06.

2. Перейдите во вновь созданный каталог.

3. Вызовите vi и создайте файл hello.sh(рис. [-@fig:001])

![Вызываем vi](image/1.png){#fig:001 width=70%}

4. Нажмите клавишу i и вводите следующий текст.

5. Нажмите клавишу Esc для перехода в командный режим после завершения ввода
текста.

6. Нажмите : для перехода в режим последней строки и внизу вашего экрана появится
приглашение в виде двоеточия.

7. Нажмите w (записать) и q (выйти), а затем нажмите клавишу Enter для сохранения
вашего текста и завершения работы.

8. Сделайте файл исполняемым (рис. [-@fig:002]).

![Проделываем все команды](image/2.png){#fig:002 width=70%}

# Задание 2

1. Вызовите vi на редактирование файла
1 vi ~/work/os/lab06/hello.sh

2. Установите курсор в конец слова HELL второй строки.

3. Перейдите в режим вставки и замените на HELLO. Нажмите Esc для возврата в команд-
ный режим.

4. Установите курсор на четвертую строку и сотрите слово LOCAL.

5. Перейдите в режим вставки и наберите следующий текст: local, нажмите Esc для
возврата в командный режим.

6. Установите курсор на последней строке файла. Вставьте после неё строку, содержащую
следующий текст: echo $HELLO.

7. Нажмите Esc для перехода в командный режим.

8. Удалите последнюю строку.

9. Введите команду отмены изменений u для отмены последней команды.

10. Введите символ : для перехода в режим последней строки. Запишите произведённые
изменения и выйдите из vi.(рис. [-@fig:003])

![Проделываем все команды](image/3.png){#fig:003 width=70%}

# Ответы на контрольные вопросы

1. Режимы vi: Командный (выполнение команд), Вставки (ввод текста), Последней строки (команды с “:”).

2. Выход без сохранения: :q!

3. Команды позиционирования:

h, j, k, l: влево, вниз, вверх, вправо.

w, b: следующее/предыдущее слово.

^, $: начало/конец строки.

gg, G: начало/конец файла.

4. Слово в vi: Последовательность символов, разделенная пробелами или знаками пунктуации.

5. В начало/конец файла: gg, G

6. Команды редактирования:


Вставки (i, a, o).

Удаления (x, dd, dw).

Изменения (r, c).

Копирования/вставки (yy, p).

7. Заполнить строку “$”: Перейдите в конец строки ($), затем A и многократно введите $ или используйте команду :s/./$/g в режиме последней строки

8. Отмена действия: u (undo)

9. Команды последней строки:

:w: запись в файл.

:q: выход.

:s: замена.

:set: установка опций.

10. Определение конца строки без перемещения: Визуально (отображение строки на экране). Можно использовать команду :set list для отображения специальных символов, включая $ в конце строки.

11. Анализ опций: Много; :set all - список всех, :help option-name - помощь по конкретной опции.

12. Определение режима: Визуально (по поведению редактора). Нет явного индикатора.

13. Граф режимов:

[Командный] --i, a, o-->[Вставки] 

[Командный] --: --> [Последней строки]

[Последней строки] --Enter--> [Командный] 

[Вставки] --Esc--> [Командный]

# Выводы

Мы познакомились с операционной системой Linux. Получили практические навыки работы с редактором vi, установленным по умолчанию практически во всех дистрибутивах.
