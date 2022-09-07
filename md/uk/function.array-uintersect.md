---
navigation:
  - function.array-uintersect-uassoc.md: « arrayuintersectuassoc
  - function.array-unique.md: arrayunique »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: arrayuintersect
---
# arrayuintersect

(PHP 5, PHP 7, PHP 8)

arrayuintersect - обчислює перетин масивів, використовуючи для порівняння значень callback-функцію

### Опис

```methodsynopsis
array_uintersect(array $array, array ...$arrays, callable $value_compare_func): array
```

Обчислює перетин масивів, використовуючи для порівняння значень callback-функцію.

### Список параметрів

`array`

Перший масив.

`arrays`

Масиви для порівняння.

`value_compare_func`

Функція порівняння повинна повертати ціле, яке менше, дорівнює чи більше нуля, якщо перший аргумент є відповідно меншим, рівним чи більшим, ніж другий.

```methodsynopsis
callback(mixed $a, mixed $b): int
```

### Значення, що повертаються

Повертає масив, що містить усі елементи `array`, які існують у всіх інших аргументах.

### Приклади

**Приклад #1 Приклад використання **arrayuintersect()****

```php
<?php
$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "GREEN", "B" => "brown", "yellow", "red");

print_r(array_uintersect($array1, $array2, "strcasecmp"));
?>
```

Результат виконання цього прикладу:

```
Array
(
    [a] => green
    [b] => brown
    [0] => red
)
```

### Дивіться також

-   [arrayintersect()](function.array-intersect.md) - обчислює сходження масивів
-   [arrayintersectassoc()](function.array-intersect-assoc.md) - обчислює сходження масивів з додатковою перевіркою індексу
-   [arrayuintersectassoc()](function.array-uintersect-assoc.md) - обчислює перетин масивів з додатковою перевіркою індексів, використовуючи для порівняння значень callback-функцію
-   [arrayuintersectuassoc()](function.array-uintersect-uassoc.md) - обчислює перетин масивів з додатковою перевіркою індексу, використовуючи для порівняння індексів та значень індивідуальні callback-функції
