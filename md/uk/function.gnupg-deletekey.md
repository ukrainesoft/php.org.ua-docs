---
navigation:
  - function.gnupg-decryptverify.md: « gnupg\_decryptverify
  - function.gnupg-encrypt.md: gnupg\_encrypt »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupg\_deletekey
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gnupg\_deletekey

(PECL gnupg >= 0.5)

gnupg\_deletekey — Видаляє ключ зі зв'язування ключів

### Опис

```methodsynopsis
gnupg_deletekey(resource $identifier, string $key, bool $allow_secret): bool
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.md)или**gnupg**

`key`

Ключ для видалення.

`allow_secret`

Вказує, чи слід видаляти секретні ключі.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** gnupg\_deletekey()\*\* у процедурному стилі\*\*

```php
<?php
$res = gnupg_init();
gnupg_deletekey($res, "8660281B6051D071D94B5B230549F9DC851566DC");
?>
```

**Приклад #2 Приклад використання** gnupg\_deletekey()\*\* в об'єктно-орієнтованому стилі\*\*

```php
<?php
$gpg = new gnupg();
$gpg->deletekey("8660281B6051D071D94B5B230549F9DC851566DC");
?>
```
