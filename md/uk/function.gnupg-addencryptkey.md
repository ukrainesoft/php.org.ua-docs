---
navigation:
  - function.gnupg-adddecryptkey.md: « gnupg\_adddecryptkey
  - function.gnupg-addsignkey.md: gnupg\_addsignkey »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupg\_addencryptkey
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gnupg\_addencryptkey

(PECL gnupg >= 0.5)

gnupg\_addencryptkey — Додає ключ для шифрування

### Опис

```methodsynopsis
gnupg_addencryptkey(resource $identifier, string $fingerprint): bool
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.md)или**gnupg**

`fingerprint`

Відбиток ключа.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Процедурний приклад використання **gnupg\_addencryptkey()****

```php
<?php
$res = gnupg_init();
gnupg_addencryptkey($res, "8660281B6051D071D94B5B230549F9DC851566DC");
?>
```

**Приклад #2 Об'єктно-орієнтований приклад використання **gnupg\_addencryptkey()****

```php
<?php
$gpg = new gnupg();
$gpg->addencryptkey("8660281B6051D071D94B5B230549F9DC851566DC");
?>
```
