---
navigation:
  - mhash.constants.md: « Зумовлені константи
  - ref.mhash.md: Функції Mhash »
  - index.md: PHP Manual
  - book.mhash.md: Mhash
title: Приклади
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Приклади

**Приклад #1 Обчислення MD5 та HMAC та друк їх у шістнадцятковому вигляді**

```php
<?php
$input = "what do ya want for nothing?";
$hash = mhash(MHASH_MD5, $input);
echo "Хеш MD5 - " . bin2hex($hash) . "<br />\n";
$hash = mhash(MHASH_MD5, $input, "Jefe");
echo "Хеш HMAC - " . bin2hex($hash) . "<br />\n";
?>
```

Результат виконання наведеного прикладу:

```
Хеш MD5 - d03cb659cbf9192dcd066272249f8412
Хеш HMAC - 750c783e6ab0b503eaa86e310a5db738
```
