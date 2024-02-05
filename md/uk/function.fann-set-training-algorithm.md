---
navigation:
  - function.fann-set-train-stop-function.md: « fann\_set\_train\_stop\_function
  - function.fann-set-weight-array.md: fann\_set\_weight\_array »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_training\_algorithm
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_training\_algorithm

(PECL fann >= 1.0.0)

fann\_set\_training\_algorithm - Встановлює алгоритм навчання

### Опис

```methodsynopsis
fann_set_training_algorithm(resource $ann, int $training_algorithm): bool
```

Встановлює алгоритм навчання.

Докладніша інформація доступна в [fann\_get\_training\_algorithm()](function.fann-get-training-algorithm.md)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`training_algorithm`

Константа[Алгоритма навчання](fann.constants.md#constants.fann-train)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_training\_algorithm()](function.fann-get-training-algorithm.md) \- Повертає алгоритм навчання
