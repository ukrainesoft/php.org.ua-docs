---
navigation:
  - ds-map.hasvalue.md: '« Ds\\Map::hasValue'
  - ds-map.isempty.md: 'Ds\\Map::isEmpty »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::intersect'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::intersect

(PECL ds >= 1.0.0)

Ds\\Map::intersect — Створює нову колекцію пар, створену перетином з іншою колекцією пар

### Опис

```methodsynopsis
public Ds\Map::intersect(Ds\Map $map): Ds\Map
```

Створює нову колекцію пар з поточної, що містить елементи, ключі яких присутні як у поточній колекції, так і переданій у параметрі `map`. Іншими словами, повертає копію поточної колекції, з якої видалено всі елементи, ключі яких відсутні в колекції `map`

`A ∩ B = {x : x ∈ A ∧ x ∈ B}`

> **Зауваження** :
> 
> Значення беруться із поточної колекції пар.

### Список параметрів

`map`

Нова колекція типу Map.

### Значення, що повертаються

Перетин поточної колекції та переданої в `map`

### Дивіться також

-   [» Перетин](https://en.wikipedia.org/wiki/Intersection_(set_theory))на Вікіпедія

### Приклади

**Пример #1 Пример использования**Ds\\Map::intersect()\*\*\*\*

```php
<?php
$a = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
$b = new \Ds\Map(["b" => 4, "c" => 5, "d" => 6]);

var_dump($a->intersect($b));
?>
```

Висновок наведеного прикладу буде схожим на:

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
