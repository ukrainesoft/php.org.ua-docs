---
navigation:
  - function.is-finite.md: « isfinite
  - function.is-nan.md: ісnan »
  - index.md: PHP Manual
  - ref.math.md: Математичні функції
title: ісinfinite
---
# ісinfinite

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

ісinfinite — Перевіряє, чи є значення нескінченним

### Опис

```methodsynopsis
is_infinite(float $num): bool
```

Повертає **`true`**, якщо `num` є нескінченністю (позитивною або негативною), наприклад, як результат обчислення `log(0)` або будь-які інші значення, занадто великі, щоб уміститися в тип float на даній платформі.

### Список параметрів

`num`

Перевірене значення

### Значення, що повертаються

**`true`**, якщо `num` є нескінченним, **`false`** в іншому випадку.

### Дивіться також

-   [ісfinite()](function.is-finite.md) - Перевіряє, чи є значення допустимим кінцевим числом
-   [ісnan()](function.is-nan.md) - Перевіряє, чи є значення "не числом"
