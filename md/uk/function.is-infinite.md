---
navigation:
  - function.is-finite.md: « is\_finite
  - function.is-nan.md: is\_nan »
  - index.md: PHP Manual
  - ref.math.md: Математичні функції
title: is\_infinite
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# is\_infinite

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

is\_infinite — Перевіряє, чи нескінченне число з плаваючою точкою

### Опис

```methodsynopsis
is_infinite(float $num): bool
```

Повертає результат перевірки того, чи належить передане параметр `num` значення до позитивної (`INF`) або негативної нескінченності (`-INF`

### Список параметрів

`num`

Перевірене число з плаваючою точкою (float).

### Значення, що повертаються

Повертає **`true`**, если значение параметра`num` - Безкінечне позитивне число (`INF`) або негативне нескінченне число (`-INF`), иначе\*\*`false`\*\*

### Приклади

**Пример #1 Пример использования функции**is\_infinite()\*\*\*\*

```php
<?php

$inf = 1e308 * 2;

var_dump($inf, is_infinite($inf));

$negative_inf = -$inf;

var_dump($negative_inf, is_infinite($negative_inf));

?>
```

Результат виконання наведеного прикладу:

```
float(INF)
bool(true)
float(-INF)
bool(true)
```

### Дивіться також

-   [is\_finite()](function.is-finite.md) \- Перевіряє, чи звичайно число з плаваючою точкою
-   [is\_nan()](function.is-nan.md) \- Перевіряє, чи є число з плаваючою точкою нечисло
