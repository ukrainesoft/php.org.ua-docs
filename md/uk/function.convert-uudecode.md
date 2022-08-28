Декодує рядок із формату uuencode у звичайний вигляд

-   [« convert\_cyr\_string](function.convert-cyr-string.html)
    
-   [convert\_uuencode »](function.convert-uuencode.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы со строками](ref.strings.html)
    
-   Декодує рядок із формату uuencode у звичайний вигляд
    

# convertuudecode

(PHP 5, PHP 7, PHP 8)

convertuudecode — Декодує рядок із формату uuencode у звичайний вигляд

### Опис

```methodsynopsis
convert_uudecode(string $string): string|false
```

**convertuudecode()** декодує рядок із формату uuencode у звичайний вигляд.

> **Зауваження** **convertuudecode()** не приймає ні початкової (`begin`), ні кінцевої (`end`) рядки, яка є частиною файлів (*files*) uuencoded.

### Список параметрів

`string`

Дані у форматі uuencode.

### Значення, що повертаються

Повертає декодовані дані у вигляді рядка або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **convertuudecode()****

```php
<?php
echo convert_uudecode("+22!L;W9E(%!(4\"$`\n`");
?>
```

Результат виконання цього прикладу:

```
I love PHP!
```

### Дивіться також

-   [convert\_uuencode()](function.convert-uuencode.html) - Кодує рядок у форматі uuencode