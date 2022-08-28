Сортує колекцію

-   [« Ds\\Sequence::slice](ds-sequence.slice.html)
    
-   [Ds\\Sequence::sorted »](ds-sequence.sorted.html)
    
-   [PHP Manual](index.html)
    
-   [Последовательность](class.ds-sequence.html)
    
-   Сортує колекцію
    

# ДсSequence::sort

(PECL ds >= 1.0.0)

ДсSequence::sort — Сортує колекцію

### Опис

```methodsynopsis
abstract public Ds\Sequence::sort(callable $comparator = ?): void
```

Сортує колекцію, опціонально використовуючи callback-функцію `comparator`

### Список параметрів

`comparator`

Функція порівняння повинна повертати ціле, яке менше, дорівнює чи більше нуля, якщо перший аргумент є відповідно меншим, рівним чи більшим, ніж другий.

```methodsynopsis
callback(mixed $a, mixed $b): int
```

**Застереження**

*Не ціле* значення, повернене з функції порівняння, такого як float, буде приведено до цілого числа (int). Отже значення типу 0.99 і 0.1 будуть наведені до 0, що означатиме рівність порівнюваних значень.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсSequence::sort()****

```php
<?php
$sequence = new \Ds\Vector([4, 5, 1, 3, 2]);
$sequence->sort();

print_r($sequence);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Vector Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
    [4] => 5
)
```

**Приклад #2 Приклад використання **ДсSequence::sort()** з callback-функцією порівняння**

```php
<?php
$sequence = new \Ds\Vector([4, 5, 1, 3, 2]);

$sequence->sort(function($a, $b) {
    return $b <=> $a;
});

print_r($sequence);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Vector Object
(
    [0] => 5
    [1] => 4
    [2] => 3
    [3] => 2
    [4] => 1
)
```