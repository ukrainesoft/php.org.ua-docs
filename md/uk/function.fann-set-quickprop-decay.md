---
navigation:
  - function.fann-set-output-scaling-params.html: « fannsetoutputscalingparams
  - function.fann-set-quickprop-mu.html: fannsetquickpropmu »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannsetquickpropdecay
---
# fannsetquickpropdecay

(PECL fann> = 1.0.0)

fannsetquickpropdecay - Встановлює коефіцієнт загасання quickprop

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

-   [fanngetquickpropdecay()](function.fann-get-quickprop-decay.html) - Повертає зниження, яке є фактором, при якому ваги повинні зменшуватись на кожній ітерації під час навчання quickprop
