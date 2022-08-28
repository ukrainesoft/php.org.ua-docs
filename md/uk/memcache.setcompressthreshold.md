Увімкнути автоматичний стиск для великих значень

-   [« Memcache::set](memcache.set.html)
    
-   [Memcache::setServerParams »](memcache.setserverparams.html)
    
-   [PHP Manual](index.html)
    
-   [Memcache](class.memcache.html)
    
-   Увімкнути автоматичний стиск для великих значень
    

# Memcache::setCompressThreshold

(PECL memcache >= 2.0.0)

Memcache::setCompressThreshold — Увімкнути автоматичний стиск для великих значень.

### Опис

```methodsynopsis
Memcache::setCompressThreshold(int $threshold, float $min_savings = ?): bool
```

**Memcache::setCompressThreshold()** включає автоматичне стиск для великих значень. Ви також можете використати функцію **memcachesetcompressthreshold()**

> **Зауваження**
> 
> Ця функція була додана до Memcache версії 2.0.0.

### Список параметрів

`threshold`

Встановлює мінімальний розмір елементів для спроб автоматичного стиснення.

`min_saving`

Вказує мінімальний розмір заощадженого розміру. Передане значення має бути в межах від 0 до 1. Значення за умовчанням 0.2, що задає мінімальний розмір заощадженого розміру 20%.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Memcache::setCompressThreshold()****

```php
<?php

/* объектно-ориентированное API */

$memcache_obj = new Memcache;
$memcache_obj->addServer('memcache_host', 11211);
$memcache_obj->setCompressThreshold(20000, 0.2);

/* процедурное API */

$memcache_obj = memcache_connect('memcache_host', 11211);
memcache_set_compress_threshold($memcache_obj, 20000, 0.2);

?>
```