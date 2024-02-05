---
navigation:
  - function.gnupg-encrypt.md: « gnupg\_encrypt
  - function.gnupg-export.md: gnupg\_export »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupg\_encryptsign
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gnupg\_encryptsign

(PECL gnupg >= 0.2)

gnupg\_encryptsign — Шифрує та підписує переданий текст

### Опис

```methodsynopsis
gnupg_encryptsign(resource $identifier, string $plaintext): string|false
```

Шифрує та підписує переданий у параметрі `plaintext` текст ключами, які були встановлені [gnupg\_addsignkey](function.gnupg-addsignkey.md) і [gnupg\_addencryptkey](function.gnupg-addencryptkey.md) раніше і повертає зашифрований та підписаний текст.

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.md)или**gnupg**

`plaintext`

Текст для шифрування.

### Значення, що повертаються

У разі успішного виконання ця функція повертає зашифрований та підписаний текст. У разі помилки ця функція повертає **`false`**

### Приклади

**Приклад #1 Процедурний приклад використання **gnupg\_encryptsign()****

```php
<?php
$res = gnupg_init();
gnupg_addencryptkey($res, "8660281B6051D071D94B5B230549F9DC851566DC");
gnupg_addsignkey($res, "8660281B6051D071D94B5B230549F9DC851566DC", "test");
$enc = gnupg_encryptsign($res, "просто тест");
echo $enc;
?>
```

**Приклад #2 Об'єктно-орієнтований приклад використання **gnupg\_encryptsign()****

```php
<?php
$gpg = new gnupg();
$gpg->addencryptkey("8660281B6051D071D94B5B230549F9DC851566DC");
$gpg->addsignkey("8660281B6051D071D94B5B230549F9DC851566DC","test");
$enc = $gpg->encryptsign("just a test");
echo $enc;
?>
```
