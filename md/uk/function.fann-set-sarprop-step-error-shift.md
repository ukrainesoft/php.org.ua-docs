---
navigation:
  - function.fann-set-rprop-increase-factor.html: « fannsetrpropincreasefactor
  - function.fann-set-sarprop-step-error-threshold-factor.html: fannsetsarpropsteperrorthresholdfactor »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
title: fannsetsarpropsteperrorshift
---
# fannsetsarpropsteperrorshift

(PECL fann> = 1.0.0)

fannsetsarpropsteperrorshift - Встановлює зрушення помилки кроку sarprop

### Опис

```methodsynopsis
fann_set_sarprop_step_error_shift(resource $ann, float $sarprop_step_error_shift): bool
```

Встановлює зрушення помилки кроку sarprop.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`sarprop_step_error_shift`

Зрушення помилки кроку sarprop.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Примітки

> **Зауваження**
> 
> Функція доступна лише у випадку, якщо модуль fann був зібраний для libfann >= 2.2.

### Дивіться також

-   [fanngetsarpropsteperrorshift()](function.fann-get-sarprop-step-error-shift.html) - Повертає зрушення помилки кроку sarprop
