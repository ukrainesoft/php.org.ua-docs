---
navigation:
  - function.fann-get-rprop-increase-factor.md: « fanngetrpropincreasefactor
  - function.fann-get-sarprop-step-error-threshold-factor.md: fanngetsarpropsteperrorthresholdfactor »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanngetsarpropsteperrorshift
---
# fanngetsarpropsteperrorshift

(PECL fann> = 1.0.0)

fanngetsarpropsteperrorshift — Повертає помилку зрушення кроку sarprop

### Опис

```methodsynopsis
fann_get_sarprop_step_error_shift(resource $ann): float
```

Повертає зрушення помилки кроку sarprop.

Зсув помилки кроку за умовчанням становить 1385.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Зрушення помилки кроку sarprop або **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fannsetsarpropsteperrorshift()](function.fann-set-sarprop-step-error-shift.md) - Встановлює зрушення помилки кроку sarprop
