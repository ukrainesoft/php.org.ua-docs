---
navigation:
  - function.fann-get-rprop-delta-min.md: « fanngetrpropdeltamin
  - function.fann-get-rprop-increase-factor.md: fanngetrpropincreasefactor »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanngetrpropdeltazero
---
# fanngetrpropdeltazero

(PECL fann> = 1.0.0)

fanngetrpropdeltazero — Повертає початковий розмір кроку

### Опис

```methodsynopsis
fann_get_rprop_delta_zero(resource $ann): int
```

Початковий розмір кроку - це позитивне число, що визначає початковий розмір кроку.

За умовчанням нульове значення дельти дорівнює 0.1.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Початковий розмір кроку або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannsetrpropdeltazero()](function.fann-set-rprop-delta-zero.md) - Встановлює початковий розмір кроку
-   [fanngetrpropdeltamin()](function.fann-get-rprop-delta-min.md) - Повертає мінімальний розмір кроку
-   [fanngetrpropdeltamax()](function.fann-get-rprop-delta-max.md) - Повертає максимальний розмір кроку
