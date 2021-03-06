- [« Memcached::getServerByKey](memcached.getserverbykey.md)
- [Memcached::getStats »](memcached.getstats.md)

- [PHP Manual](index.md)
- [Memcached](class.memcached.md)
- Отримує список серверів у пулі

# Memcached::getServerList

(PECL memcached \>= 0.1.0)

Memcached::getServerList — Отримує список серверів у пулі

### Опис

public **Memcached::getServerList**(): array

**Memcached::getServerList()** повертає список усіх серверів, які
перебувають у пулі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Список серверів у пулі.

### Приклади

**Приклад #1 Приклад використання **Memcached::getServerList()****

` <?php$m = new Memcached();$m->addServers(array(    array('mem1.domain.com', 11211, 20),    array('mem2.domain.com', 1) ));var_dump($m->getServerList());?> `

Результат виконання цього прикладу:

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
