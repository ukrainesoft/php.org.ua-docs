Кодує рядок у формат uuencode

-   [« convert\_uudecode](function.convert-uudecode.html)
    
-   [count\_chars »](function.count-chars.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы со строками](ref.strings.html)
    
-   Кодує рядок у формат uuencode
    

# convertuuencode

(PHP 5, PHP 7, PHP 8)

convertuuencode — Кодує рядок у форматі uuencode

### Опис

```methodsynopsis
convert_uuencode(string $string): string
```

**convertuuencode()** кодує рядок за допомогою алгоритму uuencode.

Кодування uuencode переводить рядки (включаючи бінарні символи) у послідовності друкованих (7-бітних) ASCII-символів, що дозволяє безпечно обмінюватися даними через мережу. Закодовані дані приблизно на 35% більше від оригіналу.

> **Зауваження** [convert\_uudecode()](function.convert-uudecode.html) не приймає ні початкової (`begin`), ні кінцевої (`end`) рядки, яка є частиною файлів (*files*) uuencoded.

### Список параметрів

`string`

Кодовані дані.

### Значення, що повертаються

Повертає закодовані дані у форматі uuencode.

### список змін

| Версия | Описание |
| --- | --- |
|  | До цієї версії при спробі перетворити порожній рядок поверталося **`false`** без особливих причин. |

### Приклади

**Приклад #1 Приклад використання **convertuuencode()****

```php
<?php
$some_string = "test\ntext text\r\n";

echo convert_uuencode($some_string);
?>
```

Результат виконання цього прикладу:

```
0=&5S=`IT97AT('1E>'0-"@``
`
```

### Дивіться також

-   [convert\_uudecode()](function.convert-uudecode.html) - Декодує рядок із формату uuencode у звичайний вигляд
-   [base64\_encode()](function.base64-encode.html) - Кодує дані у формат MIME base64