---
navigation:
  - memcache.connect.md: '« Memcache::connect'
  - memcache.delete.md: 'Memcache::delete »'
  - index.md: PHP Manual
  - class.memcache.md: Memcache
title: 'Memcache::decrement'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcache::decrement

(PECL memcache >= 0.2.0)

Memcache::decrement — Декрементувати значення елемента

### Опис

```methodsynopsis
Memcache::decrement(string $key, int $value = 1): int|false
```

**Memcache::decrement()** зменшує значення елемента на величину `value`. Аналогічно [Memcache::increment()](memcache.increment.md), поточне значення елемента наводиться до числового і після цього віднімається `value`

> **Зауваження** :
> 
> Нове значення елемента не може бути меншим за нуль.

> **Зауваження** :
> 
> Не используйте**Memcache::decrement()** з елементами, які були збережені за допомогою стиснення, тому що відповідний виклик [Memcache::get()](memcache.get.md) обернеться невдачею.

**Memcache::decrement()** *не* створює елемент, якщо він раніше не існував. Також можна використовувати функцію **memcache\_decrement()**

### Список параметрів

`key`

Ключ елемента, що декрементується.

`value`

Зменшення елемента на величину `value`

### Значення, що повертаються

У разі успішного виконання повертає нове значення елемента або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** Memcache::decrement()\*\*\*\*

```php
<?php

/* процедурное API */
$memcache_obj = memcache_connect('memcache_host', 11211);
/* декрементировать на 2 */
$new_value = memcache_decrement($memcache_obj, 'test_item', 2);

/* объектно-ориентированное API */
$memcache_obj = new Memcache;
$memcache_obj->connect('memcache_host', 11211);
/* декрементировать на 3 */
$new_value = $memcache_obj->decrement('test_item', 3);
?>
```

### Дивіться також

-   [Memcache::increment()](memcache.increment.md) \- Збільшити значення елемента
-   [Memcache::replace()](memcache.replace.md) \- Замінити значення наявного елемента
