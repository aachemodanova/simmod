---
## Front matter
lang: ru-RU
title: Лабораторная работа №9
subtitle: "Модель «Накорми студентов»"
author:
  - Чемоданова Ангелина Александровна
teacher:
  - Кулябов Д. С.
  - д.ф.-м.н., профессор
  - профессор кафедры теории вероятностей и кибербезопасности 
institute:
  - Российский университет дружбы народов имени Патриса Лумумбы, Москва, Россия
date: 20 марта 2025

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

## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

  * Чемоданова Ангелина Александровна
  * Cтудентка НФИбд-02-22
  * Российский университет дружбы народов имени Патриса Лумумбы
  * [1132226443@pfur.ru](mailto:1132226443@pfur.ru)
  * <https://github.com/aachemodanova>

:::
::: {.column width="30%"}

![](./image/angelina_1.jpg)

:::
::::::::::::::

## Цель работы

Исследовать модель «Накорми студентов» с помощью программы *CPN Tools*.

## Задание

- реализовать модель «Накорми студентов» в *CPN Tools*;
- вычислить пространство состояний, сформировать отчет о нем и построить граф.


# Выполнение лабораторной работы.

## Реализация модели в *CPN Tools*

Рассмотрим пример студентов, обедающих пирогами. Голодный студент становится сытым после того, как съедает пирог.

Таким образом, имеем:

- два типа фишек: «пироги» и «студенты»;

- три позиции: «голодный студент», «пирожки», «сытый студент»;

- один переход: «съесть пирожок».

## Реализация модели в *CPN Tools*

![Граф сети модели «Накорми студентов»](image/1_1.png){#fig:001 width=50%}

## Реализация модели в *CPN Tools*

![Декларации модели «Накорми студентов»](image/2_1.png){#fig:002 width=50%}

## Реализация модели в *CPN Tools*

![Модель «Накорми студентов»](image/3_1.png){#fig:003 width=50%}

## Реализация модели в *CPN Tools*

![Запуск модели «Накорми студентов»](image/4_1.png){#fig:004 width=50%}

## Упражнение

![Граф пространства состояний](image/5_1.png){#fig:005 width=70%}

## Упражнение

```
CPN Tools state space report for:
/home/openmodelica/Desktop/lab9.cpn
Report generated: Thu Mar 20 20:54:00 2025


 Statistics
------------------------------------------------------------------------
```
## Упражнение
```
  State Space
     Nodes:  4
     Arcs:   3
     Secs:   0
     Status: Full

  Scc Graph
     Nodes:  4
     Arcs:   3
     Secs:   0
```
## Упражнение
```
 Boundedness Properties
------------------------------------------------------------------------

  Best Integer Bounds
                             Upper      Lower
     nakormi_studenta'food 1 5          2
     nakormi_studenta'hungry_student 1
                             3          0
     nakormi_studenta'satisfied_student 1
                             3          0
```
## Упражнение
```
  Best Upper Multi-set Bounds
     nakormi_studenta'food 1
                         5`pasty
     nakormi_studenta'hungry_student 1
                         3`student
     nakormi_studenta'satisfied_student 1
                         3`student
```
## Упражнение                         
```
  Best Lower Multi-set Bounds
     nakormi_studenta'food 1
                         2`pasty
     nakormi_studenta'hungry_student 1
                         empty
     nakormi_studenta'satisfied_student 1
                         empty
```
## Упражнение
```
 Home Properties
------------------------------------------------------------------------

  Home Markings
     [4]


 Liveness Properties
------------------------------------------------------------------------

  Dead Markings
     [4]
```
## Упражнение
```
  Dead Transition Instances
     None

  Live Transition Instances
     None


 Fairness Properties
------------------------------------------------------------------------
     No infinite occurrence sequences.
```

## Выводы

Мы исследовали модель «Накорми студентов» с помощью программы *CPN Tools*.
