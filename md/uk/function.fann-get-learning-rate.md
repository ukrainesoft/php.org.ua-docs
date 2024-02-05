---
navigation:
  - function.fann-get-learning-momentum.md: « fann\_get\_learning\_momentum
  - function.fann-get-mse.md: fann\_get\_MSE »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_learning\_rate
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_learning\_rate

(PECL fann >= 1.0.0)

fann\_get\_learning\_rate — Повертає швидкість навчання

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

Швидкість навчання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_set\_learning\_rate()](function.fann-set-learning-rate.md) \- встановлює швидкість навчання
-   [fann\_set\_training\_algorithm()](function.fann-set-training-algorithm.md) \- встановлює алгоритм навчання
