---
navigation:
  - function.fann-get-learning-momentum.html: « fanngetlearningmomentum
  - function.fann-get-mse.html: fanngetMSE »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
title: fanngetlearningrate
---
# fanngetlearningrate

(PECL fann> = 1.0.0)

fanngetlearningrate — Повертає швидкість навчання

### Опис

```methodsynopsis
fann_get_learning_rate(resource $ann): float
```

Швидкість навчання використовується визначення того, наскільки агресивним має бути навчання деяких алгоритмів навчання (**`FANN_TRAIN_INCREMENTAL`** **`FANN_TRAIN_BATCH`** **`FANN_TRAIN_QUICKPROP`**). Однак зверніть увагу, що вона не використовується в **`FANN_TRAIN_RPROP`**

Швидкість навчання за замовчуванням дорівнює 0.7.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Швидкість навчання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannsetlearningrate()](function.fann-set-learning-rate.md) - встановлює швидкість навчання
-   [fannsettrainingalgorithm()](function.fann-set-training-algorithm.md) - встановлює алгоритм навчання
