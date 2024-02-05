---
navigation:
  - function.mhash-get-block-size.md: « mhash\_get\_block\_size
  - function.mhash-keygen-s2k.md: mhash\_keygen\_s2k »
  - index.md: PHP Manual
  - ref.mhash.md: Функції Mhash
title: mhash\_get\_hash\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mhash\_get\_hash\_name

(PHP 4, PHP 5, PHP 7, PHP 8)

mhash\_get\_hash\_name — Отримати ім'я вказаного хеша

**Увага**

Функція оголошена *застарілої* починаючи з PHP 8.1.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mhash_get_hash_name(int $algo): string|false
```

Повертає ім'я заданого `algo`

### Список параметрів

`algo`

Идентификатор хеша. Одна из констант\*\*`MHASH_hashname`\*\*

### Значення, що повертаються

Повертає рядок з назвою або \*\*`false`\*\*якщо такого хеша немає.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Функцію оголошено застарілою. Використовуйте замість неї [функції `hash_*()`](ref.hash.md) |

### Приклади

**Приклад #1 Приклад використання** mhash\_get\_hash\_name()\*\*\*\*

```php
<?php

echo mhash_get_hash_name(MHASH_MD5); // MD5

?>
```
