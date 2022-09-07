---
navigation:
  - function.fann-set-sarprop-step-error-threshold-factor.md: « fannsetsarpropsteperrorthresholdfactor
  - function.fann-set-sarprop-weight-decay-shift.md: fannsetsarpropweightdecayshift »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannsetsarproptemperature
---
# fannsetsarproptemperature

(PECL fann> = 1.0.0)

fannsetsarproptemperature - Встановлює температуру sarprop

### Опис

```methodsynopsis
fann_set_sarprop_temperature(resource $ann, float $sarprop_temperature): bool
```

Встановлює температуру sarprop.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`sarprop_temperature`

Температура сарprop.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Примітки

> **Зауваження**
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fanngetsarproptemperature()](function.fann-get-sarprop-temperature.md) - Повертає температуру sarprop
