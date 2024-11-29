---
## Front matter
title: "Oтчёт по лабораторной работе 5"
subtitle: "Структура программы на языке ассемблера NASM. Системные
вызовы в ОС GNU Linux"
author: "Осман АлиНиколай"

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

Изучить структуру программы на языке ассемблера NASM

# Задание
1. Открыть Midnight Commander
2. Создать папку lab05 и внутри нее создать файл lab5-1.asm
3. Открыть файл lab5-1.asm, ввести информацию из листинга 5.1 и сохранить
изменения
4. Убедится что файл содержит информацию
5. Оттранслировать текст файла lab5-1.asm, выполнить компановку объект-
ного файла
6. Запустить файл
7. Скачать и скопировать файл in_out.asm с помощью клавиши f5
8. С помощью клавиши f6 скопировать файл lab5-1.asm с именем lab5-2.asm
9. Исправить файл lab5-2.asm в соответствии с листингом 5.2
10. В файле lab5-2.asm заменить подпрограмму sprintLF на sprint
11. Создать исполняемый файл и проверить его работу
12. Создать копию файла lab5-1.asm и внести изменения, чтобы выводила вве-
денная строка на экран
13. Создать копию файла lab5-2.asm и внести изменения, чтобы выводила вве-
денная строка на экран

# Теоретическое введение

Здесь описываются теоретические аспекты, связанные с выполнением работы.

Например, в табл. [-@tbl:std-dir] приведено краткое описание стандартных каталогов Unix.

: Описание некоторых каталогов файловой системы GNU Linux {#tbl:std-dir}

| Имя каталога | Описание каталога                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------|
| `/`          | Корневая директория, содержащая всю файловую                                                                               |
| `/bin `      | Основные системные утилиты, необходимые как в однопользовательском режиме, так и при обычной работе всем пользователям     |
| `/etc`       | Общесистемные конфигурационные файлы и файлы конфигурации установленных программ                                           |
| `/home`      | Содержит домашние директории пользователей, которые, в свою очередь, содержат персональные настройки и данные пользователя |
| `/media`     | Точки монтирования для сменных носителей                                                                                   |
| `/root`      | Домашняя директория пользователя  `root`                                                                                   |
| `/tmp`       | Временные файлы                                                                                                            |
| `/usr`       | Вторичная иерархия для данных пользователя                                                                                 |

Более подробно про Unix см. в [@tanenbaum_book_modern-os_ru; @robbins_book_bash_en; @zarrelli_book_mastering-bash_en; @newham_book_learning-bash_en].

# Выполнение лабораторной работы

Описываются проведённые действия, в качестве иллюстрации даётся ссылка на иллюстрацию (рис. [-@fig:001]).
1. Открыть Midnight Commander 
![РИС 1](image/1.png){#fig:001 width=100%}

2. Создать папку lab05 и внутри нее создать файл lab5-1.asm 
![РИС 2](image/2.png){#fig:001 width=100%}

3. Открыть файл lab5-1.asm, ввести информацию из листинга 5.1 и сохранить
изменения 
![РИС 3](image/3.png){#fig:001 width=100%}

4.  Убедится что файл содержит информацию 
![РИС 4](image/4.png){#fig:001 width=100%}

5.  Оттранслировать текст файла lab5-1.asm, выполнить компановку объект-
ного файла (
![РИС 5](image/4.png){#fig:001 width=100%}

6. Запустить файл
![РИС 6](image/5.png){#fig:001 width=100%}

7. Скачать и скопировать файл in_out.asm с помощью клавиши f5 (
![РИС 7](image/6.png){#fig:001 width=100%}

8. С помощью клавиши f6 скопировать файл lab5-1.asm с именем lab5-2.asm
![РИС 8](image/8.png){#fig:001 width=100%}

9. Исправить файл lab5-2.asm в соответствии с листингом 5.2 и заменить
подпрограмму sprintLF на sprint 
![РИС 9](image/9.png){#fig:001 width=100%}

10. Создать исполняемый файл и проверить его работу 
![РИС 10](image/10.png){#fig:001 width=100%}

11. Создать копию файла lab5-1.asm и внести изменения, чтобы выводила введенная строка на экран
![РИС 11](image/11.png){#fig:001 width=100%}

12.  Создать копию файла lab5-2.asm и внести изменения, чтобы выводила введенная строка на экран
![РИС 12](image/12.png){#fig:001 width=100%}


![РИС 13](image/13.png){#fig:001 width=100%}

# Выводы

В процессе выполнения лабораторной работы я ознакомился со структурой
программы на языке ассемблера NASM


