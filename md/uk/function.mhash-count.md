---
navigation:
  - ref.mhash.html: « Функции Mhash
  - function.mhash-get-block-size.html: mhashgetblocksize »
  - index.html: PHP Manual
  - ref.mhash.html: Функции Mhash
title: mhashcount
---
# mhashcount

(PHP 4, PHP 5, PHP 7, PHP 8)

mhashcount — Отримати найбільш доступний ідентифікатор хешу

**Увага**

Функція оголошена *застарілої*починаючи з PHP 8.1.0. Використовувати цю функцію не рекомендується.

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

| Версия | Описание |
| --- | --- |
|  | Функцію оголошено застарілою. Використовуйте замість неї [функції`hash_*()`](ref.hash.html) |

### Приклади

**Приклад #1 Обхід усіх хешей**

```php
<?php

$nr = mhash_count();

for ($i = 0; $i <= $nr; $i++) {
    echo sprintf("Размер блока хеша %s - %d\n",
        mhash_get_hash_name($i),
        mhash_get_block_size($i));
}
?>
```
