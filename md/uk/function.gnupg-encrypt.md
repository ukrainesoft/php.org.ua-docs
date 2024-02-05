---
navigation:
  - function.gnupg-deletekey.md: « gnupg\_deletekey
  - function.gnupg-encryptsign.md: gnupg\_encryptsign »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupg\_encrypt
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gnupg\_encrypt

(PECL gnupg >= 0.1)

gnupg\_encrypt - Шифрує заданий текст

### Опис

```methodsynopsis
gnupg_encrypt(resource $identifier, string $plaintext): string|false
```

Шифрує заданий текст `plaintext` за допомогою ключа, заданого раніше за допомогою функції [gnupg\_addencryptkey](function.gnupg-addencryptkey.md) та повертає результат.

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.md)или**gnupg**

`plaintext`

Текст для шифрування.

### Значення, що повертаються

У разі успішного виконання, повертає зашифрований текст. У разі виникнення помилки повертає **`false`**

### Приклади

**Приклад #1 Приклад використання** gnupg\_encrypt()\*\* у процедурному стилі\*\*

```php
<?php
$res = gnupg_init();
gnupg_addencryptkey($res,"8660281B6051D071D94B5B230549F9DC851566DC");
$enc = gnupg_encrypt($res, "just a test");
echo $enc;
?>
```

**Приклад #2 Приклад використання** gnupg\_encrypt()\*\* в об'єктно-орієнтованому стилі\*\*

```php
<?php
$gpg = new gnupg();
$gpg->addencryptkey("8660281B6051D071D94B5B230549F9DC851566DC");
$enc = $gpg->encrypt("just a test");
echo $enc;
?>
```
