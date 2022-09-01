---
navigation:
  - ds-map.filter.html: '« DsMap::filter'
  - ds-map.get.html: 'ДсMap::get »'
  - index.md: PHP Manual
  - class.ds-map.html: Коллекция пар ключ-значение
title: 'ДсMap::first'
---
# ДсMap::first

(PECL ds >= 1.0.0)

ДсMap::first — Повертає перший елемент колекції

### Опис

```methodsynopsis
public Ds\Map::first(): Ds\Pair
```

Повертає перший елемент колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перший елемент колекції.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо колекція порожня.

### Приклади

**Приклад #1 Приклад використання **ДсMap::first()****

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
var_dump($map->first());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Pair)#2 (2) {
  ["key"]=>
  string(1) "a"
  ["value"]=>
  int(1)
}
```
