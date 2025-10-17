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

Получить навыки работы с журналами мониторинга различных событий в системе.

# Задание

1. Продемонстрируйте навыки работы с журналом мониторинга событий в реальном
времени.
2. Продемонстрируйте навыки создания и настройки отдельного файла конфигурации
мониторинга отслеживания событий веб-службы.
3. Продемонстрируйте навыки работы с journalctl.
4. Продемонстрируйте навыки работы с journald.


# Выполнение лабораторной работы

1. Мониторинг журнала системных событий в реальном времени.

Запустите три вкладки терминала и в каждом из них получите полномочия админи-
стратора.
На второй вкладке терминала запустите мониторинг системных событий в реальном
времени. В третьей вкладке терминала вернитесь к учётной записи своего пользователя (до-
статочно нажать Ctrl + d ) и попробуйте получить полномочия администратора, но
введите неправильный пароль. Обратите внимание, что во второй вкладке терминала
с мониторингом событий или ничего не отобразится, или появится сообщение «FAILED
SU (to root) username ...». Отображаемые на экране сообщения также фиксируются
в файле /var/log/messages.
В третьей вкладке терминала из оболочки пользователя введите
logger hello
Во второй вкладке терминала с мониторингом событий вы увидите сообщение, кото-
рое также будет зафиксировано в файле /var/log/messages.
Во второй вкладке терминала с мониторингом остановите трассировку файла со-
общений мониторинга реального времени, используя Ctrl + c . Затем запустите
мониторинг сообщений безопасности (последние 20 строк соответствующего файла
логов).
Вы увидите сообщения, которые ранее были зафиксированы во время ошибки авто-
ризации при вводе команды su. (рис. [-@fig:001])

![Выполняем команды](image/1.png){#fig:001 width=70%}

2. Изменение правил rsyslog.conf.

По умолчанию веб-служба не регистрирует свои сообщения через rsyslog, а пишет
свой собственный журнал (в каталоге /var/log/httpd). Настройте регистрацию сообще-
ний веб-службы через syslog, создав правило, регистрирующее отладочные сообщения
в отдельном лог-файле. (рис. [-@fig:002])

![Настраиваем регистрацию](image/2.png){#fig:002 width=70%}

В третьей вкладке терминала создайте отдельный файл конфигурации для монито-
ринга отладочной информации. (рис. [-@fig:003])

![Создаем файл](image/3.png){#fig:003 width=70%}

3. Использование journalctl

Во второй вкладке терминала посмотрите содержимое журнала с событиями с момента
последнего запуска системы:
journalctl
Для пролистывания журнала используйте или Enter (построчный просмотр), или про-
бел (постраничный просмотр). Для выхода из просмотра используйте q .
Для просмотра дополнительной информации о модуле sshd введите
journalctl _SYSTEMD_UNIT=sshd.service (рис. [-@fig:004])

![Просматриваем журнал](image/4.png){#fig:004 width=70%}

4. Постоянный журнал journald.

По умолчанию журнал journald хранит сообщения в оперативной памяти системы
и записи доступны в каталоге /run/log/journal только до перезагрузки системы. Для
того чтобы сделать журнал journald постоянным, выполните следующие действия.
Запустите терминал и получите полномочия администратора.
Создайте каталог для хранения записей журнала. Скорректируйте права доступа для каталога /var/log/journal, чтобы journald смог
записывать в него информацию:
chown root:systemd-journal /var/log/journal
chmod 2755 /var/log/journal

Для принятия изменений необходимо или перезагрузить систему (перезапустить
службу systemd-journald недостаточно), или использовать команду:
killall -USR1 systemd-journald(рис. [-@fig:005])

![Делаем журнал постоянным](image/5.png){#fig:005 width=70%}

# Выводы

Мы получили навыки работы с журналами мониторинга различных событий в системе.

