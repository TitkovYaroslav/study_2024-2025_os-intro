
---
## Front matter
title: "Лабораторная работа номер 6"
subtitle: "Основы интерфейса взаимодействия
пользователя с системой Unix на уровне командной строки"
author: "Титков Ярослав Максимович"

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
Приобретение практических навыков взаимодействия пользователя с системой по-
средством командной строки

# Задание
1. Определить полное имя  домашнего каталога. Далее относительно этого ката-
лога будут выполняться последующие упражнения.
2. Выполнить предложенные упражнения 

# Теоретическое введение
В операционной системе типа Linux взаимодействие пользователя с системой обычно
осуществляется с помощью командной строки посредством построчного ввода ко-
манд. При этом обычно используется командные интерпретаторы языка shell: /bin/sh;
/bin/csh; /bin/ksh.
Формат команды. Командой в операционной системе называется записанный по
специальным правилам текст (возможно с аргументами), представляющий собой ука-
зание на выполнение какой-либо функций (или действий) в операционной системе.
Обычно первым словом идёт имя команды, остальной текст — аргументы или опции,
конкретизирующие действие.
Общий формат команд можно представить следующим образом:
<имя_команды><разделитель><аргументы>
Команда man. Команда man используется для просмотра (оперативная помощь) в диа-
логовом режиме руководства (manual) по основным командам операционной системы
типа Linux.
Формат команды:
man <команда>
Пример (вывод информации о команде man):
man man
Для управления просмотром результата выполнения команды man можно использовать
следующие клавиши:
– Space — перемещение по документу на одну страницу вперёд;
– Enter — перемещение по документу на одну строку вперёд;
– q — выход из режима просмотра описания.
Команда cd. Команда cd используется для перемещения по файловой системе опера-
ционной системы типа Linux.
Замечание 1. Файловая система ОС типа Linux — иерархическая система каталогов,
подкаталогов и файлов, которые обычно организованы и сгруппированы по функ-
циональному признаку. Самый верхний каталог в иерархии называется корневым
и обозначается символом /. Корневой каталог содержит системные файлы и другие
каталоги.
Формат команды:
cd [путь_к_каталогу]


# Выполнение лабораторной работы

![Определение имени домашнего каталога и выполнения действий с каталогами](image/1.png){#fig:001 width=70%}

![Проверка наличия каталога cron, возвращение в домашний каталог и просмотр содержимого](image/2.png){#fig:002 width=70%}

![Работа с каталогами. Создание/Удаление](image/3.png){#fig:003 width=70%}

![Определение опции ls](image/4.png){#fig:004 width=70%}

![Описание опции](image/5.png){#fig:005 width=70%}

![Проверка опции ls для сортировки, проверка основных команд man](image/6.png){#fig:006 width=70%}

![Проверка команд man](image/7.png){#fig:007 width=70%}

![Использование команды history](image/8.png){#fig:008 width=70%}

![Замена команд](image/9.png){#fig:009 width=70%}





# Выводы
В ходе лабораторной работы, Я приобрел практические навыки взаимодействия пользователя с системой по-
средством командной строки

# Ответ на контрольные вопросы:
1. командная строка – текстовый интерфейс для управления системой
2. pwd
3. ls -F
4. ls -a
5. rm для файлов, rm -r для каталогов, можно удалить одной командой
6. history
7. !!, !n, !название_команды
8. ;, &&, || для выполнения нескольких команд
9. символы \, ', " защищают специальные символы
10. подробный список файлов с правами, владельцем, размером и датой
11. относительный путь указывает расположение от текущего каталога, абсолютный – от корня системы
12. man название_команды или --help
13. клавиша Tab

