---
navigation:
  - function.gnupg-addencryptkey.md: « gnupg\_addencryptkey
  - function.gnupg-cleardecryptkeys.md: gnupg\_cleardecryptkeys »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupg\_addsignkey
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gnupg\_addsignkey

(PECL gnupg >= 0.5)

gnupg\_addsignkey — Додати ключ для підписання

### Опис

```methodsynopsis
gnupg_addsignkey(resource $identifier, string $fingerprint, string $passphrase = ?): bool
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.md)или**gnupg**

`fingerprint`

Відбиток ключа.

`passphrase`

Пароль.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Процедурний приклад використання **gnupg\_addsignkey()****

```php
<?php
$res = gnupg_init();
gnupg_addsignkey($res, "8660281B6051D071D94B5B230549F9DC851566DC", "test");
?>
```

**Приклад #2 Об'єктно-орієнтований приклад використання **gnupg\_addsignkey()****

```php
<?php
$gpg = new gnupg();
$gpg->addsignkey("8660281B6051D071D94B5B230549F9DC851566DC","test");
?>
```
