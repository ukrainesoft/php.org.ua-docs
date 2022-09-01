---
navigation:
  - ds-map.jsonserialize.html: '« DsMap::jsonSerialize'
  - ds-map.ksort.html: 'ДсMap::ksort »'
  - index.md: PHP Manual
  - class.ds-map.html: Коллекция пар ключ-значение
title: 'ДсMap::keys'
---
# ДсMap::keys

(PECL ds >= 1.0.0)

ДсMap::keys — Повертає набір ключів колекції

### Опис

```methodsynopsis
public Ds\Map::keys(): Ds\Set
```

Повертає набір ключів колекції зі збереженням їх порядку.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Колекція **ДсSet**містить всі ключі поточної колекції.

### Приклади

**Приклад #1 Приклад використання **ДсMap::keys()****

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
var_dump($map->keys());
?>
```

Результатом виконання цього прикладу буде щось подібне:

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
