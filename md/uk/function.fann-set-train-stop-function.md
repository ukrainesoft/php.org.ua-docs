---
navigation:
  - function.fann-set-train-error-function.md: « fannsettrainerrorfunction
  - function.fann-set-training-algorithm.md: fannsettrainingalgorithm »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannsettrainstopfunction
---
# fannsettrainstopfunction

(PECL fann> = 1.0.0)

fannsettrainstopfunction — Встановлює функцію зупинки під час тренування.

### Опис

```methodsynopsis
fann_set_train_stop_function(resource $ann, int $stop_function): bool
```

Встановлює функцію зупинки під час тренування.

Функції зупинки описані далі в константах [функции остановки](fann.constants.md#constants.fann-stopfunc)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`stop_function`

Константа [функции остановки](fann.constants.md#constants.fann-stopfunc)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanngettrainstopfunction()](function.fann-get-train-stop-function.md) - Повертає функцію зупинки, що використовується під час навчання
