---
navigation:
  - function.intdiv.md: « intdiv
  - function.is-infinite.md: ісinfinite »
  - index.md: PHP Manual
  - ref.math.md: Математичні функції
title: ісfinite
---
# ісfinite

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

ісfinite — Перевіряє, чи є значення допустимим кінцевим числом

### Опис

```methodsynopsis
is_finite(float $num): bool
```

Перевіряє, чи є `num` допустимим кінцевим числом на цій платформі.

### Список параметрів

`num`

Перевірене значення

### Значення, що повертаються

**`true`**, якщо `num` є допустимим кінцевим числом у дозволеному для типу PHP float діапазоні на даній платформі, **`false`** в іншому випадку.

### Дивіться також

-   [ісinfinite()](function.is-infinite.md) - Перевіряє, чи є значення нескінченним
-   [ісnan()](function.is-nan.md) - Перевіряє, чи є значення "не числом"
