---
navigation:
  - function.fann-set-quickprop-decay.html: « fannsetquickpropdecay
  - function.fann-set-rprop-decrease-factor.html: fannsetrpropdecreasefactor »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
title: fannsetquickpropму
---
# fannsetquickpropму

(PECL fann> = 1.0.0)

fannsetquickpropmu - Встановлює МЮ-фактор quickprop

### Опис

```methodsynopsis
fann_set_quickprop_mu(resource $ann, float $quickprop_mu): bool
```

Встановлює МЮ-фактор quickprop.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`quickprop_mu`

МЮ-фактор quickprop.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanngetquickpropmu()](function.fann-get-quickprop-mu.html) - Повертає коефіцієнт mu
