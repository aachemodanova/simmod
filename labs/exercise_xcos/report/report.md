---
## Front matter
title: "Выполнение упражнения"
subtitle: "Построение с помощью xcos фигуры Лиссажу с различными значениями параметров"
author: "Чемоданова Ангелина Александровна"

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
lot: false # List of tables
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

Выполнить упражнение по построению фигуры Лиссажу с помощью программы *xcos*.

# Задание

Постройте с помощью xcos фигуры Лиссажу со следующими параметрами:

1) $A = B = 1, a = 2, b = 2, \, \delta = 0; \, \pi/4; \, \pi/2; \,  3\pi/4;\,  \pi;$

2) $A = B = 1, a = 2, b = 4, \, \delta = 0; \, \pi/4; \, \pi/2; \, 3\pi/4; \, \pi;$

3) $A = B = 1, a = 2, b = 6, \, \delta = 0; \, \pi/4; \, \pi/2; \, 3π/4; \, π;$

4) $A = B = 1, a = 2, b = 3, \, \delta = 0; \, \pi/4; \, \pi/2; \, 3\pi/4; \, \pi.$


# Выполнение лабораторной работы

## Математическая модель

Математическое выражение для кривой Лиссажу:
$$
\begin{cases}
  x(t) = A * sin(a * t + \delta),\\
  y(t) = B * sin(b * t),
\end{cases}
$$
где $A, B$ -- амплитуды колебаний, $a, b$ -- частоты, $\delta$ -- сдвиг фаз.

## Реализация модели в xcos

В модели, изображённой на рис. [-@fig:001], использованы следующие блоки xcos:
- CLOCK_c -- запуск часов модельного времени;
- GENSIN_f -- блок генератора синусоидального сигнала;
- CSOPXY -- анимированное регистрирующее устройство для построения графика типа y = f(x);
- TEXT_f -- задаёт текст примечаний.

![Модель для построения фигуры Лиссажу в xcos](image/1.png){#fig:001 width=70%}

Настроим параметры регистрирующего устройства.  (рис. [-@fig:002]).

![Ввод параметров для регистрирующего устройства](image/2.png){#fig:002 width=70%}

Настроим параметры генераторов синусоидального сигнала. (рис. [-@fig:003]).

![Ввод параметров для генераторов синусоидального сигнала](image/3.png){#fig:003 width=70%}

## Построение фигуры Лиссажу при параметрах: $A = B = 1, a = 2, b = 2$

Перейдем к построению. Получим график фигуры Лиссажу при параметрах: $A = B = 1, a = 2, b = 2, \delta = 0$ (рис. [-@fig:004]). 

![Фигура Лиссажу: $A = B = 1, a = 2, b = 2, \delta = 0$](image/4.png){#fig:004 width=70%}

Изменим фазу в первом генераторе на $\pi/4; \, \pi/2; \,  3\pi/4;\,  \pi;$ получим соответственно другие фигуры Лиссажу (рис. [-@fig:005]-[-@fig:008]).

![Фигура Лиссажу: $A = B = 1, a = 2, b = 2, \delta = \pi /4$](image/5.png){#fig:005 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 2, \delta = \pi /2$](image/6.png){#fig:006 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 2, \delta = 3\pi /4$](image/7.png){#fig:007 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 2, \delta = \pi$](image/8.png){#fig:008 width=70%}

## Построение фигуры Лиссажу при параметрах: $A = B = 1, a = 2, b = 4$

Изменим частоту на 4(рад/c) на втором генераторе синусоидального сигнала.  (рис. [-@fig:009]).

![Изменение параметров для второго генератора синусоидального сигнала](image/9.png){#fig:009 width=70%}

Перейдем к построению. Получим график фигуры Лиссажу при параметрах: $A = B = 1, a = 2, b = 4, \delta = 0$ (рис. [-@fig:010]). 

![Фигура Лиссажу: $A = B = 1, a = 2, b = 4, \delta = 0$](image/10.png){#fig:010 width=70%}

Изменим фазу в первом генераторе на $\pi/4; \, \pi/2; \,  3\pi/4;\,  \pi;$ получим соответственно другие фигуры Лиссажу (рис. [-@fig:011]-[-@fig:014]).

![Фигура Лиссажу: $A = B = 1, a = 2, b = 4, \delta = \pi /4$](image/11.png){#fig:011 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 4, \delta = \pi /2$](image/12.png){#fig:012 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 4, \delta = 3\pi /4$](image/13.png){#fig:013 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 4, \delta = \pi$](image/14.png){#fig:014 width=70%}

## Построение фигуры Лиссажу при параметрах: $A = B = 1, a = 2, b = 6$

Изменим частоту на 6(рад/c) на втором генераторе синусоидального сигнала.  (рис. [-@fig:015]).

![Изменение параметров для второго генератора синусоидального сигнала](image/15.png){#fig:015 width=70%}

Перейдем к построению. Получим график фигуры Лиссажу при параметрах: $A = B = 1, a = 2, b = 6, \delta = 0$ (рис. [-@fig:016]). 

![Фигура Лиссажу: $A = B = 1, a = 2, b = 6, \delta = 0$](image/16.png){#fig:016 width=70%}

Изменим фазу в первом генераторе на $\pi/4; \, \pi/2; \,  3\pi/4;\,  \pi;$ получим соответственно другие фигуры Лиссажу (рис. [-@fig:017]-[-@fig:020]).

![Фигура Лиссажу: $A = B = 1, a = 2, b = 6, \delta = \pi /4$](image/17.png){#fig:017 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 6, \delta = \pi /2$](image/18.png){#fig:018 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 6, \delta = 3\pi /4$](image/19.png){#fig:019 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 6, \delta = \pi$](image/20.png){#fig:020 width=70%}

## Построение фигуры Лиссажу при параметрах: $A = B = 1, a = 2, b = 3$

Изменим частоту на 3(рад/c) на втором генераторе синусоидального сигнала.  (рис. [-@fig:021]).

![Изменение параметров для второго генератора синусоидального сигнала](image/21.png){#fig:021 width=70%}

Перейдем к построению. Получим график фигуры Лиссажу при параметрах: $A = B = 1, a = 2, b = 3, \delta = 0$ (рис. [-@fig:022]). 

![Фигура Лиссажу: $A = B = 1, a = 2, b = 3, \delta = 0$](image/22.png){#fig:022 width=70%}

Изменим фазу в первом генераторе на $\pi/4; \, \pi/2; \,  3\pi/4;\,  \pi;$ получим соответственно другие фигуры Лиссажу (рис. [-@fig:023]-[-@fig:026]).

![Фигура Лиссажу: $A = B = 1, a = 2, b = 3, \delta = \pi /4$](image/23.png){#fig:023 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 3, \delta = \pi /2$](image/24.png){#fig:024 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 3, \delta = 3\pi /4$](image/25.png){#fig:025 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 3, \delta = \pi$](image/26.png){#fig:026 width=70%}

# Выводы

Мы выполнили упражнение по построению фигуры Лиссажу с помощью программы *xcos*.

# Список литературы{.unnumbered}

::: {#refs}
:::
