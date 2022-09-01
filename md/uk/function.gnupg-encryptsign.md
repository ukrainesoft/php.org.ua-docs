---
navigation:
  - function.gnupg-encrypt.html: « gnupgencrypt
  - function.gnupg-export.html: gnupgexport »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupgencryptsign
---
# gnupgencryptsign

(PECL gnupg >= 0.2)

gnupgencryptsign — Шифрує та підписує переданий текст

### Опис

```methodsynopsis
gnupg_encryptsign(resource $identifier, string $plaintext): string
```

Шифрує та підписує переданий у параметрі `plaintext` текст ключами, які були встановлені [gnupgaddsignkey](function.gnupg-addsignkey.html) і [gnupgaddencryptkey](function.gnupg-addencryptkey.html) раніше і повертає зашифрований та підписаний текст.

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupginit()](function.gnupg-init.html) або **gnupg**

`plaintext`

Текст для шифрування.

### Значення, що повертаються

У разі успішного виконання, ця функція повертає зашифрований та підписаний текст. У разі помилки ця функція повертає **`false`**

### Приклади

**Приклад #1 Процедурний приклад використання **gnupgencryptsign()****

```php
<?php
$res = gnupg_init();
gnupg_addencryptkey($res, "8660281B6051D071D94B5B230549F9DC851566DC");
gnupg_addsignkey($res, "8660281B6051D071D94B5B230549F9DC851566DC", "test");
$enc = gnupg_encryptsign($res, "просто тест");
echo $enc;
?>
```

**Приклад #2 Об'єктно-орієнтований приклад використання **gnupgencryptsign()****

```php
<?php
$gpg = new gnupg();
$gpg->addencryptkey("8660281B6051D071D94B5B230549F9DC851566DC");
$gpg->addsignkey("8660281B6051D071D94B5B230549F9DC851566DC","test");
$enc = $gpg->encryptsign("just a test");
echo $enc;
?>
```
