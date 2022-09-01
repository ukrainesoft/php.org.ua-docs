---
navigation:
  - function.fann-set-quickprop-mu.html: « fannsetquickpropму
  - function.fann-set-rprop-delta-max.html: fannsetrpropdeltamax »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
title: fannsetrpropdecreasefactor
---
# fannsetrpropdecreasefactor

(PECL fann> = 1.0.0)

fannsetrpropdecreasefactor — Встановлює коефіцієнт зменшення під час навчання RPROP

### Опис

```methodsynopsis
fann_set_rprop_decrease_factor(resource $ann, float $rprop_decrease_factor): bool
```

Встановлює коефіцієнт зменшення під час навчання RPROP.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`rprop_decrease_factor`

Коефіцієнт зменшення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanngetrpropdecreasefactor()](function.fann-get-rprop-decrease-factor.html) - Повертає коефіцієнт зменшення під час навчання RPROP
