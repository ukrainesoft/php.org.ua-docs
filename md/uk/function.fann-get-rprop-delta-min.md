---
navigation:
  - function.fann-get-rprop-delta-max.md: « fann\_get\_rprop\_delta\_max
  - function.fann-get-rprop-delta-zero.md: fann\_get\_rprop\_delta\_zero »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_rprop\_delta\_min
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_rprop\_delta\_min

(PECL fann >= 1.0.0)

fann\_get\_rprop\_delta\_min — Повертає мінімальний розмір кроку

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

Мінімальний розмір кроку або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_set\_rprop\_delta\_min()](function.fann-set-rprop-delta-min.md) \- Встановлює мінімальний розмір кроку
