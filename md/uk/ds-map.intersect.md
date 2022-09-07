---
navigation:
  - ds-map.hasvalue.md: '« DsMap::hasValue'
  - ds-map.isempty.md: 'ДсMap::isEmpty »'
  - index.md: PHP Manual
  - class.ds-map.md: Коллекция пар ключ-значение
title: 'ДсMap::intersect'
---
# ДсMap::intersect

(PECL ds >= 1.0.0)

ДсMap::intersect — Створює нову колекцію пар, створену перетином з іншою колекцією пар

### Опис

```methodsynopsis
public Ds\Map::intersect(Ds\Map $map): Ds\Map
```

Створює нову колекцію пар з поточної, що містить елементи, ключі яких присутні як у поточній колекції, так і переданій у параметрі `map`. Іншими словами, повертає копію поточної колекції, з якої видалено всі елементи, ключі яких відсутні в колекції `map`

`A ∩ B = {x : x ∈ A ∧ x ∈ B}`

> **Зауваження**
> 
> Значення беруться із поточної колекції пар.

### Список параметрів

`map`

Нова колекція типу Map.

### Значення, що повертаються

Перетин поточної колекції та переданої в `map`

### Також дивіться

-   [» Перетин](https://en.wikipedia.org/wiki/Intersection_(set_theory)) на Вікіпедія

### Приклади

**Приклад #1 Приклад використання **ДсMap::intersect()****

```php
<?php
$a = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
$b = new \Ds\Map(["b" => 4, "c" => 5, "d" => 6]);

var_dump($a->intersect($b));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Map)#3 (2) {
  [0]=>
  object(Ds\Pair)#4 (2) {
    ["key"]=>
    string(1) "b"
    ["value"]=>
    int(2)
  }
  [1]=>
  object(Ds\Pair)#5 (2) {
    ["key"]=>
    string(1) "c"
    ["value"]=>
    int(3)
  }
}
```
