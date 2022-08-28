Повернути версію сервера

-   [« Memcache::getStats](memcache.getstats.html)
    
-   [Memcache::increment »](memcache.increment.html)
    
-   [PHP Manual](index.html)
    
-   [Memcache](class.memcache.html)
    
-   Повернути версію сервера
    

# Memcache::getVersion

(PECL memcache >= 0.2.0)

Memcache::getVersion — Повернути версію сервера

### Опис

```methodsynopsis
Memcache::getVersion(): string|false
```

**Memcache::getVersion()** повертає рядок із номером версії сервера. Також можна використовувати функцію **memcachegetversion()**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок з номером версії сервера або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Memcache::getVersion()****

```php
<?php

/* объектно-ориентированное API */
$memcache = new Memcache;
$memcache->connect('memcache_host', 11211);
echo $memcache->getVersion();

/* процедурное API */
$memcache = memcache_connect('memcache_host', 11211);
echo memcache_get_version($memcache);

?>
```

### Дивіться також

-   [Memcache::getExtendedStats()](memcache.getextendedstats.html) - Отримати статистику з усіх серверів у пулі
-   [Memcache::getStats()](memcache.getstats.html) - Отримати статистику сервера