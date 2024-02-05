---
navigation:
  - function.gnupg-cleardecryptkeys.md: « gnupg\_cleardecryptkeys
  - function.gnupg-clearsignkeys.md: gnupg\_clearsignkeys »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupg\_clearencryptkeys
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gnupg\_clearencryptkeys

(PECL gnupg >= 0.5)

gnupg\_clearencryptkeys — Видалення всіх ключів, які були встановлені для шифрування раніше

### Опис

```methodsynopsis
gnupg_clearencryptkeys(resource $identifier): bool
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.md)или**gnupg**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Процедурний приклад використання **gnupg\_clearencryptkeys()****

```php
<?php
$res = gnupg_init();
gnupg_clearencryptkeys($res);
?>
```

**Приклад #2 Об'єктно-орієнтований приклад використання **gnupg\_clearencryptkeys()****

```php
<?php
$gpg = new gnupg();
$gpg->clearencryptkeys();
?>
```
