---
navigation:
  - function.fann-set-quickprop-mu.md: « fannsetquickpropму
  - function.fann-set-rprop-delta-max.md: fannsetrpropdeltamax »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
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

-   [fanngetrpropdecreasefactor()](function.fann-get-rprop-decrease-factor.md) - Повертає коефіцієнт зменшення під час навчання RPROP
