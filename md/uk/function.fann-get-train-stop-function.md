---
navigation:
  - function.fann-get-train-error-function.md: « fanngettrainerrorfunction
  - function.fann-get-training-algorithm.md: fanngettrainingalgorithm »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanngettrainstopfunction
---
# fanngettrainstopfunction

(PECL fann> = 1.0.0)

fanngettrainstopfunction — Повертає функцію зупинки, що використовується під час навчання

### Опис

```methodsynopsis
fann_get_train_stop_function(resource $ann): int
```

Повертає функцію зупинки під час навчання.

Опції зупинки описані далі в константах [функции остановки](fann.constants.md#constants.fann-stopfunc)

За замовчуванням функція зупинки: **`FANN_STOPFUNC_MSE`**

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Константа [функции остановки](fann.constants.md#constants.fann-stopfunc) або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannsettrainstopfunction()](function.fann-set-train-stop-function.md) - Встановлює функцію зупинки під час тренування.
