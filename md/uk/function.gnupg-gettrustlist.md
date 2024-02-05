---
navigation:
  - function.gnupg-getprotocol.md: « gnupg\_getprotocol
  - function.gnupg-import.md: gnupg\_import »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupg\_gettrustlist
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gnupg\_gettrustlist

(PECL gnupg >= 0.5)

gnupg\_gettrustlist — Пошук довірчих елементів

### Опис

```methodsynopsis
gnupg_gettrustlist(resource $identifier, string $pattern): ?array
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.md)или**gnupg**

`pattern`

Вираз обмеження списку довірчих елементів лише тими, які відповідають шаблону.

### Значення, що повертаються

У разі успішного виконання, функція повертає масив довірчих елементів. У разі помилки функція повертає **`null`**

### Приклади

**Пример #1 Пример использования**gnupg\_gettrustlist()\*\* у процедурному стилі\*\*

```php
<?php
$res = gnupg_init();
$items = gnupg_gettrustlist($res);
print_r($items);
?>
```

**Пример #2 Пример использования**gnupg\_gettrustlist()\*\* в об'єктно-орієнтованому стилі\*\*

```php
<?php
$gpg = new gnupg();
$items = $gpg->gettrustlist();
print_r($items);
?>
```
