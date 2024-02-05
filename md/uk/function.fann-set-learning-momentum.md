---
navigation:
  - function.fann-set-input-scaling-params.md: « fann\_set\_input\_scaling\_params
  - function.fann-set-learning-rate.md: fann\_set\_learning\_rate »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_learning\_momentum
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_learning\_momentum

(PECL fann >= 1.0.0)

fann\_set\_learning\_momentum - Встановлює імпульс навчання

### Опис

```methodsynopsis
fann_set_learning_momentum(resource $ann, float $learning_momentum): bool
```

Встановлює імпульс навчання.

Докладніша інформація доступна в [fann\_get\_learning\_momentum()](function.fann-get-learning-momentum.md)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`learning_momentum`

Імпульс навчання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_learning\_momentum()](function.fann-get-learning-momentum.md) \- Повертає імпульс навчання
-   [fann\_set\_training\_algorithm()](function.fann-set-training-algorithm.md) \- встановлює алгоритм навчання
