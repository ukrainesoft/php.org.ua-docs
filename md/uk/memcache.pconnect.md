Відкриває постійне з'єднання з сервером memcached

-   [« Memcache::increment](memcache.increment.html)
    
-   [Memcache::replace »](memcache.replace.html)
    
-   [PHP Manual](index.html)
    
-   [Memcache](class.memcache.html)
    
-   Відкриває постійне з'єднання з сервером memcached
    

# Memcache::pconnect

(PECL memcache >= 0.4.0)

Memcache::pconnect — Відкриває постійне з'єднання з сервером memcached

### Опис

```methodsynopsis
Memcache::pconnect(string $host, int $port = ?, int $timeout = ?): mixed
```

**Memcache::pconnect()** аналогічна [Memcache::connect()](memcache.connect.html) з тією різницею, що з'єднання встановлюється незмінним. Це з'єднання не закривається після завершення виконання скрипту та функцією [Memcache::close()](memcache.close.html). Ви також можете використати функцію **memcachepconnect()**

### Список параметрів

`host`

Вказує на хост, на якому memcached прослуховує з'єднання. Цей параметр також може вказувати на інший транспорт, такий як `unix:///path/to/memcached.sock`, для використання сокетів домену UNIX, у цьому випадку `port` повинен встановлений у `0`

`port`

Вказує на порт, на якому memcached прослуховує з'єднання. Встановіть цей параметр на `0`коли використовуються сокети домену UNIX.

`timeout`

Значення в секундах, яке використовуватиметься для підключення до домену. Подумайте двічі, перш ніж змінювати значення за замовчуванням в 1 секунду - ви можете втратити всі переваги кешування, якщо з'єднання занадто повільне.

### Значення, що повертаються

Повертає об'єкт Memcache або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Memcache::pconnect()****

```php
<?php

/* процедурное API */
$memcache_obj = memcache_pconnect('memcache_host', 11211);

/* объектно-ориентированное API */
$memcache_obj = new Memcache;
$memcache_obj->pconnect('memcache_host', 11211);

?>
```

### Дивіться також

-   [Memcache::connect()](memcache.connect.html) - Відкриває з'єднання з сервером memcached