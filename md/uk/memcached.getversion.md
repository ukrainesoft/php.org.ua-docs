Отримує інформацію про версію серверів у пулі

-   [« Memcached::getStats](memcached.getstats.html)
    
-   [Memcached::increment »](memcached.increment.html)
    
-   [PHP Manual](index.html)
    
-   [Memcached](class.memcached.html)
    
-   Отримує інформацію про версію серверів у пулі
    

# Memcached::getVersion

(PECL memcached >= 0.1.5)

Memcached::getVersion — Отримує інформацію про версію серверів у пулі

### Опис

```methodsynopsis
public Memcached::getVersion(): array
```

**Memcached::getVersion()** повертає масив, що містить інформацію про версію кожного доступного сервера memcache.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Список масивів з інформацією про версію кожного сервера, де кожен елемент- окремий сервер.

### Приклади

**Приклад #1 Приклад використання **Memcached::getVersion()****

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

print_r($m->getVersion());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [localhost:11211] => 1.2.6
)
```