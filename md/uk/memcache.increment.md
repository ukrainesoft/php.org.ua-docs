---
navigation:
  - memcache.getversion.md: '« Memcache::getVersion'
  - memcache.pconnect.md: 'Memcache::pconnect »'
  - index.md: PHP Manual
  - class.memcache.md: Memcache
title: 'Memcache::increment'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcache::increment

(PECL memcache >= 0.2.0)

Memcache::increment — Збільшити значення елемента

### Опис

```methodsynopsis
Memcache::increment(string $key, int $value = 1): int|false
```

**Memcache::increment()** збільшує значення елемента на величину `value`. Якщо елемент із зазначеним ключем `key` не числовий і не може бути приведений до числа, то його значення буде встановлено в `value`. . **Memcache::increment()** *не* створює елемент, якщо він раніше не існував.

> **Зауваження** :
> 
> Не используйте**Memcache::increment()** з елементами, які були збережені за допомогою стиснення, тому що відповідний виклик [Memcache::get()](memcache.get.md) обернеться невдачею.

Також можна використовувати функцію **memcache\_increment()**

### Список параметрів

`key`

Ключ елемент.

`value`

Увеличение значения на величину`value`

### Значення, що повертаються

У разі успішного виконання повертає нове значення елемента або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** Memcache::increment()\*\*\*\*

```php
<?php

/* процедурное API */
$memcache_obj = memcache_connect('memcache_host', 11211);
/* инкрементировать счётчик на 2 */
$current_value = memcache_increment($memcache_obj, 'counter', 2);

/* объектно-ориентированное API */
$memcache_obj = new Memcache;
$memcache_obj->connect('memcache_host', 11211);
/* инкрементировать счётчик на 3 */
$current_value = $memcache_obj->increment('counter', 3);

?>
```

### Дивіться також

-   [Memcache::decrement()](memcache.decrement.md) \- декрементувати значення елемента
-   [Memcache::replace()](memcache.replace.md) \- Замінити значення наявного елемента
