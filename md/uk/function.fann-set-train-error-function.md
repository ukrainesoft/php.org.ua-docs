---
navigation:
  - function.fann-set-scaling-params.md: « fann\_set\_scaling\_params
  - function.fann-set-train-stop-function.md: fann\_set\_train\_stop\_function »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_train\_error\_function
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_train\_error\_function

(PECL fann >= 1.0.0)

fann\_set\_train\_error\_function — Встановлює функцію помилки під час тренування.

### Опис

```methodsynopsis
fann_set_train_error_function(resource $ann, int $error_function): bool
```

Встановлює функцію помилки під час тренування.

Функції помилок описані далі у константах [функцій помилок](fann.constants.md#constants.fann-errorfunc)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`error_function`

Константа[функцій помилок](fann.constants.md#constants.fann-errorfunc)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_train\_error\_function()](function.fann-get-train-error-function.md) \- Повертає функцію обробки помилок, що використовується під час навчання
