---
navigation:
  - function.fann-set-train-stop-function.html: « fannsettrainstopfunction
  - function.fann-set-weight-array.html: fannsetweightarray »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannsettrainingalgorithm
---
# fannsettrainingalgorithm

(PECL fann> = 1.0.0)

fannsettrainingalgorithm - Встановлює алгоритм навчання

### Опис

```methodsynopsis
fann_set_training_algorithm(resource $ann, int $training_algorithm): bool
```

Встановлює алгоритм навчання.

Докладніша інформація доступна в [fanngettrainingalgorithm()](function.fann-get-training-algorithm.html)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`training_algorithm`

Константа [Алгоритма обучения](fann.constants.html#constants.fann-train)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanngettrainingalgorithm()](function.fann-get-training-algorithm.html) - Повертає алгоритм навчання
