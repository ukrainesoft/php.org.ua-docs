---
navigation:
  - function.fann-set-sarprop-temperature.md: « fannsetsarproptemperature
  - function.fann-set-scaling-params.md: fannsetscalingparams »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannsetsarpropweightdecayshift
---
# fannsetsarpropweightdecayshift

(PECL fann> = 1.0.0)

fannsetsarpropweightdecayshift - Встановлює зміщення згасання sarprop

### Опис

```methodsynopsis
fann_set_sarprop_weight_decay_shift(resource $ann, float $sarprop_weight_decay_shift): bool
```

Встановлює зміщення загасання sarprop.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`sarprop_weight_decay_shift`

Зміщення загасання sarprop.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Примітки

> **Зауваження**
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fanngetsarpropweightdecayshift()](function.fann-get-sarprop-weight-decay-shift.md) - Повертає зсув зменшення ваги sarprop
