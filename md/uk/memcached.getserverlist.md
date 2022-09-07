---
navigation:
  - memcached.getserverbykey.md: '« Memcached::getServerByKey'
  - memcached.getstats.md: 'Memcached::getStats »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::getServerList'
---
# Memcached::getServerList

(PECL memcached >= 0.1.0)

Memcached::getServerList — Отримує список серверів у пулі

### Опис

```methodsynopsis
public Memcached::getServerList(): array
```

**Memcached::getServerList()** повертає список усіх серверів, які знаходяться у пулі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Список серверів у пулі.

### Приклади

**Приклад #1 Приклад використання **Memcached::getServerList()****

```php
<?php
$m = new Memcached();
$m->addServers(array(
    array('mem1.domain.com', 11211, 20),
    array('mem2.domain.com', 11311, 80),
));
var_dump($m->getServerList());
?>
```

Результат виконання цього прикладу:

```
array(2) {
  [0]=>
  array(3) {
    ["host"]=>
    string(15) "mem1.domain.com"
    ["port"]=>
    int(11211)
    ["weight"]=>
    int(20)
  }
  [1]=>
  array(3) {
    ["host"]=>
    string(15) "mem2.domain.com"
    ["port"]=>
    int(11311)
    ["weight"]=>
    int(80)
  }
}
```
