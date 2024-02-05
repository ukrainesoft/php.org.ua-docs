---
navigation:
  - ref.mhash.md: « Функції Mhash
  - function.mhash-get-block-size.md: mhash\_get\_block\_size »
  - index.md: PHP Manual
  - ref.mhash.md: Функції Mhash
title: mhash\_count
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mhash\_count

(PHP 4, PHP 5, PHP 7, PHP 8)

mhash\_count — Отримати найбільш доступний ідентифікатор хешу

**Увага**

Функція оголошена *застарілої* починаючи з PHP 8.1.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mhash_count(): int
```

Повертає найбільш доступний ідентифікатор хешу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Отримати найбільш доступний ідентифікатор хешу. Хеші нумеруються від 0 до цього ідентифікатора.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Функцію оголошено застарілою. Використовуйте замість неї [функції `hash_*()`](ref.hash.md) |

### Приклади

**Приклад #1 Обхід усіх хешей**

```php
<?php

$nr = mhash_count();

for ($i = 0; $i <= $nr; $i++) {
    echo sprintf("Размер блока хеша %s - %d\n",
        mhash_get_hash_name($i),
        mhash_get_block_size($i));
}
?>
```
