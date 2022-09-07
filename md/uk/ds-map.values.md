---
navigation:
  - ds-map.union.md: '« DsMap::union'
  - ds-map.xor.md: 'ДсMap::xor »'
  - index.md: PHP Manual
  - class.ds-map.md: Коллекция пар ключ-значение
title: 'ДсMap::values'
---
# ДсMap::values

(PECL ds >= 1.0.0)

ДсMap::values ​​— Повертає послідовність значень колекції

### Опис

```methodsynopsis
public Ds\Map::values(): Ds\Sequence
```

Повертає послідовність значень колекції, зберігаючи їхній порядок.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Послідовність (**ДсSequence**), що містить усі значення колекції.

### Приклади

**Приклад #1 Приклад використання **ДсMap::values()****

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
var_dump($map->values());
?>
```

Результатом виконання цього прикладу буде щось подібне:

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
