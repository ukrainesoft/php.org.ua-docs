---
navigation:
  - ds-map.ksorted.md: '« DsMap::ksorted'
  - ds-map.map.md: 'ДсMap::map »'
  - index.md: PHP Manual
  - class.ds-map.md: Коллекция пар ключ-значение
title: 'ДсMap::last'
---
# ДсMap::last

(PECL ds >= 1.0.0)

ДсMap::last — Повертає останню пару колекції

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

**Приклад #1 Приклад використання **ДсMap::last()****

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
var_dump($map->last());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Pair)#2 (2) {
  ["key"]=>
  string(1) "c"
  ["value"]=>
  int(3)
}
```
