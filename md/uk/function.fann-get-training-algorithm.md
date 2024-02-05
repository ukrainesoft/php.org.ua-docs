---
navigation:
  - function.fann-get-train-stop-function.md: « fann\_get\_train\_stop\_function
  - function.fann-init-weights.md: fann\_init\_weights »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_training\_algorithm
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_training\_algorithm

(PECL fann >= 1.0.0)

fann\_get\_training\_algorithm - Повертає алгоритм навчання

### Опис

```methodsynopsis
fann_get_training_algorithm(resource $ann): int
```

Повертає алгоритм навчання. Цей алгоритм навчання використовується [fann\_train\_on\_data()](function.fann-train-on-data.md) та пов'язаними функціями.

Зверніть увагу, що цей алгоритм також використовується під час [fann\_cascadetrain\_on\_data()](function.fann-cascadetrain-on-data.md), хоча під час каскадного навчання дозволено лише **`FANN_TRAIN_RPROP`**and**`FANN_TRAIN_QUICKPROP`**

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Константа[Алгоритма навчання](fann.constants.md#constants.fann-train)или\*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_set\_training\_algorithm()](function.fann-set-training-algorithm.md) \- встановлює алгоритм навчання
