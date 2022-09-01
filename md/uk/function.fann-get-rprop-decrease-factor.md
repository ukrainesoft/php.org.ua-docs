---
navigation:
  - function.fann-get-quickprop-mu.html: « fanngetquickpropму
  - function.fann-get-rprop-delta-max.html: fanngetrpropdeltamax »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanngetrpropdecreasefactor
---
# fanngetrpropdecreasefactor

(PECL fann> = 1.0.0)

fanngetrpropdecreasefactor — Повертає коефіцієнт зменшення під час навчання RPROP

### Опис

```methodsynopsis
fann_get_rprop_decrease_factor(resource $ann): float
```

Коефіцієнт зменшення - це значення менше 1, яке використовується зменшення розміру кроку під час навчання RPROP.

Коефіцієнт зменшення за промовчанням становить 0.5.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Коефіцієнт зменшення або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannsetrpropdecreasefactor()](function.fann-set-rprop-decrease-factor.html) - Встановлює коефіцієнт зменшення під час навчання RPROP
