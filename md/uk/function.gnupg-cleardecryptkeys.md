---
navigation:
  - function.gnupg-addsignkey.md: « gnupg\_addsignkey
  - function.gnupg-clearencryptkeys.md: gnupg\_clearencryptkeys »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupg\_cleardecryptkeys
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gnupg\_cleardecryptkeys

(PECL gnupg >= 0.5)

gnupg\_cleardecryptkeys — Видалення всіх ключів, які були встановлені для розшифровки раніше

### Опис

```methodsynopsis
gnupg_cleardecryptkeys(resource $identifier): bool
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.md)или**gnupg**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Процедурний приклад використання **gnupg\_cleardecryptkeys()****

```php
<?php
$res = gnupg_init();
gnupg_cleardecryptkeys($res);
?>
```

**Приклад #2 Об'єктно-орієнтований приклад використання **gnupg\_cleardecryptkeys()****

```php
<?php
$gpg = new gnupg();
$gpg->cleardecryptkeys();
?>
```
