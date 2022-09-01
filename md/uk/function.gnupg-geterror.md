---
navigation:
  - function.gnupg-getengineinfo.html: « gnupggetengineinfo
  - function.gnupg-geterrorinfo.html: gnupggeterrorinfo »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupggeterror
---
# gnupggeterror

(PECL gnupg >= 0.1)

gnupggeterror — Повертає текст повідомлення про помилку, якщо функція не була виконана

### Опис

```methodsynopsis
gnupg_geterror(resource $identifier): string
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupginit()](function.gnupg-init.md) або **gnupg**

### Значення, що повертаються

Повертає текст повідомлення про помилку, якщо сталася помилка, інакше повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **gnupggeterror()** у процедурному стилі**

```php
<?php
$res = gnupg_init();
echo gnupg_geterror($res);
?>
```

**Приклад #2 Приклад використання **gnupggeterror()** в об'єктно-орієнтованому стилі**

```php
<?php
$gpg = new gnupg();
echo $gpg->geterror();
?>
```
