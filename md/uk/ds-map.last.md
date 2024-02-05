---
navigation:
  - ds-map.ksorted.md: '« Ds\\Map::ksorted'
  - ds-map.map.md: 'Ds\\Map::map »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::last'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::last

(PECL ds >= 1.0.0)

Ds\\Map::last — Повертає останню пару колекції

### Опис

```methodsynopsis
public Ds\Map::last(): Ds\Pair
```

Повертає останню пару колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Останній елемент колекції.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо колекція порожня.

### Приклади

**Приклад #1 Приклад використання** Ds\\Map::last()\*\*\*\*

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
var_dump($map->last());
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(Ds\Pair)#2 (2) {
  ["key"]=>
  string(1) "c"
  ["value"]=>
  int(3)
}
```
