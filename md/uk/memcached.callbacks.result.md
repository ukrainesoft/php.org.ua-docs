---
navigation:
  - memcached.callbacks.md: « Функції зворотного виклику
  - memcached.callbacks.read-through.md: Функції зворотного виклику наскрізного читання кеша »
  - index.md: PHP Manual
  - memcached.callbacks.md: Функції зворотного дзвінка
title: Функції зворотного дзвінка для результуючого набору
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Функції зворотного дзвінка для результуючого набору

[callable](language.types.callable.md) для результуючого набору викликаються методами [Memcached::getDelayed()](memcached.getdelayed.md) або [Memcached::getDelayedBykey()](memcached.getdelayedbykey.md) для кожного елемента із результуючого набору. Функціям зворотного виклику передаються об'єкт Memcached та масив з інформацією про елемент. Ці функції нічого не винні повертати.

**Приклад #1 Приклад функції зворотного дзвінка**

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);
$items = array(
    'key1' => 'value1',
    'key2' => 'value2',
    'key3' => 'value3'
);
$m->setMulti($items);
$m->getDelayed(array('key1', 'key3'), true, 'result_cb');

function result_cb($memc, $item)
{
    var_dump($item);
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(3) {
  ["key"]=>
  string(4) "key1"
  ["value"]=>
  string(6) "value1"
  ["cas"]=>
  float(49)
}
array(3) {
  ["key"]=>
  string(4) "key3"
  ["value"]=>
  string(6) "value3"
  ["cas"]=>
  float(50)
}
```
