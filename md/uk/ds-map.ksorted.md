---
navigation:
  - ds-map.ksort.md: '« Ds\\Map::ksort'
  - ds-map.last.md: 'Ds\\Map::last »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::ksorted'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::ksorted

(No version information available, might only be in Git)

Ds\\Map::ksorted — Повертає копію колекції, відсортованої за ключами

### Опис

```methodsynopsis
public Ds\Map::ksorted(callable $comparator = ?): Ds\Map
```

Повертає копію колекції, відсортованої за ключами, опціонально використовуючи callback-функцію `comparator` для порівняння елементів.

### Список параметрів

`comparator`

Функція порівняння повинна повертати ціле, яке менше, дорівнює чи більше нуля, якщо перший аргумент є відповідно меншим, рівним чи більшим, ніж другий.

```methodsynopsis
callback(mixed $a, mixed $b): int
```

**Застереження**

Возвращение*нецілих* значень з функції порівняння, таких як число з плаваючою точкою (float), призведе до внутрішнього приведення значення callback-функції, що повертається, до цілого числа (int). Таким чином, значення `0.99`и`0.1` будуть приведені до цілого значення що дозволить порівняти ці значення як рівні.

### Значення, що повертаються

Повертає копію колекції відсортованої за ключами.

### Приклади

**Пример #1 Пример использования**Ds\\Map::ksorted()\*\*\*\*

```php
<?php
$map = new \Ds\Map(["b" => 2, "c" => 3, "a" => 1]);

print_r($map->ksorted());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Map Object
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
            [value] => 2
        )

    [2] => Ds\Pair Object
        (
            [key] => c
            [value] => 3
        )

)
```

**Пример #2 Пример использования**Ds\\Map::ksorted()\*\* з callback-функцією порівняння\*\*

```php
<?php
$map = new \Ds\Map([1 => "x", 2 => "y", 0 => "z"]);

// Обратный порядок
$sorted = $map->ksorted(function($a, $b) {
    return $b <=> $a;
});

print_r($sorted);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Map Object
Ds\Map Object
(
    [0] => Ds\Pair Object
        (
            [key] => 2
            [value] => y
        )

    [1] => Ds\Pair Object
        (
            [key] => 1
            [value] => x
        )

    [2] => Ds\Pair Object
        (
            [key] => 0
            [value] => z
        )

)
```
