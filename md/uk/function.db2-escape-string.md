Використовується для екранування деяких символів

-   [« db2cursortype](function.db2-cursor-type.html)
    
-   [db2exec »](function.db2-exec.html)
    
-   [PHP Manual](index.html)
    
-   [Функції IBM DB2](ref.ibm-db2.html)
    
-   Використовується для екранування деяких символів
    

# db2escapestring

(PECL ibmdb2> = 1.6.0)

db2escapestring — Використовується для екранування деяких символів

### Опис

```methodsynopsis
db2_escape_string(string $string_literal): string
```

Додає зворотні сліші перед спеціальними символами в переданому рядку.

### Список параметрів

`string_literal`

Рядок, що містить символи, які потрібно екранувати. Символи, які потрібно екранувати: `\x00` `\n` `\r` `\` `'` `"` і `\x1a`

### Значення, що повертаються

Повертає `string_literal` з екранованих спеціальних символів.

### Приклади

**Приклад #1 Приклад використання **db2escapestring()****

Результат виконання функції **db2escapestring()**

```php
<?php

$conn = db2_connect($database, $user, $password);

if ($conn) {
    $str[0] = "All characters: \x00 , \n , \r , \ , ' , \" , \x1a .";
    $str[1] = "Backslash (\). Single quote ('). Double quote (\")";
    $str[2] = "The NULL character \0 must be quoted as well";
    $str[3] = "Intersting characters: \x1a , \x00 .";
    $str[4] = "Nothing to quote";
    $str[5] = 200676;
    $str[6] = "";

    foreach( $str as $string ) {
        echo "db2_escape_string: " . db2_escape_string($string). "\n";
    }
}
?>
```

Результат виконання цього прикладу:

```
db2_escape_string: All characters: \0 , \n , \r , \\ , \' , \" , \Z .
db2_escape_string: Backslash (\\). Single quote (\'). Double quote (\")
db2_escape_string: The NULL character \0 must be quoted as well
db2_escape_string: Intersting characters: \Z , \0 .
db2_escape_string: Nothing to quote
db2_escape_string: 200676
db2_escape_string:
```

### Дивіться також

-   [db2prepare()](function.db2-prepare.html) - готує SQL-запит до виконання