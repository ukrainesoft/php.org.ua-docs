Визначити найкращий шлях декодування

-   [« Mailparse](ref.mailparse.html)
    
-   [mailparse\_msg\_create »](function.mailparse-msg-create.html)
    
-   [PHP Manual](index.html)
    
-   [Mailparse](ref.mailparse.html)
    
-   Визначити найкращий шлях декодування
    

# mailparsedeterminebestxferencoding

(PECL mailparse >= 0.9.0)

mailparsedeterminebestxferencoding - Визначити найкращий шлях декодування

### Опис

```methodsynopsis
mailparse_determine_best_xfer_encoding(resource $fp): string
```

Визначає найкращий шлях для декодування контенту, прочитаного із зазначеного файлового дескриптора.

### Список параметрів

`fp`

Коректний покажчик на файл, який має бути перемотується.

### Значення, що повертаються

Повертає одне з кодувань, що підтримується модулем [mbstring](ref.mbstring.html)

### Приклади

**Приклад #1 Приклад використання **mailparsedeterminebestxferencoding()****

```php
<?php

$fp = fopen('somemail.eml', 'r');
echo 'Best encoding: ' . mailparse_determine_best_xfer_encoding($fp);

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Best encoding: 7bit
```