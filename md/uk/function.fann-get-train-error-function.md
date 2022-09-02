---
navigation:
  - function.fann-get-total-neurons.md: « fanngettotalneurons
  - function.fann-get-train-stop-function.md: fanngettrainstopfunction »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanngettrainerrorfunction
---
# fanngettrainerrorfunction

(PECL fann> = 1.0.0)

fanngettrainerrorfunction — Повертає функцію обробки помилок, що використовується під час навчання

### Опис

```methodsynopsis
fann_get_train_error_function(resource $ann): int
```

Повертає функцію обробки помилок, яка використовується під час навчання.

Функції обробки помилок описані далі у константах [функции обработки ошибок](fann.constants.md#constants.fann-errorfunc)

Функції обробки помилок за замовчуванням: **`FANN_ERRORFUNC_TANH`**

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Константа [функции обработки ошибок](fann.constants.md#constants.fann-errorfunc) або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannsettrainerrorfunction()](function.fann-set-train-error-function.md) - Встановлює функцію помилки, що використовується під час тренування
