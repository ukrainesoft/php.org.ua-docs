---
navigation:
  - function.fann-set-learning-momentum.md: « fann\_set\_learning\_momentum
  - function.fann-set-output-scaling-params.md: fann\_set\_output\_scaling\_params »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_learning\_rate
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_learning\_rate

(PECL fann >= 1.0.0)

fann\_set\_learning\_rate — Встановлює швидкість навчання

### Опис

```methodsynopsis
fann_set_learning_rate(resource $ann, float $learning_rate): bool
```

Встановлює швидкість навчання.

Докладніша інформація доступна в [fann\_get\_learning\_rate()](function.fann-get-learning-rate.md)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`learning_rate`

Швидкість навчання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_learning\_rate()](function.fann-get-learning-rate.md) \- Повертає швидкість навчання
-   [fann\_set\_training\_algorithm()](function.fann-set-training-algorithm.md) \- встановлює алгоритм навчання
