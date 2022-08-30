Функції зворотного дзвінка для результуючого набору

-   [« Функції зворотного виклику](memcached.callbacks.html)
    
-   [Функції зворотного виклику наскрізного читання кеша »](memcached.callbacks.read-through.html)
    
-   [PHP Manual](index.html)
    
-   [Опції зворотного дзвінка](memcached.callbacks.html)
    
-   Функції зворотного дзвінка для результуючого набору
    

## Функції зворотного дзвінка для результуючого набору

[callable](language.types.callable.html) для результуючого набору викликаються методами [Memcached::getDelayed()](memcached.getdelayed.html) або [Memcached::getDelayedBykey()](memcached.getdelayedbykey.html) для кожного елемента із результуючого набору. Функціям зворотного виклику передаються об'єкт Memcached та масив з інформацією про елемент. Ці функції нічого не винні повертати.

**Приклад #1 Приклад функції зворотного дзвінка**

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);
$items = array(
    'key1' => 'value1',
    'key2' => 'value2',
    'key3' => 'value3'
);
$m->setMulti($items);
$m->getDelayed(array('key1', 'key3'), true, 'result_cb');

function result_cb($memc, $item)
{
    var_dump($item);
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

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