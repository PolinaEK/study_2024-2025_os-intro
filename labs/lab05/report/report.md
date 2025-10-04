---
## Front matter
title: "Отчёт по лабораторной работе №5"
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

Получить навыки управления системными службами операционной системы посред-
ством systemd.

# Задание
1. Выполните основные операции по запуску (останову), определению статуса, добавле-
нию (удалению) в автозапуск и пр. службы Very Secure FTP.
2. Продемонстрируйте навыки по разрешению конфликтов юнитов для служб
firewalld и iptables.
3. Продемонстрируйте навыки работы с изолированными целями.

# Выполнение лабораторной работы

1. Управление сервисами
 Получите полномочия администратора. Проверьте статус службы Very Secure FTP.
Вывод команды должен показать, что сервис в настоящее время отключён, так как
служба Very Secure FTP не установлена.
Установите службу Very Secure FTP: (рис. [-@fig:001])

![Устанавливаем](image/1.png){#fig:001 width=70%}

Запустите службу Very Secure FTP. Проверьте статус службы Very Secure FTP.
Вывод команды должен показать, что служба в настоящее время работает, но не будет
активирована при перезапуске операционной системы.
Добавьте службу Very Secure FTP в автозапуск при загрузке операционной системы, ис-
пользуя команду systemctl enable. Затем проверьте статус службы. Удалите службу
из автозапуска, используя команду systemctl disable, и снова проверьте её статус.
Выведите на экран символические ссылки, ответственные за запуск различных серви-
сов (рис. [-@fig:002])

![Выводим ссылки](image/2.png){#fig:002 width=70%}

2. Конфликты юнитов
Получите полномочия администратора. Установите iptables. Проверьте статус firewalld и iptables.
 Попробуйте запустить firewalld и iptables.
 Выгрузите службу iptables (на всякий случай, чтобы убедиться, что данная служба
не загружена в систему).
Заблокируйте запуск iptables.
 Попробуйте запустить iptables:
 Попробуйте добавить iptables в автозапуск: (рис. [-@fig:003])

![Добавляем в автозапуск](image/3.png){#fig:003 width=70%}

3. Изолируемые цели
 Получите полномочия администратора. Перейдите в каталог systemd и найдите спи-
сок всех целей, которые можно изолировать (рис. [-@fig:004])

![Список целей](image/4.png){#fig:004 width=70%}

4. Цель по умолчанию
Получите полномочия администратора. Выведите на экран цель, установленную по
умолчанию. 
Перегрузите систему командой reboot. Убедитесь, что система загрузилась в тек-
стовом режиме. Получите полномочия администратора. Для запуска по умолчанию
графического режима.
Вновь перегрузите систему командой reboot. Убедитесь, что система загрузилась
в графическом режиме. (рис. [-@fig:005])

![Выполняем команды](image/5.png){#fig:005 width=70%}



# Выводы

Мы получили навыки управления системными службами операционной системы посред-
ством systemd.
