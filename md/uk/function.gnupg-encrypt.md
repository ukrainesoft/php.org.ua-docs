Шифрує заданий текст

-   [« gnupgdeletekey](function.gnupg-deletekey.html)
    
-   [gnupgencryptsign »](function.gnupg-encryptsign.html)
    
-   [PHP Manual](index.html)
    
-   [GnuPG Функції](ref.gnupg.html)
    
-   Шифрує заданий текст
    

# gnupgencrypt

(PECL gnupg >= 0.1)

gnupgencrypt - Шифрує заданий текст

### Опис

```methodsynopsis
gnupg_encrypt(resource $identifier, string $plaintext): string
```

Шифрує заданий текст `plaintext` за допомогою ключа, заданого раніше за допомогою функції [gnupgaddencryptkey](function.gnupg-addencryptkey.html) та повертає результат.

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupginit()](function.gnupg-init.html) або **gnupg**

`plaintext`

Текст для шифрування.

### Значення, що повертаються

У разі успішного виконання, повертає зашифрований текст. У разі виникнення помилки повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **gnupgencrypt()** у процедурному стилі**

```php
<?php
$res = gnupg_init();
gnupg_addencryptkey($res,"8660281B6051D071D94B5B230549F9DC851566DC");
$enc = gnupg_encrypt($res, "just a test");
echo $enc;
?>
```

**Приклад #2 Приклад використання **gnupgencrypt()** в об'єктно-орієнтованому стилі**

```php
<?php
$gpg = new gnupg();
$gpg->addencryptkey("8660281B6051D071D94B5B230549F9DC851566DC");
$enc = $gpg->encrypt("just a test");
echo $enc;
?>
```