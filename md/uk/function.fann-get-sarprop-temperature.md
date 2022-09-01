---
navigation:
  - function.fann-get-sarprop-step-error-threshold-factor.html: « fanngetsarpropsteperrorthresholdfactor
  - function.fann-get-sarprop-weight-decay-shift.html: fanngetsarpropweightdecayshift »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
title: fanngetsarproptemperature
---
# fanngetsarproptemperature

(PECL fann> = 1.0.0)

fanngetsarproptemperature - Повертає температуру sarprop

### Опис

```methodsynopsis
fann_get_sarprop_temperature(resource $ann): float
```

Повертає температуру сарprop.

Температура за промовчанням становить 0.015.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Температура sarprop або **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fannsetsarproptemperature()](function.fann-set-sarprop-temperature.html) - Встановлює температуру sarprop
