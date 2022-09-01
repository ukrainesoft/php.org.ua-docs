---
navigation:
  - function.mhash-count.html: « mhashcount
  - function.mhash-get-hash-name.html: mhashgethashname »
  - index.html: PHP Manual
  - ref.mhash.html: Функции Mhash
title: mhashgetblocksize
---
# mhashgetblocksize

(PHP 4, PHP 5, PHP 7, PHP 8)

mhashgetblocksize — Отримати розмір блоку для заданого хеша

**Увага**

Функція оголошена *застарілої*починаючи з PHP 8.1.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mhash_get_block_size(int $algo): int|false
```

Повертає розмір блоку для заданого `algo`

### Список параметрів

`algo`

Ідентифікатор хешу. Одна з констант **`MHASH_hashname`**

### Значення, що повертаються

Повертає розмір у байтах або **`false`**, якщо параметр `algo` заданий некоректно.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функцію оголошено застарілою. Використовуйте замість неї [функції`hash_*()`](ref.hash.html) |

### Приклади

**Приклад #1 Приклад використання **mhashgetblocksize()****

```php
<?php

echo mhash_get_block_size(MHASH_MD5); // 16

?>
```
