---
navigation:
  - function.gnupg-decryptverify.md: « gnupgdecryptverify
  - function.gnupg-encrypt.md: gnupgencrypt »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupgdeletekey
---
# gnupgdeletekey

(PECL gnupg >= 0.5)

gnupgdeletekey — Видаляє ключ зі зв'язування ключів

### Опис

```methodsynopsis
gnupg_deletekey(resource $identifier, string $key, bool $allow_secret): bool
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupginit()](function.gnupg-init.md) або **gnupg**

`key`

Ключ для видалення.

`allow_secret`

Вказує, чи слід видаляти секретні ключі.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **gnupgdeletekey()** у процедурному стилі**

```php
<?php
$res = gnupg_init();
gnupg_deletekey($res, "8660281B6051D071D94B5B230549F9DC851566DC");
?>
```

**Приклад #2 Приклад використання **gnupgdeletekey()** в об'єктно-орієнтованому стилі**

```php
<?php
$gpg = new gnupg();
$gpg->deletekey("8660281B6051D071D94B5B230549F9DC851566DC");
?>
```
