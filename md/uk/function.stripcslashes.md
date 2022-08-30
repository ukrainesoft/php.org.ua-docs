Видаляє екранування символів, зроблене функцією addcslashes

-   [« striptags](function.strip-tags.html)
    
-   [stripos »](function.stripos.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з рядками](ref.strings.html)
    
-   Видаляє екранування символів, зроблене функцією addcslashes
    

# stripcslashes

(PHP 4, PHP 5, PHP 7, PHP 8)

stripcslashes — Видаляє екранування символів, зроблене функцією [addcslashes()](function.addcslashes.html)

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

-   [addcslashes()](function.addcslashes.html) - Екранує рядок слішами у стилі мови C