---
navigation:
  - function.mhash-count.md: « mhash\_count
  - function.mhash-get-hash-name.md: mhash\_get\_hash\_name »
  - index.md: PHP Manual
  - ref.mhash.md: Функції Mhash
title: mhash\_get\_block\_size
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mhash\_get\_block\_size

(PHP 4, PHP 5, PHP 7, PHP 8)

mhash\_get\_block\_size — Отримати розмір блоку для заданого хеша

**Увага**

Функція оголошена *застарілої* починаючи з PHP 8.1.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mhash_get_block_size(int $algo): int|false
```

Повертає розмір блоку для заданого `algo`

### Список параметрів

`algo`

Идентификатор хеша. Одна из констант\*\*`MHASH_hashname`\*\*

### Значення, що повертаються

Повертає розмір у байтах або **`false`**, якщо параметр `algo`задан некорректно.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Функцію оголошено застарілою. Використовуйте замість неї [функції `hash_*()`](ref.hash.md) |

### Приклади

**Пример #1 Пример использования**mhash\_get\_block\_size()\*\*\*\*

```php
<?php

echo mhash_get_block_size(MHASH_MD5); // 16

?>
```
