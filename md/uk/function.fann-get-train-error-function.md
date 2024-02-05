---
navigation:
  - function.fann-get-total-neurons.md: « fann\_get\_total\_neurons
  - function.fann-get-train-stop-function.md: fann\_get\_train\_stop\_function »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_train\_error\_function
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_train\_error\_function

(PECL fann >= 1.0.0)

fann\_get\_train\_error\_function — Повертає функцію обробки помилок, що використовується під час навчання

### Опис

```methodsynopsis
fann_get_train_error_function(resource $ann): int
```

Повертає функцію обробки помилок, яка використовується під час навчання.

Функції обробки помилок описані далі у константах [функції обробки помилок](fann.constants.md#constants.fann-errorfunc)

Функции обработки ошибок по умолчанию:**`FANN_ERRORFUNC_TANH`**

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Константа[функції обробки помилок](fann.constants.md#constants.fann-errorfunc)или\*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_set\_train\_error\_function()](function.fann-set-train-error-function.md) \- Встановлює функцію помилки, що використовується під час тренування
