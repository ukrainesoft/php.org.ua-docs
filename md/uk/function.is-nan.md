---
navigation:
  - function.is-infinite.html: « isinfinite
  - function.lcg-value.html: lcgvalue »
  - index.html: PHP Manual
  - ref.math.html: Математичні функції
title: ісnan
---
# ісnan

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

ісnan — Перевіряє, чи є значення "не числом"

### Опис

```methodsynopsis
is_nan(float $num): bool
```

Перевіряє, чи є `num` "не числом" (NaN), наприклад, як результат виконання функції `acos(1.01)`

### Список параметрів

`num`

Перевірене значення

### Значення, що повертаються

Повертає **`true`**, якщо `num` має значення "не число" (NaN), **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ісnan()****

```php
<?php
// Недопустимое вычисление, возвращает
// значение "не число" (NaN)
$nan = acos(8);

var_dump($nan, is_nan($nan));
?>
```

Результат виконання цього прикладу:

```
float(NAN)
bool(true)
```

### Дивіться також

-   [ісfinite()](function.is-finite.html) - Перевіряє, чи є значення допустимим кінцевим числом
-   [ісinfinite()](function.is-infinite.html) - Перевіряє, чи є значення нескінченним
