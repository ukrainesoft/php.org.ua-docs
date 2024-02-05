---
navigation:
  - function.fann-set-activation-steepness.md: « fann\_set\_activation\_steepness
  - function.fann-set-callback.md: fann\_set\_callback »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_bit\_fail\_limit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_bit\_fail\_limit

(PECL fann >= 1.0.0)

fann\_set\_bit\_fail\_limit — Встановлює межу помилок, що використовується під час навчання

### Опис

```methodsynopsis
fann_set_bit_fail_limit(resource $ann, float $bit_fail_limit): bool
```

Встановлює межу помилок, що використовується під час навчання.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`bit_fail_limit`

Межа помилок.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_bit\_fail\_limit()](function.fann-get-bit-fail-limit.md) \- Повертає межу збою бітів, використану під час навчання
