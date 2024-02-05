---
navigation:
  - function.fann-get-train-error-function.md: « fann\_get\_train\_error\_function
  - function.fann-get-training-algorithm.md: fann\_get\_training\_algorithm »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_train\_stop\_function
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_train\_stop\_function

(PECL fann >= 1.0.0)

fann\_get\_train\_stop\_function — Повертає функцію зупинки, що використовується під час навчання

### Опис

```methodsynopsis
fann_get_train_stop_function(resource $ann): int
```

Повертає функцію зупинки під час навчання.

Опції зупинки описані далі в константах [функції зупинки](fann.constants.md#constants.fann-stopfunc)

Функция остановки по умолчанию:**`FANN_STOPFUNC_MSE`**

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Константа[функції зупинки](fann.constants.md#constants.fann-stopfunc)или\*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_set\_train\_stop\_function()](function.fann-set-train-stop-function.md) \- Встановлює функцію зупинки під час тренування.
