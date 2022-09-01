---
navigation:
  - function.fann-set-learning-momentum.html: « fannsetlearningmomentum
  - function.fann-set-output-scaling-params.html: fannsetoutputscalingparams »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannsetlearningrate
---
# fannsetlearningrate

(PECL fann> = 1.0.0)

fannsetlearningrate — Встановлює швидкість навчання

### Опис

```methodsynopsis
fann_set_learning_rate(resource $ann, float $learning_rate): bool
```

Встановлює швидкість навчання.

Докладніша інформація доступна в [fanngetlearningrate()](function.fann-get-learning-rate.md)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`learning_rate`

Швидкість навчання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanngetlearningrate()](function.fann-get-learning-rate.md) - Повертає швидкість навчання
-   [fannsettrainingalgorithm()](function.fann-set-training-algorithm.md) - встановлює алгоритм навчання
