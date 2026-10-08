---
## Front matter
lang: ru-RU
title: Четвертый этап реализации проекта
subtitle: Тестирование веб приложений
author:
  - Кичигина Полина Евгеньевна
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 2 мая 2026

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
---

## Цель работы

Получить навыки работы в nikto.



## Выполнение 

nikto — базовый сканер безопасности веб-сервера. Он сканирует и обнаруживает уязвимости в веб-приложениях, обычно вызванные неправильной конфигурацией на самом сервере, файлами, установленными по умолчанию, и небезопасными файлами, а также устаревшими серверными приложениями.

##

Nikto просканирует сайт и напишет список уязвимостей, ошибок конфигурации и опасных файлов. 

![Разведка с nikto](image/1.png){#fig:001 width=70%}

##
     
Получаем куки для sqlmap. Sqlmap найдет все базы данных на сервере. 

![Запускаем sqlmap](image/2.png){#fig:002 width=70%}

##

Теперь вытащим все пароли пользователей. 

![выполняем команду](image/3.png){#fig:003 width=70%}

##

Получаем таблицу с логинами и хэшами паролей. 

![Смотрим таблицу](image/4.png){#fig:004 width=70%}

## Выводы

Мы получили навыки работы в nikto.

