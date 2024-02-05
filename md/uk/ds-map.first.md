---
navigation:
  - ds-map.filter.md: '« Ds\\Map::filter'
  - ds-map.get.md: 'Ds\\Map::get »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::first'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::first

(PECL ds >= 1.0.0)

Ds\\Map::first — Повертає перший елемент колекції

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

**Пример #1 Пример использования**Ds\\Map::first()\*\*\*\*

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
var_dump($map->first());
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(Ds\Pair)#2 (2) {
  ["key"]=>
  string(1) "a"
  ["value"]=>
  int(1)
}
```
