Декрементувати значення елемента

-   [« Memcache::connect](memcache.connect.html)
    
-   [Memcache::delete »](memcache.delete.html)
    
-   [PHP Manual](index.html)
    
-   [Memcache](class.memcache.html)
    
-   Декрементувати значення елемента
    

# Memcache::decrement

(PECL memcache >= 0.2.0)

Memcache::decrement — Декрементувати значення елемента

### Опис

```methodsynopsis
Memcache::decrement(string $key, int $value = 1): int|false
```

**Memcache::decrement()** зменшує значення елемента на величину `value`. Аналогічно [Memcache::increment()](memcache.increment.html), поточне значення елемента наводиться до числового і після цього віднімається `value`

> **Зауваження**
> 
> Нове значення елемента не може бути меншим за нуль.

> **Зауваження**
> 
> Не використовуйте **Memcache::decrement()** з елементами, які були збережені за допомогою стиснення, тому що відповідний виклик [Memcache::get()](memcache.get.html) обернеться невдачею.

**Memcache::decrement()** *не* створює елемент, якщо він раніше не існував. Також можна використовувати функцію **memcachedecrement()**

### Список параметрів

`key`

Ключ елемента, що декрементується.

`value`

Зменшення елемента на величину `value`

### Значення, що повертаються

У разі успішного виконання повертає нове значення елемента або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Memcache::decrement()****

```php
<?php

/* процедурное API */
$memcache_obj = memcache_connect('memcache_host', 11211);
/* декрементировать на 2 */
$new_value = memcache_decrement($memcache_obj, 'test_item', 2);

/* объектно-ориентированное API */
$memcache_obj = new Memcache;
$memcache_obj->connect('memcache_host', 11211);
/* декрементировать на 3 */
$new_value = $memcache_obj->decrement('test_item', 3);
?>
```

### Дивіться також

-   [Memcache::increment()](memcache.increment.html) - Збільшити значення елемента
-   [Memcache::replace()](memcache.replace.html) - Замінити значення наявного елемента