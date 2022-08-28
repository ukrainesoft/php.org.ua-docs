Повертає рядок, що повторюється

-   [« str\_pad](function.str-pad.html)
    
-   [str\_replace »](function.str-replace.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы со строками](ref.strings.html)
    
-   Повертає рядок, що повторюється
    

# strrepeat

(PHP 4, PHP 5, PHP 7, PHP 8)

strrepeat — Повертає рядок, що повторюється.

### Опис

```methodsynopsis
str_repeat(string $string, int $times): string
```

Повертає рядок `string`, повторену `times` разів.

### Список параметрів

`string`

Повторюваний рядок.

`times`

Кількість разів, які потрібно повторити рядок `string`

`times` повинен бути більшим або дорівнює нулю. Якщо `times` дорівнює нулю, повертається порожній рядок.

### Значення, що повертаються

Повертає рядок, що повторюється.

### Приклади

**Приклад #1 Приклад використання **strrepeat()****

```php
<?php
echo str_repeat("-=", 10);
?>
```

Результат виконання цього прикладу:

```
-=-=-=-=-=-=-=-=-=-=
```

### Дивіться також

-   [for](control-structures.for.html)
-   [str\_pad()](function.str-pad.html) - Доповнює рядок іншим рядком до заданої довжини
-   [substr\_count()](function.substr-count.html) - Повертає кількість входжень підрядка