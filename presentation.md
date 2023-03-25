---
## Front matter
title: "Отчёт по лабораторной работе №7"
subtitle: "Математическое моделирование"
author: "Новосельцев Данила Сергеевич"

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
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
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

## Цель работы

---

Познакомиться с простейшей моделью рекламной кампании
Визуализировать модель с помощью Julia
Задание
1. Построить графики распространения рекламы
2. Рассмотреть три случая: где a1 << a2, где а1 >> a2 и где a1 и a2 --- периодические функции
3. Для второго случая найти момент времени, в который скорость распространения рекламы принимает максимальное значение

---

## Теоретическое введение

---

Организуется рекламная кампания нового товара или услуги. Необходимо, чтобы прибыль будущих продаж с избытком покрывала издержки на рекламу. Вначале расходы могут превышать прибыль, поскольку лишь малая часть потенциальных покупателей будет информирована о новинке. Затем, при увеличении числа продаж, возрастает и прибыль, и, наконец, наступит момент, когда рынок насытится, и рекламировать товар станет бесполезным.

Предположим, что торговыми учреждениями реализуется некоторая продукция, о которой в момент времени t из числа потенциальных покупателей N знает лишь n покупателей. Для ускорения сбыта продукции запускается реклама по радио, телевидению и других средств массовой информации. После запуска рекламной кампании информация о продукции начнет распространяться среди потенциальных покупателей путем общения друг с другом. Таким образом, после запуска рекламных объявлений скорость изменения числа знающих о продукции людей пропорциональна как числу знающих о товаре покупателей, так и числу покупателей, о нем не знающих.

---

## Выполнение лабораторной работы

---

![Первый пункт](lab7_1.png)

---

![Второй пункт](lab7_2.png)

---

![Третий пункт](lab7_3.png)

---

## Выводы

---

В ходе работы мы изучили модель рекламной кампании и применили навыки работы с Julia для построения графиков, визуализирующих эту модель. Результатом работы стали графики распространения рекламы для трех случаев. Мы увидели, что в первом случае численность осведомленных клиентов изменяется плавно, так как a1 >> a2, а для второго и третьего случаев численность осведомленных клиентов растет стремительно за короткие сроки, и график принимает вид логистической кривой, так как a1 << a2. Также для второго случая мы нашли момент времени, в который скорость распространения рекламы максимальна.
