---
## Front matter
title: "Лабораторная работа номер 1"
subtitle: "Выполнение лабораторной работы"
author: "Титков Ярослав Максимович"

## Generic options
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

Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

# Задание

1. Установка операционной системы.
2. Действия после установки.
3. Установка имени пользователя и названия хоста.
4. Установка программного обеспечения для создания документации.

# Теоретическое введение

Лабораторная работа подразумевает установку на виртуальную машину VirtualBox (https://www.virtualbox.org/) операционной системы Linux (дистрибутив Fedora).  
Выполнение работы возможно как в дисплейном классе факультета физико-математических и естественных наук РУДН, так и дома. Описание выполнения работы приведено для дисплейного класса со следующими характеристиками техники:  
- Intel Core i3-550 3.2 GHz, 4 GB оперативной памяти, 80 GB свободного места на жёстком диске;  
- ОС Linux Gentoo (http://www.gentoo.ru/);  
- VirtualBox версии 7.0 или новее.  

Для установки в виртуальную машину используется дистрибутив Linux Fedora (https://getfedora.org), вариант с менеджером окон sway (https://fedoraproject.org/spins/sway/).  
При выполнении лабораторной работы на своей технике вам необходимо скачать необходимый образ операционной системы (https://fedoraproject.org/spins/sway/download/index.html).  
В дисплейных классах можно воспользоваться образом в каталоге `/afs/dk.sci.pfu.edu.ru/common/files/iso`.  
Для определённости в описании будем использовать версию `Fedora-Sway-Live-x86_64-41-1.4.iso`.

# Выполнение лабораторной работы

![Установка операционной системы](image/3.png){#fig:001 width=70%}

![Обновление операционной системы](image/4.png){#fig:002 width=70%}

![Делаем систему более комфортной](image/5.png){#fig:003 width=70%}

![Снятие защиты через mc](image/6.png){#fig:004 width=70%}

![Установка dmsk](image/7.png){#fig:005 width=70%}

![Работа с ядром](image/8.png){#fig:006 width=70%}

![Установка Pandoc](image/9.png){#fig:007 width=70%}

![Проверяем установку нужных утилит для работы с файлами](image/10.png){#fig:008 width=70%}

# Выводы

В ходе выполнения лабораторной работы мы приобрели практические навыки выполнения лабораторной работы.

# Контрольные вопросы

1. **Учётная запись пользователя** содержит имя пользователя, UID, GID, домашний каталог, оболочку (shell), пароль (хранится в зашифрованном виде).

2. **Команды терминала**:  
   - Получение справки: `man команда` (пример: `man ls`).  
   - Перемещение по файловой системе: `cd путь` (пример: `cd /home/user`).  
   - Просмотр содержимого каталога: `ls` (пример: `ls -la`).  
   - Определение объёма каталога: `du -sh каталог` (пример: `du -sh /var/log`).  
   - Создание / удаление каталогов / файлов:  
     - `mkdir каталог` (пример: `mkdir test`).  
     - `rmdir каталог` (пример: `rmdir test`).  
     - `touch файл` (пример: `touch file.txt`).  
     - `rm файл` (пример: `rm file.txt`).  
   - Задание прав на файл / каталог:  
     - `chmod 755 файл` (пример: `chmod 755 script.sh`).  
     - `chown user:group файл` (пример: `chown user:user file.txt`).  
   - Просмотр истории команд: `history`.

3. **Файловая система** – способ организации, хранения и управления данными на диске. Примеры:  
   - `ext4` – стандарт для Linux, журналируемая.  
   - `XFS` – высокопроизводительная, хороша для больших файлов.  
   - `Btrfs` – поддержка снимков, дедупликация.  
   - `NTFS` – используется в Windows, поддерживается в Linux.

4. **Просмотр смонтированных файловых систем**:  
   - `mount`  
   - `df -T`  
   - `lsblk -f`

5. **Удаление зависшего процесса**:  
   - `kill PID` (пример: `kill 1234`).  
   - `kill -9 PID` (жёсткое завершение).  
   - `htop` → выбор процесса → `F9`.

::: {#refs}
:::