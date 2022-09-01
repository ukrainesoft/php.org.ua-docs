---
navigation:
  - function.gnupg-getprotocol.html: « gnupggetprotocol
  - function.gnupg-import.html: gnupgimport »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupggettrustlist
---
# gnupggettrustlist

(PECL gnupg >= 0.5)

gnupggettrustlist — Пошук довірчих елементів

### Опис

```methodsynopsis
gnupg_gettrustlist(resource $identifier, string $pattern): array
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupginit()](function.gnupg-init.html) або **gnupg**

`pattern`

Вираз обмеження списку довірчих елементів лише тими, які відповідають шаблону.

### Значення, що повертаються

У разі успішного виконання, функція повертає масив довірчих елементів. У разі помилки функція повертає **`null`**

### Приклади

**Приклад #1 Приклад використання **gnupggettrustlist()** у процедурному стилі**

```php
<?php
$res = gnupg_init();
$items = gnupg_gettrustlist($res);
print_r($items);
?>
```

**Приклад #2 Приклад використання **gnupggettrustlist()** в об'єктно-орієнтованому стилі**

```php
<?php
$gpg = new gnupg();
$items = $gpg->gettrustlist();
print_r($items);
?>
```
