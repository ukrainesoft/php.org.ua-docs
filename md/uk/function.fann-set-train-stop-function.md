---
navigation:
  - function.fann-set-train-error-function.md: « fann\_set\_train\_error\_function
  - function.fann-set-training-algorithm.md: fann\_set\_training\_algorithm »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_train\_stop\_function
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_train\_stop\_function

(PECL fann >= 1.0.0)

fann\_set\_train\_stop\_function — Встановлює функцію зупинки під час тренування.

### Опис

```methodsynopsis
fann_set_train_stop_function(resource $ann, int $stop_function): bool
```

Встановлює функцію зупинки під час тренування.

Функції зупинки описані далі в константах [функції зупинки](fann.constants.md#constants.fann-stopfunc)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`stop_function`

Константа[функції зупинки](fann.constants.md#constants.fann-stopfunc)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_train\_stop\_function()](function.fann-get-train-stop-function.md) \- Повертає функцію зупинки, що використовується під час навчання
