Отримати статистику з усіх серверів у пулі

-   [« Memcache::get](memcache.get.md)
    
-   [Memcache::getServerStatus »](memcache.getserverstatus.md)
    
-   [PHP Manual](index.md)
    
-   [Memcache](class.memcache.md)
    
-   Отримати статистику з усіх серверів у пулі
    

# Memcache::getExtendedStats

(PECL memcache >= 2.0.0)

Memcache::getExtendedStats — Отримати статистику з усіх серверів у пулі

### Опис

```methodsynopsis
Memcache::getExtendedStats(string $type = ?, int $slabid = ?, int $limit = 100): array
```

**Memcache::getExtendedStats()** повертає двовимірний асоціативний масив, що містить статистику сервера. Ключі масиву відповідають серверу host:port, а значення містять статистику по даному серверу. Якщо не вдалося отримати дані для будь-якого сервера, то відповідне значення буде виставлено в **`false`**. Ви також можете використати функцію **memcachegetextendedstats()**

> **Зауваження**
> 
> Ця функція була додана до Memcache версії 2.0.0.

### Список параметрів

`type`

Тип статистики для отримання. Коректні значення: reset, malloc, maps, cachedump, slabs, items, sizes. Відповідно до специфікації протоколу memcached, ці додаткові аргументи "можуть бути змінені для зручності розробників memcache".

`slabid`

Використовується спільно з `type` для вказівки, з якого slab-файлу робити вивантаження. Використовується тільки для налагодження. Команда cachedump намагається запустити сервер і повинна використовуватися лише для налагодження.

`limit`

Використовується разом з `type` для обмеження кількості записів, що витягуються.

**Увага**

Тип статистики cachedump був вилучений з демона memcached для безпеки.

### Значення, що повертаються

Повертає двовимірний асоціативний масив, що містить статистику серверів або **`false`** у разі невдачі.

### Приклади

**Приклад #1 Приклад використання **Memcache::getExtendedStats()****

```php
<?php
    $memcache_obj = new Memcache;
    $memcache_obj->addServer('memcache_host', 11211);
    $memcache_obj->addServer('failed_host', 11211);

    $stats = $memcache_obj->getExtendedStats();
    print_r($stats);
?>
```

Результат виконання цього прикладу:

```
Array
(
    [memcache_host:11211] => Array
        (
            [pid] => 3756
            [uptime] => 603011
            [time] => 1133810435
            [version] => 1.1.12
            [rusage_user] => 0.451931
            [rusage_system] => 0.634903
            [curr_items] => 2483
            [total_items] => 3079
            [bytes] => 2718136
            [curr_connections] => 2
            [total_connections] => 807
            [connection_structures] => 13
            [cmd_get] => 9748
            [cmd_set] => 3096
            [get_hits] => 5976
            [get_misses] => 3772
            [bytes_read] => 3448968
            [bytes_written] => 2318883
            [limit_maxbytes] => 33554432
        )

    [failed_host:11211] => false
)
```

### Дивіться також

-   [Memcache::getVersion()](memcache.getversion.md) - Повернути версію сервера
-   [Memcache::getStats()](memcache.getstats.md) - Отримати статистику сервера