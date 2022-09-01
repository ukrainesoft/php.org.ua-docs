---
navigation:
  - function.gnupg-cleardecryptkeys.html: « gnupgcleardecryptkeys
  - function.gnupg-clearsignkeys.html: gnupgclearsignkeys »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupgclearencryptkeys
---
# gnupgclearencryptkeys

(PECL gnupg >= 0.5)

gnupgclearencryptkeys — Видалення всіх ключів, які були встановлені для шифрування раніше

### Опис

```methodsynopsis
gnupg_clearencryptkeys(resource $identifier): bool
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupginit()](function.gnupg-init.html) або **gnupg**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Процедурний приклад використання **gnupgclearencryptkeys()****

```php
<?php
$res = gnupg_init();
gnupg_clearencryptkeys($res);
?>
```

**Приклад #2 Об'єктно-орієнтований приклад використання **gnupgclearencryptkeys()****

```php
<?php
$gpg = new gnupg();
$gpg->clearencryptkeys();
?>
```
