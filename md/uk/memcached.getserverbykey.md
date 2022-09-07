---
navigation:
  - memcached.getresultmessage.md: '« Memcached::getResultMessage'
  - memcached.getserverlist.md: 'Memcached::getServerList »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::getServerByKey'
---
# Memcached::getServerByKey

(PECL memcached >= 0.1.0)

Memcached::getServerByKey — Отримує інформацію про сервер за ключом

### Опис

```methodsynopsis
public Memcached::getServerByKey(string $server_key): array
```

**Memcached::getServerByKey()** повертає інформацію про сервер, який можна вибрати за допомогою спеціального параметра `server_key`, який використовується в **Memcached::ByKey()** функціях.

### Список параметрів

`server_key`

Ключ, що ідентифікує сервер, де зберігається значення. Замість хешування за ключем самого елемента, ми хешуємо по ключу сервера при виборі сервера, що підключається, memcached. Цей підхід дозволяє групувати зв'язані елементи разом на одному сервері, що покращує ефективність групових операцій.

### Значення, що повертаються

Повертає масив, що містить такі ключі: `host` `port`, і `weight` у разі успішного виконання або **`false`** у разі невдачі. Використовуйте за необхідності [Memcached::getResultCode()](memcached.getresultcode.md)

### Приклади

**Приклад #1 Приклад використання **Memcached::getServerByKey()****

```php
<?php
$m = new Memcached();
$m->addServers(array(
    array('mem1.domain.com', 11211, 40),
    array('mem2.domain.com', 11211, 40),
    array('mem3.domain.com', 11211, 20),
));

$m->setOption(Memcached::OPT_LIBKETAMA_COMPATIBLE, true);

var_dump($m->getServerByKey('user'));
var_dump($m->getServerByKey('log'));
var_dump($m->getServerByKey('ip'));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(3) {
  ["host"]=>
  string(15) "mem3.domain.com"
  ["port"]=>
  int(11211)
  ["weight"]=>
  int(20)
}
array(3) {
  ["host"]=>
  string(15) "mem2.domain.com"
  ["port"]=>
  int(11211)
  ["weight"]=>
  int(40)
}
array(3) {
  ["host"]=>
  string(15) "mem2.domain.com"
  ["port"]=>
  int(11211)
  ["weight"]=>
  int(40)
}
```
