---
navigation:
  - function.fann-get-rprop-delta-zero.md: « fanngetrpropdeltazero
  - function.fann-get-sarprop-step-error-shift.md: fanngetsarpropsteperrorshift »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanngetrpropincreasefactor
---
# fanngetrpropincreasefactor

(PECL fann> = 1.0.0)

fanngetrpropincreasefactor — Повертає коефіцієнт збільшення під час навчання RPROP

### Опис

```methodsynopsis
fann_get_rprop_increase_factor(resource $ann): float
```

Коефіцієнт збільшення – це значення більше 1, яке використовується для збільшення розміру кроку під час навчання RPROP.

Коефіцієнт збільшення за умовчанням становить 1.2.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Коефіцієнт збільшення або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannsetrpropincreasefactor()](function.fann-set-rprop-increase-factor.md) - Встановлює коефіцієнт збільшення, який використовується під час навчання Rprop
