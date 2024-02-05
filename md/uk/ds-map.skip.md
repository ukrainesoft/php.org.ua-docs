---
navigation:
  - ds-map.reversed.md: '« Ds\\Map::reversed'
  - ds-map.slice.md: 'Ds\\Map::slice »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::skip'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::skip

(PECL ds >= 1.0.0)

Ds\\Map::skip — Повертає пару за індексом позиції

### Опис

```methodsynopsis
public Ds\Map::skip(int $position): Ds\Pair
```

Возвращает пару по индексу позиции`position`, перша пара має індекс 0

### Список параметрів

`position`

Індекс позиції.

### Значення, що повертаються

Повертає [Ds\\Pair](class.ds-pair.md) із заданої позиції `position`

### Помилки

Викидає виняток [OutOfRangeException](class.outofrangeexception.md)якщо індекс некоректний.

### Приклади

**Пример #1 Пример использования**Ds\\Map::skip()\*\*\*\*

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

var_dump($map->skip(1));
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(Ds\Pair)#2 (2) {
  ["key"]=>
  string(1) "b"
  ["value"]=>
  int(2)
}
```
