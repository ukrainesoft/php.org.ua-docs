---
navigation:
  - ds-map.clear.html: '« DsMap::clear'
  - ds-map.copy.html: 'ДсMap::copy »'
  - index.md: PHP Manual
  - class.ds-map.html: Коллекция пар ключ-значение
title: 'ДсMap::construct'
---
# ДсMap::construct

(PECL ds >= 1.0.0)

ДсMap::construct — Створює новий екземпляр

### Опис

public **ДсMap::construct**[mixed](language.types.declarations.html#language.types.declarations.mixed) `...$values`

Створює новий екземпляр, використовуючи або об'єкт, що реалізує [traversable](class.traversable.md), або масив, переданий як параметр `values`

### Список параметрів

`values`

Об'єкт, що реалізує інтерфейс traversable або масив.

### Приклади

**Приклад #1 Приклад використання **ДсMap::construct()****

```php
<?php
$map = new \Ds\Map();
var_dump($map);

$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
var_dump($map);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Map)#1 (0) {
}
object(Ds\Map)#2 (3) {
  [0]=>
  object(Ds\Pair)#1 (2) {
    ["key"]=>
    string(1) "a"
    ["value"]=>
    int(1)
  }
  [1]=>
  object(Ds\Pair)#3 (2) {
    ["key"]=>
    string(1) "b"
    ["value"]=>
    int(2)
  }
  [2]=>
  object(Ds\Pair)#4 (2) {
    ["key"]=>
    string(1) "c"
    ["value"]=>
    int(3)
  }
}
```
