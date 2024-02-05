---
navigation:
  - function.gnupg-clearencryptkeys.md: « gnupg\_clearencryptkeys
  - function.gnupg-decrypt.md: gnupg\_decrypt »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupg\_clearsignkeys
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gnupg\_clearsignkeys

(PECL gnupg >= 0.5)

gnupg\_clearsignkeys — Видалення всіх ключів, які були встановлені для підписання раніше

### Опис

```methodsynopsis
gnupg_clearsignkeys(resource $identifier): bool
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.md)или**gnupg**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Процедурний приклад використання **gnupg\_clearsignkeys()****

```php
<?php
$res = gnupg_init();
gnupg_clearsignkeys($res);
?>
```

**Приклад #2 Об'єктно-орієнтований приклад використання **gnupg\_clearsignkeys()****

```php
<?php
$gpg = new gnupg();
$gpg->clearsignkeys();
?>
```
