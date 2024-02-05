---
navigation:
  - function.fann-set-rprop-delta-max.md: « fann\_set\_rprop\_delta\_max
  - function.fann-set-rprop-delta-zero.md: fann\_set\_rprop\_delta\_zero »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_rprop\_delta\_min
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_rprop\_delta\_min

(PECL fann >= 1.0.0)

fann\_set\_rprop\_delta\_min — Встановлює мінімальний розмір кроку

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

-   [fann\_get\_rprop\_delta\_min()](function.fann-get-rprop-delta-min.md) \- Повертає мінімальний розмір кроку
