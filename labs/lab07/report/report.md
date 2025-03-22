---
## Front matter
title: "Отчет по Лабораторной Работе №7"
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

Ознакомление с файловой системой Linux, её структурой, именами и содержанием каталогов. Приобретение практических навыков по применению команд для работы с файлами и каталогами, по управлению процессами (и работами), по проверке использования диска и обслуживанию файловой системы.


# Выполнение лабораторной работы

1. Выполните все примеры, приведённые в первой части описания лабораторной работы (рис. [-@fig:001])

![Выполняем примеры](image/1.png){#fig:001 width=70%}

2. Выполните следующие действия, зафиксировав в отчёте по лабораторной работе
используемые при этом команды и результаты их выполнения:

 Скопируйте файл /usr/include/sys/io.h в домашний каталог и назовите его
equipment. Если файла io.h нет, то используйте любой другой файл в каталоге
/usr/include/sys/ вместо него.

В домашнем каталоге создайте директорию ~/ski.plases.
 
Переместите файл equipment в каталог ~/ski.plases.
 
Переименуйте файл ~/ski.plases/equipment в ~/ski.plases/equiplist.

Создайте в домашнем каталоге файл abc1 и скопируйте его в каталог
~/ski.plases, назовите его equiplist2.

Создайте каталог с именем equipment в каталоге ~/ski.plases.

Переместите файлы ~/ski.plases/equiplist и equiplist2 в каталог
~/ski.plases/equipment.

Создайте и переместите каталог ~/newdir в каталог ~/ski.plases и назовите
его plans (рис. [-@fig:002])

![Выполняем](image/2.png){#fig:002 width=70%}

3. Определите опции команды chmod, необходимые для того, чтобы присвоить перечис-
ленным ниже файлам выделенные права доступа, считая, что в начале таких прав
нет:

drwxr--r-- ... australia

drwx--x--x ... play

-r-xr--r-- ... my_os

3-rw-rw-r-- ... feathers

При необходимости создайте нужные файлы (рис. [-@fig:003])

![Определяем опции команды chmod](image/3.png){#fig:003 width=70%}

4. Проделайте приведённые ниже упражнения, записывая в отчёт по лабораторной
работе используемые при этом команды:

Просмотрите содержимое файла /etc/password.

Скопируйте файл ~/feathers в файл ~/file.old.

Переместите файл ~/file.old в каталог ~/play.

Скопируйте каталог ~/play в каталог ~/fun.

Переместите каталог ~/fun в каталог ~/play и назовите его games.

Лишите владельца файла ~/feathers права на чтение.

Что произойдёт, если вы попытаетесь просмотреть файл ~/feathers командой
cat?

Что произойдёт, если вы попытаетесь скопировать файл ~/feathers?

Дайте владельцу файла ~/feathers право на чтение.

Лишите владельца каталога ~/play права на выполнение.

Перейдите в каталог ~/play. Что произошло?

Дайте владельцу каталога ~/play право на выполнение (рис. [-@fig:004])

![Выполняем](image/4.png){#fig:004 width=70%}

5. Прочитайте man по командам mount, fsck, mkfs, kill и кратко их охарактеризуйте,
приведя примеры (рис. [-@fig:005])

![Применяем man для характеристики](image/5.png){#fig:005 width=70%}

# Выводы

Мы ознакомились с файловой системой Linux, её структурой, именами и содержанием каталогов. Приобрели практические навыки по применению команд для работы с файлами и каталогами, по управлению процессами (и работами), по проверке использования диска и обслуживанию файловой системы.

# Ответы на контрольные вопросы 

1. Файловые системы: Каждая ФС характеризуется типом (ext4, NTFS, swap), структурой, организацией данных, журналированием. Ext4 - для Linux, NTFS - для Windows, swap - для подкачки памяти. Различаются по надежности, производительности, размеру блока.

2. Структура ФС (FHS): Иерархия, начинающаяся с корня (/). /bin - базовые команды, /boot - загрузчик, /dev - устройства, /etc - конфиги, /home - пользовательские каталоги, /lib - библиотеки, /media, /mnt - точки монтирования, /proc - информация о процессах, /tmp - временные файлы, /usr - пользовательские программы, /var - переменные данные.

3. Доступ к ФС: ФС нужно смонтировать (mount) к точке монтирования, чтобы ОС могла ее видеть и использовать.

4. Нарушение целостности: Внезапное отключение питания, аппаратные сбои, программные ошибки приводят к повреждениям. Устранение: fsck проверяет и пытается исправить ошибки после отмонтирования.

5. Создание ФС: Команда mkfs.тип_фс /dev/раздел (например, mkfs.ext4 /dev/sda1) создаёт новую ФС на разделе (осторожно, стирает данные!).

6. Просмотр текста: cat выводит файл целиком, less - постранично (навигация, поиск), head и tail - начало и конец файла соответственно. tail -f - мониторинг изменений в реальном времени.

7. cp: Копирует файлы и каталоги (рекурсивно -r), сохраняя атрибуты (-p), создает символические ссылки (-s), а не копии.

8. mv: Перемещает или переименовывает файлы и каталоги.

9. Права доступа: Указывают, кто (владелец, группа, остальные) может что делать (читать, писать, выполнять) с файлом/каталогом (rwx). Изменяются командой chmod, численно или символически.
