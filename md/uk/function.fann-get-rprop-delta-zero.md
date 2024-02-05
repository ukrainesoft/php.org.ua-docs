---
navigation:
  - function.fann-get-rprop-delta-min.md: « fann\_get\_rprop\_delta\_min
  - function.fann-get-rprop-increase-factor.md: fann\_get\_rprop\_increase\_factor »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_rprop\_delta\_zero
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_rprop\_delta\_zero

(PECL fann >= 1.0.0)

fann\_get\_rprop\_delta\_zero — Повертає початковий розмір кроку

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

Початковий розмір кроку або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_set\_rprop\_delta\_zero()](function.fann-set-rprop-delta-zero.md) \- Встановлює початковий розмір кроку
-   [fann\_get\_rprop\_delta\_min()](function.fann-get-rprop-delta-min.md) \- Повертає мінімальний розмір кроку
-   [fann\_get\_rprop\_delta\_max()](function.fann-get-rprop-delta-max.md) \- Повертає максимальний розмір кроку
