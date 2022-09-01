---
navigation:
  - function.strip-tags.html: « striptags
  - function.stripos.html: stripos »
  - index.html: PHP Manual
  - ref.strings.html: Функції для роботи з рядками
title: stripcslashes
---
# stripcslashes

(PHP 4, PHP 5, PHP 7, PHP 8)

stripcslashes — Видаляє екранування символів, зроблене функцією [addcslashes()](function.addcslashes.md)

### Опис

```methodsynopsis
stripcslashes(string $string): string
```

Видаляє екранні зворотні сліші. Розпізнає екранування у стилі C (`\n` `\r` ..., вісімкове та шістнадцяткове уявлення).

### Список параметрів

`string`

Рядок, у якого потрібно прибрати екранування.

### Значення, що повертаються

Повертає неекранований рядок.

### Приклади

**Приклад #1 Приклад використання **stripcslashes()****

```php
<?php

var_dump(stripcslashes('I\'d have a coffee.\nNot a problem.') === "I'd have a coffee.
Not a problem."); // true
?>
```

### Дивіться також

-   [addcslashes()](function.addcslashes.md) - Екранує рядок слішами у стилі мови C
