---
navigation:
  - function.fann-set-scaling-params.md: « fannsetscalingparams
  - function.fann-set-train-stop-function.md: fannsettrainstopfunction »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannsettrainerrorfunction
---
# fannsettrainerrorfunction

(PECL fann> = 1.0.0)

fannsettrainerrorfunction — Встановлює функцію помилки під час тренування.

### Опис

```methodsynopsis
fann_set_train_error_function(resource $ann, int $error_function): bool
```

Встановлює функцію помилки під час тренування.

Функції помилок описані далі у константах [функций ошибок](fann.constants.md#constants.fann-errorfunc)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`error_function`

Константа [функций ошибок](fann.constants.md#constants.fann-errorfunc)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanngettrainerrorfunction()](function.fann-get-train-error-function.md) - Повертає функцію обробки помилок, що використовується під час навчання
