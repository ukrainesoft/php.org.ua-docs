---
navigation:
  - function.fann-set-output-scaling-params.md: « fann\_set\_output\_scaling\_params
  - function.fann-set-quickprop-mu.md: fann\_set\_quickprop\_mu »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_quickprop\_decay
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_quickprop\_decay

(PECL fann >= 1.0.0)

fann\_set\_quickprop\_decay - Встановлює коефіцієнт загасання quickprop

### Опис

```methodsynopsis
fann_set_quickprop_decay(resource $ann, float $quickprop_decay): bool
```

Встановлює коефіцієнт загасання quickprop.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`quickprop_decay`

Коефіцієнт згасання quickprop.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_get\_quickprop\_decay()](function.fann-get-quickprop-decay.md) \- Повертає зниження, яке є фактором, при якому ваги повинні зменшуватись на кожній ітерації під час навчання quickprop
