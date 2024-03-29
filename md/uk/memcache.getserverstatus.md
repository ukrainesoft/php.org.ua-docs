---
navigation:
  - memcache.getextendedstats.md: '« Memcache::getExtendedStats'
  - memcache.getstats.md: 'Memcache::getStats »'
  - index.md: PHP Manual
  - class.memcache.md: Memcache
title: 'Memcache::getServerStatus'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcache::getServerStatus

(PECL memcache >= 2.1.0)

Memcache::getServerStatus — Повертає статус сервера

### Опис

```methodsynopsis
Memcache::getServerStatus(string $host, int $port = 11211): int
```

**Memcache::getServerStatus()** повертає статус онлайн/офлайн-серверів. Ви також можете використати функцію **memcache\_get\_server\_status()**

> **Зауваження** :
> 
> Ця функція була додана до Memcache версії 2.1.0.

### Список параметрів

`host`

Вказує на хост, на якому memcached прослуховує з'єднання.

`port`

Вказує на порт, на якому memcached прослуховує з'єднання.

### Значення, що повертаються

Повертає статус серверів. 0, у разі виникнення помилки на сервері і значення, відмінне від нуля, інакше

### Приклади

**Приклад #1 Приклад використання** Memcache::getServerStatus()\*\*\*\*

```php
<?php

/* объектно-ориентированное API */
$memcache = new Memcache;
$memcache->addServer('memcache_host', 11211);
echo $memcache->getServerStatus('memcache_host', 11211);

/* процедурное API */
$memcache = memcache_connect('memcache_host', 11211);
echo memcache_get_server_status($memcache, 'memcache_host', 11211);

?>
```

### Дивіться також

-   [Memcache::addServer()](memcache.addserver.md) \- Додає сервер memcached в пул з'єднань
-   [Memcache::setServerParams()](memcache.setserverparams.md) \- Змінює параметри сервера та статус під час виконання
