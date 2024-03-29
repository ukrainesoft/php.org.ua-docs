---
navigation:
  - memcache.getstats.md: '« Memcache::getStats'
  - memcache.increment.md: 'Memcache::increment »'
  - index.md: PHP Manual
  - class.memcache.md: Memcache
title: 'Memcache::getVersion'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcache::getVersion

(PECL memcache >= 0.2.0)

Memcache::getVersion — Повернути версію сервера

### Опис

```methodsynopsis
Memcache::getVersion(): string|false
```

**Memcache::getVersion()** повертає рядок із номером версії сервера. Також можна використовувати функцію **memcache\_get\_version()**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок з номером версії сервера або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** Memcache::getVersion()\*\*\*\*

```php
<?php

/* объектно-ориентированное API */
$memcache = new Memcache;
$memcache->connect('memcache_host', 11211);
echo $memcache->getVersion();

/* процедурное API */
$memcache = memcache_connect('memcache_host', 11211);
echo memcache_get_version($memcache);

?>
```

### Дивіться також

-   [Memcache::getExtendedStats()](memcache.getextendedstats.md) \- Отримати статистику з усіх серверів у пулі
-   [Memcache::getStats()](memcache.getstats.md) \- Отримати статистику сервера
