---
navigation:
  - ref.mailparse.md: « Mailparse
  - function.mailparse-msg-create.md: mailparse\_msg\_create »
  - index.md: PHP Manual
  - ref.mailparse.md: Mailparse
title: mailparse\_determine\_best\_xfer\_encoding
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mailparse\_determine\_best\_xfer\_encoding

(PECL mailparse >= 0.9.0)

mailparse\_determine\_best\_xfer\_encoding - Визначити найкращий шлях декодування

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

**Пример #1 Пример использования**mailparse\_determine\_best\_xfer\_encoding()\*\*\*\*

```php
<?php

$fp = fopen('somemail.eml', 'r');
echo 'Best encoding: ' . mailparse_determine_best_xfer_encoding($fp);

?>
```

Висновок наведеного прикладу буде схожим на:

```
Best encoding: 7bit
```
