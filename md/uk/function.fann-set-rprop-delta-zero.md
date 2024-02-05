---
navigation:
  - function.fann-set-rprop-delta-min.md: « fann\_set\_rprop\_delta\_min
  - function.fann-set-rprop-increase-factor.md: fann\_set\_rprop\_increase\_factor »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_set\_rprop\_delta\_zero
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_set\_rprop\_delta\_zero

(PECL fann >= 1.0.0)

fann\_set\_rprop\_delta\_zero — Встановлює початковий розмір кроку

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

-   [fann\_get\_rprop\_delta\_zero()](function.fann-get-rprop-delta-zero.md) \- Повертає початковий розмір кроку
-   [fann\_get\_rprop\_delta\_min()](function.fann-get-rprop-delta-min.md) \- Повертає мінімальний розмір кроку
-   [fann\_get\_rprop\_delta\_max()](function.fann-get-rprop-delta-max.md) \- Повертає максимальний розмір кроку
