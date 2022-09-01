---
navigation:
  - function.fann-set-rprop-decrease-factor.html: « fannsetrpropdecreasefactor
  - function.fann-set-rprop-delta-min.html: fannsetrpropdeltamin »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
title: fannsetrpropdeltamax
---
# fannsetrpropdeltamax

(PECL fann> = 1.0.0)

fannsetrpropdeltamax — Встановлює максимальний розмір кроку

### Опис

```methodsynopsis
fann_set_rprop_delta_max(resource $ann, float $rprop_delta_max): bool
```

Максимальний розмір кроку - це позитивне число, що визначає, наскільки більшим може бути максимальний розмір кроку.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`rprop_delta_max`

Максимальний розмір кроку.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanngetrpropdeltamax()](function.fann-get-rprop-delta-max.md) - Повертає максимальний розмір кроку
-   [fanngetrpropdeltamin()](function.fann-get-rprop-delta-min.md) - Повертає мінімальний розмір кроку
