---
navigation:
  - memcached.getserverlist.html: '« Memcached::getServerList'
  - memcached.getversion.html: 'Memcached::getVersion »'
  - index.html: PHP Manual
  - class.memcached.html: Memcached
title: 'Memcached::getStats'
---
# Memcached::getStats

(PECL memcached >= 0.1.0)

Memcached::getStats — Отримує статистику про сервери в пулі

### Опис

```methodsynopsis
public Memcached::getStats(): array|false
```

**Memcached::getStats()** Повертає масив, що містить статистику всіх доступних memcache серверів. Ознайомтеся також із специфікацією [» memcache протоколу](https://github.com/memcached/memcached/blob/master/doc/protocol.txt) для отримання повної інформації щодо цієї статистики.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Список масивів зі статистикою по кожному серверу, де кожен елемент - окремий сервер або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Memcached::getStats()****

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

print_r($m->getStats());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [localhost:11211] => Array
        (
            [pid] => 4933
            [uptime] => 786123
            [threads] => 1
            [time] => 1233868010
            [pointer_size] => 32
            [rusage_user_seconds] => 0
            [rusage_user_microseconds] => 140000
            [rusage_system_seconds] => 23
            [rusage_system_microseconds] => 210000
            [curr_items] => 145
            [total_items] => 2374
            [limit_maxbytes] => 67108864
            [curr_connections] => 2
            [total_connections] => 151
            [connection_structures] => 3
            [bytes] => 20345
            [cmd_get] => 213343
            [cmd_set] => 2381
            [get_hits] => 204223
            [get_misses] => 9120
            [evictions] => 0
            [bytes_read] => 9092476
            [bytes_written] => 15420512
            [version] => 1.2.6
        )

)
```
