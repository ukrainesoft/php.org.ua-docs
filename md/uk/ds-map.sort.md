---
navigation:
  - ds-map.slice.md: '« Ds\\Map::slice'
  - ds-map.sorted.md: 'Ds\\Map::sorted »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::sort'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::sort

(PECL ds >= 1.0.0)

Ds\\Map::sort — Сортує колекцію за значеннями

### Опис

```methodsynopsis
public Ds\Map::sort(callable $comparator = ?): void
```

Сортує колекцію за значеннями, необов'язково використовуючи callback-функцію `comparator`

### Список параметрів

`comparator`

Функція порівняння повинна повертати ціле, яке менше, дорівнює чи більше нуля, якщо перший аргумент є відповідно меншим, рівним чи більшим, ніж другий.

```methodsynopsis
callback(mixed $a, mixed $b): int
```

**Застереження**

Возвращение*нецілих* значень з функції порівняння, таких як число з плаваючою точкою (float), призведе до внутрішнього приведення значення callback-функції, що повертається, до цілого числа (int). Таким чином, значення `0.99`и`0.1` будуть приведені до цілого значення що дозволить порівняти ці значення як рівні.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** Ds\\Map::sort()\*\*\*\*

```php
<?php
$map = new \Ds\Map(["a" => 2, "b" => 3, "c" => 1]);
$map->sort();

print_r($map);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => c
            [value] => 1
        )

    [1] => Ds\Pair Object
        (
            [key] => a
            [value] => 2
        )

    [2] => Ds\Pair Object
        (
            [key] => b
            [value] => 3
        )

)
```

**Приклад #2 Приклад використання** Ds\\Map::sort()\*\* з callback-функцією порівняння\*\*

```php
<?php
$map = new \Ds\Map(["a" => 2, "b" => 3, "c" => 1]);

$map->sort(function($a, $b) {
    return $b <=> $a;
});

print_r($map);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => b
            [value] => 3
        )

    [1] => Ds\Pair Object
        (
            [key] => a
            [value] => 2
        )

    [2] => Ds\Pair Object
        (
            [key] => c
            [value] => 1
        )

)
```
