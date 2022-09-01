---
navigation:
  - function.fann-get-rprop-delta-max.html: « fanngetrpropdeltamax
  - function.fann-get-rprop-delta-zero.html: fanngetrpropdeltazero »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanngetrpropdeltamin
---
# fanngetrpropdeltamin

(PECL fann> = 1.0.0)

fanngetrpropdeltamin — Повертає мінімальний розмір кроку

### Опис

```methodsynopsis
fann_get_rprop_delta_min(resource $ann): float
```

Мінімальний розмір кроку - це невелике позитивне число, що визначає, наскільки невеликим може бути мінімальний розмір кроку.

Значення дельти за умовчанням min дорівнює 0.0.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Мінімальний розмір кроку або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannsetrpropdeltamin()](function.fann-set-rprop-delta-min.html) - Встановлює мінімальний розмір кроку
