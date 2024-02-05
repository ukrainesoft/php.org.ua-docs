---
navigation:
  - ds-map.clear.md: '« Ds\\Map::clear'
  - ds-map.copy.md: 'Ds\\Map::copy »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::\_\_construct

(PECL ds >= 1.0.0)

Ds\\Map::\_\_construct — Створює новий екземпляр

### Опис

public **Ds\\Map::\_\_construct** [mixed](language.types.declarations.md#language.types.declarations.mixed) `...$values`) .

Створює новий екземпляр, використовуючи або об'єкт, що реалізує [traversable](class.traversable.md), або масив, переданий як параметр `values`

### Список параметрів

`values`

Об'єкт, що реалізує інтерфейс traversable або масив.

### Приклади

**Приклад #1 Приклад використання** Ds\\Map::\_\_construct()\*\*\*\*

```php
<?php
$map = new \Ds\Map();
var_dump($map);

$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
var_dump($map);
?>
```

Висновок наведеного прикладу буде схожим на:

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
