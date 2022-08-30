Отримати ім'я вказаного хеша

-   [« mhashgetblocksize](function.mhash-get-block-size.html)
    
-   [mhashkeygens2k »](function.mhash-keygen-s2k.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Mhash](ref.mhash.html)
    
-   Отримати ім'я вказаного хеша
    

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

| Версия | Описание                                                                                     |
|--------|----------------------------------------------------------------------------------------------|
|        | Функцію оголошено застарілою. Використовуйте замість неї [функції `hash_*()`](ref.hash.html) |

### Приклади

**Приклад #1 Приклад використання **mhashgethashname()****

```php
<?php

echo mhash_get_hash_name(MHASH_MD5); // MD5

?>
```