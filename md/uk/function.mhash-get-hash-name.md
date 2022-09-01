---
navigation:
  - function.mhash-get-block-size.html: « mhashgetblocksize
  - function.mhash-keygen-s2k.html: mhashkeygens2k »
  - index.md: PHP Manual
  - ref.mhash.md: Функции Mhash
title: mhashgethashname
---
# mhashgethashname

(PHP 4, PHP 5, PHP 7, PHP 8)

mhashgethashname — Отримати ім'я вказаного хеша

**Увага**

Функція оголошена *Застарілої*починаючи з PHP 8.1.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mhash_get_hash_name(int $algo): string|false
```

Повертає ім'я заданого `algo`

### Список параметрів

`algo`

Ідентифікатор хешу. Одна з констант **`MHASH_hashname`**

### Значення, що повертаються

Повертає рядок з назвою або \*\*`false`\*\*якщо такого хеша немає.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функцію оголошено застарілою. Використовуйте замість неї [функції`hash_*()`](ref.hash.md) |

### Приклади

**Приклад #1 Приклад використання **mhashgethashname()****

```php
<?php

echo mhash_get_hash_name(MHASH_MD5); // MD5

?>
```
