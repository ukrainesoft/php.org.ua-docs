---
navigation:
  - function.fann-get-train-stop-function.md: « fanngettrainstopfunction
  - function.fann-init-weights.md: fanninitweights »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanngettrainingalgorithm
---
# fanngettrainingalgorithm

(PECL fann> = 1.0.0)

fanngettrainingalgorithm - Повертає алгоритм навчання

### Опис

```methodsynopsis
fann_get_training_algorithm(resource $ann): int
```

Повертає алгоритм навчання. Цей алгоритм навчання використовується [fanntrainвінdata()](function.fann-train-on-data.md) та пов'язаними функціями.

Зверніть увагу, що цей алгоритм також використовується під час [fanncascadetrainвінdata()](function.fann-cascadetrain-on-data.md), хоча під час каскадного навчання дозволено лише **`FANN_TRAIN_RPROP`** and **`FANN_TRAIN_QUICKPROP`**

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Константа [Алгоритма обучения](fann.constants.md#constants.fann-train) або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannsettrainingalgorithm()](function.fann-set-training-algorithm.md) - встановлює алгоритм навчання
