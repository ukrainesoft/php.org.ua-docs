---
navigation:
  - ref.mailparse.md: « Mailparse
  - function.mailparse-msg-create.md: mailparsemsgcreate »
  - index.md: PHP Manual
  - ref.mailparse.md: Mailparse
title: mailparsedeterminebestxferencoding
---
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

Повертає одне з кодувань, що підтримується модулем [mbstring](ref.mbstring.md)

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
