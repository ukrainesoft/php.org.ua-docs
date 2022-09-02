---
navigation:
  - function.fann-set-rprop-delta-max.md: « fannsetrpropdeltamax
  - function.fann-set-rprop-delta-zero.md: fannsetrpropdeltazero »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannsetrpropdeltamin
---
# fannsetrpropdeltamin

(PECL fann> = 1.0.0)

fannsetrpropdeltamin — Встановлює мінімальний розмір кроку

### Опис

```methodsynopsis
fann_set_rprop_delta_min(resource $ann, float $rprop_delta_min): bool
```

Мінімальний розмір кроку - це невелике позитивне число, що визначає, наскільки невеликим може бути мінімальний розмір кроку.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`rprop_delta_min`

Мінімальний розмір кроку.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanngetrpropdeltamin()](function.fann-get-rprop-delta-min.md) - Повертає мінімальний розмір кроку
