---
navigation:
  - function.gnupg-clearsignkeys.md: « gnupg\_clearsignkeys
  - function.gnupg-decryptverify.md: gnupg\_decryptverify »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupg\_decrypt
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gnupg\_decrypt

(PECL gnupg >= 0.1)

gnupg\_decrypt — Розшифровує переданий текст

### Опис

```methodsynopsis
gnupg_decrypt(resource $identifier, string $text): string|false
```

Розшифровує переданий текст ключами, встановленими раніше за допомогою [gnupg\_adddecryptkey](function.gnupg-adddecryptkey.md)

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.md)или**gnupg**

`text`

Текст, що розшифровується.

### Значення, що повертаються

У разі успішного виконання ця функція повертає розшифрований текст. У разі виникнення помилки ця функція повертає **`false`**

### Приклади

**Приклад #1 Процедурний приклад використання **gnupg\_decrypt()****

```php
<?php
$res = gnupg_init();
gnupg_adddecryptkey($res, "8660281B6051D071D94B5B230549F9DC851566DC", "test");
$plain = gnupg_decrypt($res,$encrypted_text);
echo $plain;
?>
```

**Приклад #2 Об'єктно-орієнтований приклад використання **gnupg\_decrypt()****

```php
<?php
$gpg = new gnupg();
$gpg->adddecryptkey("8660281B6051D071D94B5B230549F9DC851566DC","test");
$plain = $gpg->decrypt($encrypted_text);
echo $plain;
?>
```
