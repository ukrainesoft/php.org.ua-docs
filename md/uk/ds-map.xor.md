---
navigation:
  - ds-map.values.md: '« Ds\\Map::values'
  - class.ds-pair.md: Ds\\Pair »
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::xor'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::xor

(PECL ds >= 1.0.0)

Ds\\Map::xor — Створює нову колекцію пар із елементів, які є в одній із колекцій, але не в обох одночасно

### Опис

```methodsynopsis
public Ds\Map::xor(Ds\Map $map): Ds\Map
```

Створює нову колекцію пар з елементів, ключі яких є в поточній колекції, або в переданій в `map`але не в обох одночасно.

`A ⊖ B = {x : x ∈ (A \ B) ∪ (B \ A)}`

### Список параметрів

`map`

Друга колекція пар.

### Значення, що повертаються

Нова колекція пар з елементів, ключі яких є в поточній колекції, або в переданій в `map`але не в обох одночасно.

### Дивіться також

-   [» Симетрична різниця](https://en.wikipedia.org/wiki/Symmetric_difference)в Вікіпедія

### Приклади

**Пример #1 Пример использования**Ds\\Map::xor()\*\*\*\*

```php
<?php
$a = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
$b = new \Ds\Map(["b" => 4, "c" => 5, "d" => 6]);

print_r($a->xor($b));
?>
```

Висновок наведеного прикладу буде схожим на:

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
            [key] => d
            [value] => 6
        )

)
```
