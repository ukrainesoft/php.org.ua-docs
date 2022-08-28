Очищає список серверів

-   [« Memcached::replaceByKey](memcached.replacebykey.html)
    
-   [Memcached::set »](memcached.set.html)
    
-   [PHP Manual](index.html)
    
-   [Memcached](class.memcached.html)
    
-   Очищає список серверів
    

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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [Memcached::addServer()](memcached.addserver.html) - Додає сервер у пул
-   [Memcached::addServers()](memcached.addservers.html) - Додає кілька серверів у пул