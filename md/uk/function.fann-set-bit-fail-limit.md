---
navigation:
  - function.fann-set-activation-steepness.html: « fannsetactivationsteepness
  - function.fann-set-callback.html: fannsetcallback »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannsetbitfaillimit
---
# fannsetbitfaillimit

(PECL fann> = 1.0.0)

fannsetbitfaillimit — Встановлює межу помилок, що використовується під час навчання

### Опис

```methodsynopsis
fann_set_bit_fail_limit(resource $ann, float $bit_fail_limit): bool
```

Встановлює межу помилок, яка використовується під час навчання.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`bit_fail_limit`

Межа помилок.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanngetbitfaillimit()](function.fann-get-bit-fail-limit.html) - Повертає межу збою бітів, використану під час навчання
