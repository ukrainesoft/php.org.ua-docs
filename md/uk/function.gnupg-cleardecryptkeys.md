---
navigation:
  - function.gnupg-addsignkey.md: « gnupgaddsignkey
  - function.gnupg-clearencryptkeys.md: gnupgclearencryptkeys »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupgcleardecryptkeys
---
# gnupgcleardecryptkeys

(PECL gnupg >= 0.5)

gnupgcleardecryptkeys — Видалення всіх ключів, які були встановлені для розшифровки раніше

### Опис

```methodsynopsis
gnupg_cleardecryptkeys(resource $identifier): bool
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupginit()](function.gnupg-init.md) або **gnupg**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Процедурний приклад використання **gnupgcleardecryptkeys()****

```php
<?php
$res = gnupg_init();
gnupg_cleardecryptkeys($res);
?>
```

**Приклад #2 Об'єктно-орієнтований приклад використання **gnupgcleardecryptkeys()****

```php
<?php
$gpg = new gnupg();
$gpg->cleardecryptkeys();
?>
```
