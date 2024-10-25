---
## Front matter
title: "Архитектура компьютеров и операционные системы | Операционные системы"
subtitle: "Лабораторная работа № 3. Markdown"
author: "Осман Алиниколай НБИбд-02-24"

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
  name: russian!
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: IBM Plex Mono
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
lotTitle: "Список таблиц "
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---



# Цель работы

## 


- Научиться оформлять отчёты с помощью легковесного языка разметки **Markdown**.

# Задание

- Сделать отчёт по предыдущей лабораторной работе в формате **Markdown**.
- В качестве отчёта нужно предоставить отчёты в **3 форматах**: **pdf**, **docx** и **md** (в **архиве**, поскольку он должен содержать **скриншоты**, **Makefile** и т.д.)

# Теоретическое введение : 








2. Переход в каталог курса

![ рисунок 1](/home/anosman/Изображения/lab03/image1.png){#fig:001 width=70%}

Эта команда запускает процесс компиляции с использованием Makefile, в результате чего будут сгенерированы файлы report.pdf и report.docx.

3. Обновление локального репозитория с помощью Git Pull

![ рисунок 2](/afs/.dk.sci.pfu.edu.ru/home/a/n/anosman/Изображения/lab03/image2.png){#fig:002 width=70%}

Эта команда загружает изменения из удаленного репозитория и синхронизирует их с локальным репозиторием.

4. Переход в каталог с шаблоном отчета для лабораторной работы №3

![ рисунок 3](/afs/.dk.sci.pfu.edu.ru/home/a/n/anosman/Изображения/lab03/image3.png){#fig:003 width=70%}

Эта команда перемещает вас в каталог, где хранится шаблон отчета для лабораторной работы №3.


5. Компиляция шаблона отчета с использованием Makefile

![ рисунок 4](/afs/.dk.sci.pfu.edu.ru/home/a/n/anosman/Изображения/lab03/image4.png){#fig:004 width=70%}

Эта команда запускает процесс компиляции с использованием Makefile, в результате чего будут сгенерированы файлы report.pdf и report.docx.


7. Удаление файлов с использованием Makefile

![ рисунок 5](/afs/.dk.sci.pfu.edu.ru/home/a/n/anosman/Изображения/lab03/image5.png){#fig:005 width=70%}

Эта команда удаляет сгенерированные файлы, такие как report.pdf и report.docx.



9. Открытие файла report.md и изучение его структуры : 

![ рисунок 6](/afs/.dk.sci.pfu.edu.ru/home/a/n/anosman/Изображения/lab03/image6.png){#fig:006 width=70%}

Эта команда открывает файл report.md в текстовом редакторе Gedit. Внимательно изучите структуру файла.

10. Загрузка файлов на GitHub

![ рисунок 7](/afs/.dk.sci.pfu.edu.ru/home/a/n/anosman/Изображения/lab03/image7.png){#fig:007 width=70%}

Эта команда отправляет ваши изменения на удаленный репозиторий на GitHub, делая их доступными другим пользователям и синхронизируя локальный репозиторий с удаленным.
