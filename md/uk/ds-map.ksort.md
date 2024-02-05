---
navigation:
  - ds-map.keys.md: '« Ds\\Map::keys'
  - ds-map.ksorted.md: 'Ds\\Map::ksorted »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::ksort'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::ksort

(PECL ds >= 1.0.0)

Ds\\Map::ksort — Сортує поточну колекцію за ключами

### Опис

```methodsynopsis
public Ds\Map::ksort(callable $comparator = ?): void
```

Сортує поточну колекцію за ключами, опціонально використовуючи callback-функцію `comparator` для порівняння елементів.

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

**Пример #1 Пример использования**Ds\\Map::ksort()\*\*\*\*

```php
<?php
$map = new \Ds\Map(["b" => 2, "c" => 3, "a" => 1]);
$map->ksort();

print_r($map);
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

**Пример #2 Пример использования**Ds\\Map::ksort()\*\* з callback-функцією порівняння\*\*

```php
<?php
$map = new \Ds\Map([1 => "x", 2 => "y", 0 => "z"]);

// Обратный порядок
$map->ksort(function($a, $b) {
    return $b <=> $a;
});

print_r($map);
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
