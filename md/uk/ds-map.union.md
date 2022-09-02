---
navigation:
  - ds-map.toarray.md: '« DsMap::toArray'
  - ds-map.values.md: 'ДсMap::values »'
  - index.md: PHP Manual
  - class.ds-map.md: Коллекция пар ключ-значение
title: 'ДсMap::union'
---
# ДсMap::union

(PECL ds >= 1.0.0)

ДсMap::union — Створює нову колекцію пар із елементів двох колекцій

### Опис

```methodsynopsis
public Ds\Map::union(Ds\Map $map): Ds\Map
```

Створює нову колекцію пар, що містить пари поточної та переданої в `map` колекцій.

`A ∪ B = {x: x ∈ A ∨ x ∈ B}`

> **Зауваження**
> 
> У разі збігу ключів значення елементів будуть братися з переданої колекції.

### Список параметрів

`map`

Нова колекція для об'єднання з поточною.

### Значення, що повертаються

Нова колекція пар, що є об'єднанням поточної та переданої в `map`

### Також дивіться

-   [» Об'єднання](https://en.wikipedia.org/wiki/Union_(set_theory)) в Вікіпедія

### Приклади

**Приклад #1 Приклад використання **ДсMap::union()****

```php
<?php
$a = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
$b = new \Ds\Map(["b" => 3, "c" => 4, "d" => 5]);

print_r($a->union($b));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => a
            [value] => 1
        )

    [1] => Ds\Pair Object
        (
            [key] => b
            [value] => 3
        )

    [2] => Ds\Pair Object
        (
            [key] => c
            [value] => 4
        )

    [3] => Ds\Pair Object
        (
            [key] => d
            [value] => 5
        )

)
```
