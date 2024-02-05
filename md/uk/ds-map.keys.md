---
navigation:
  - ds-map.jsonserialize.md: '« Ds\\Map::jsonSerialize'
  - ds-map.ksort.md: 'Ds\\Map::ksort »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::keys'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::keys

(PECL ds >= 1.0.0)

Ds\\Map::keys — Повертає набір ключів колекції

### Опис

```methodsynopsis
public Ds\Map::keys(): Ds\Set
```

Повертає набір ключів колекції зі збереженням їх порядку.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Коллекция[Ds\\Set](class.ds-set.md)містить всі ключі поточної колекції.

### Приклади

**Приклад #1 Приклад використання** Ds\\Map::keys()\*\*\*\*

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
var_dump($map->keys());
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(Ds\Set)#2 (3) {
  [0]=>
  string(1) "a"
  [1]=>
  string(1) "b"
  [2]=>
  string(1) "c"
}
```
