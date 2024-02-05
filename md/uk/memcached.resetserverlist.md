---
navigation:
  - memcached.replacebykey.md: '« Memcached::replaceByKey'
  - memcached.set.md: 'Memcached::set »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::resetServerList'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::resetServerList

(PECL memcached >= 2.0.0)

Memcached::resetServerList — Очищає список серверів

### Опис

```methodsynopsis
public Memcached::resetServerList(): bool
```

**Memcached::resetserverlist()** видаляє всі сервери memcache з пулу, роблячи його знову порожнім.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [Memcached::addServer()](memcached.addserver.md) \- Додає сервер у пул
-   [Memcached::addServers()](memcached.addservers.md) \- Додає кілька серверів у пул
