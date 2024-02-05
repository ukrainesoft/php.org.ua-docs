---
navigation:
  - ds-map.union.md: '« Ds\\Map::union'
  - ds-map.xor.md: 'Ds\\Map::xor »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::values'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::values

(PECL ds >= 1.0.0)

Ds\\Map::values ​​— Повертає послідовність значень колекції

### Опис

```methodsynopsis
public Ds\Map::values(): Ds\Sequence
```

Повертає послідовність значень колекції, зберігаючи їхній порядок.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Послідовність ([Ds\\Sequence](class.ds-sequence.md)), що містить усі значення колекції.

### Приклади

**Пример #1 Пример использования**Ds\\Map::values()\*\*\*\*

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
var_dump($map->values());
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(Ds\Vector)#2 (3) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
}
```
