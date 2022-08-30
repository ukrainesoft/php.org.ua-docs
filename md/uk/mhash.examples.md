Приклади

-   [« Обумовлені константи](mhash.constants.md)
    
-   [Функции Mhash »](ref.mhash.md)
    
-   [PHP Manual](index.md)
    
-   [Mhash](book.mhash.md)
    
-   Приклади
    

# Приклади

**Приклад #1 Обчислення MD5 та HMAC та друк їх у шістнадцятковому вигляді**

```php
<?php
$input = "what do ya want for nothing?";
$hash = mhash(MHASH_MD5, $input);
echo "Хеш MD5 - " . bin2hex($hash) . "<br />\n";
$hash = mhash(MHASH_MD5, $input, "Jefe");
echo "Хеш HMAC - " . bin2hex($hash) . "<br />\n";
?>
```

Результат виконання цього прикладу:

```
Хеш MD5 - d03cb659cbf9192dcd066272249f8412
Хеш HMAC - 750c783e6ab0b503eaa86e310a5db738
```