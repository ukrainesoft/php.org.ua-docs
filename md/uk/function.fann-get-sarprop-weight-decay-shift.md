---
navigation:
  - function.fann-get-sarprop-temperature.html: « fanngetsarproptemperature
  - function.fann-get-total-connections.html: fanngettotalconnections »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanngetsarpropweightdecayshift
---
# fanngetsarpropweightdecayshift

(PECL fann> = 1.0.0)

fanngetsarpropweightdecayshift — Повертає зменшення ваги sarprop

### Опис

```methodsynopsis
fann_get_sarprop_weight_decay_shift(resource $ann): float
```

Повертає зсув зменшення ваги sarprop.

Максимальна дельта за промовчанням становить -6.644.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Зсув зменшення ваги sarprop або **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fannsetsarpropweightdecayshift()](function.fann-set-sarprop-weight-decay-shift.html) - Встановлює зміщення згасання sarprop
