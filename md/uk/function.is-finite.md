---
navigation:
  - function.intdiv.md: « intdiv
  - function.is-infinite.md: is\_infinite »
  - index.md: PHP Manual
  - ref.math.md: Математичні функції
title: is\_finite
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# is\_finite

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

is\_finite — Перевіряє, чи звичайно число з плаваючою точкою

### Опис

```methodsynopsis
is_finite(float $num): bool
```

Повертає результат перевірки того, чи звичайно передане параметр `num` число з плаваючою точкою.

Кінцеве число з плаваючою точкою - це не число (`NAN`), як його обчислює функція [is\_nan()](function.is-nan.md), ні нескінченність, як її обчислює функція [is\_infinite()](function.is-infinite.md)

### Список параметрів

`num`

Перевірене число з плаваючою точкою (float)

### Значення, що повертаються

Повертає **`true`**, если значение`num`не нечисло`NAN`, не позитивна нескінченність `INF`, не негативна нескінченність `-INF`, иначе\*\*`false`\*\*

### Приклади

**Пример #1 Пример использования функции**is\_finite()\*\*\*\*

```php
<?php

$float = 1.2345;
var_dump($float, is_finite($float));

$nan = sqrt(-1);
var_dump($nan, is_finite($nan));

$inf = 1e308 * 2;
var_dump($inf, is_finite($inf));

?>
```

Результат виконання наведеного прикладу:

```
float(1.2345)
bool(true)
float(NAN)
bool(false)
float(INF)
bool(false)
```

### Дивіться також

-   [is\_infinite()](function.is-infinite.md) \- Перевіряє, чи нескінченне число з плаваючою точкою
-   [is\_nan()](function.is-nan.md) \- Перевіряє, чи є число з плаваючою точкою нечисло
