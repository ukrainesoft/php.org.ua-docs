---
navigation:
  - ds-map.reversed.md: '« DsMap::reversed'
  - ds-map.slice.md: 'ДсMap::slice »'
  - index.md: PHP Manual
  - class.ds-map.md: Коллекция пар ключ-значение
title: 'ДсMap::skip'
---
# ДсMap::skip

(PECL ds >= 1.0.0)

ДсMap::skip — Повертає пару за індексом позиції

### Опис

```methodsynopsis
public Ds\Map::skip(int $position): Ds\Pair
```

Повертає пару за індексом позиції `position`, перша пара має індекс 0

### Список параметрів

`position`

Індекс позиції.

### Значення, що повертаються

Повертає **ДсPair** із заданої позиції `position`

### Помилки

Викидає виняток [OutOfRangeException](class.outofrangeexception.md)якщо індекс некоректний.

### Приклади

**Приклад #1 Приклад використання **ДсMap::skip()****

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

var_dump($map->skip(1));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Pair)#2 (2) {
  ["key"]=>
  string(1) "b"
  ["value"]=>
  int(2)
}
```
