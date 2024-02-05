---
navigation:
  - function.fann-get-rprop-decrease-factor.md: « fann\_get\_rprop\_decrease\_factor
  - function.fann-get-rprop-delta-min.md: fann\_get\_rprop\_delta\_min »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_rprop\_delta\_max
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_rprop\_delta\_max

(PECL fann >= 1.0.0)

fann\_get\_rprop\_delta\_max — Повертає максимальний розмір кроку

### Опис

```methodsynopsis
fann_get_rprop_delta_max(resource $ann): float
```

Максимальний розмір кроку - це позитивне число, що визначає, наскільки більшим може бути максимальний розмір кроку.

Максимальне значення дельти за промовчанням становить 50.0.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Максимальний розмір кроку або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_set\_rprop\_delta\_max()](function.fann-set-rprop-delta-max.md) \- Встановлює максимальний розмір кроку
-   [fann\_get\_rprop\_delta\_min()](function.fann-get-rprop-delta-min.md) \- Повертає мінімальний розмір кроку
