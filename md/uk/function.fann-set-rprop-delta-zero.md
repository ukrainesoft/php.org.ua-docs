---
navigation:
  - function.fann-set-rprop-delta-min.html: « fannsetrpropdeltamin
  - function.fann-set-rprop-increase-factor.html: fannsetrpropincreasefactor »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannsetrpropdeltazero
---
# fannsetrpropdeltazero

(PECL fann> = 1.0.0)

fannsetrpropdeltazero — Встановлює початковий розмір кроку

### Опис

```methodsynopsis
fann_set_rprop_delta_zero(resource $ann, float $rprop_delta_zero): bool
```

Початковий розмір кроку - це позитивне число, що визначає початковий розмір кроку.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`rprop_delta_zero`

Початковий розмір кроку.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanngetrpropdeltazero()](function.fann-get-rprop-delta-zero.md) - Повертає початковий розмір кроку
-   [fanngetrpropdeltamin()](function.fann-get-rprop-delta-min.md) - Повертає мінімальний розмір кроку
-   [fanngetrpropdeltamax()](function.fann-get-rprop-delta-max.md) - Повертає максимальний розмір кроку
