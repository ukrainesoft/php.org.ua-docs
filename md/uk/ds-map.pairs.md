---
navigation:
  - ds-map.merge.md: '« Ds\\Map::merge'
  - ds-map.put.md: 'Ds\\Map::put »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::pairs'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::pairs

(PECL ds >= 1.0.0)

Ds\\Map::pairs — Повертає послідовність, яка містить усі пари колекції.

### Опис

```methodsynopsis
public Ds\Map::pairs(): Ds\Sequence
```

Повертає [Ds\\Sequence](class.ds-sequence.md), що містить усі пари колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

[Ds\\Sequence](class.ds-sequence.md), що містить усі пари вихідної колекції.

### Приклади

**Пример #1 Пример использования**Ds\\Map::pairs()\*\*\*\*

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

var_dump($map->pairs());
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(Ds\Map)#8 (3) {
  [0]=>
  object(Ds\Pair)#5 (2) {
    ["key"]=>
    string(1) "a"
    ["value"]=>
    int(1)
  }
  [1]=>
  object(Ds\Pair)#6 (2) {
    ["key"]=>
    string(1) "b"
    ["value"]=>
    int(2)
  }
  [2]=>
  object(Ds\Pair)#7 (2) {
    ["key"]=>
    string(1) "c"
    ["value"]=>
    int(3)
  }
}
p
```
