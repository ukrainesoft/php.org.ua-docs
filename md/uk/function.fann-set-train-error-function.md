---
navigation:
  - function.fann-set-scaling-params.html: « fannsetscalingparams
  - function.fann-set-train-stop-function.html: fannsettrainstopfunction »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
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

Функції помилок описані далі у константах [функций ошибок](fann.constants.html#constants.fann-errorfunc)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`error_function`

Константа [функций ошибок](fann.constants.html#constants.fann-errorfunc)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanngettrainerrorfunction()](function.fann-get-train-error-function.html) - Повертає функцію обробки помилок, що використовується під час навчання
