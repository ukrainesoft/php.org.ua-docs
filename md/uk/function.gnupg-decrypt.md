---
navigation:
  - function.gnupg-clearsignkeys.md: « gnupgclearsignkeys
  - function.gnupg-decryptverify.md: gnupgdecryptverify »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupgdecrypt
---
# gnupgdecrypt

(PECL gnupg >= 0.1)

gnupgdecrypt — Розшифровує переданий текст

### Опис

```methodsynopsis
gnupg_decrypt(resource $identifier, string $text): string
```

Розшифровує переданий текст ключами, встановленими раніше за допомогою [gnupgadddecryptkey](function.gnupg-adddecryptkey.md)

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupginit()](function.gnupg-init.md) або **gnupg**

`text`

Текст, що розшифровується.

### Значення, що повертаються

У разі успішного виконання ця функція повертає розшифрований текст. У разі виникнення помилки ця функція повертає **`false`**

### Приклади

**Приклад #1 Процедурний приклад використання **gnupgdecrypt()****

```php
<?php
$res = gnupg_init();
gnupg_adddecryptkey($res, "8660281B6051D071D94B5B230549F9DC851566DC", "test");
$plain = gnupg_decrypt($res,$encrypted_text);
echo $plain;
?>
```

**Приклад #2 Об'єктно-орієнтований приклад використання **gnupgdecrypt()****

```php
<?php
$gpg = new gnupg();
$gpg->adddecryptkey("8660281B6051D071D94B5B230549F9DC851566DC","test");
$plain = $gpg->decrypt($encrypted_text);
echo $plain;
?>
```
