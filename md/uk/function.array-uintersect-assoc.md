---
navigation:
  - function.array-udiff.md: « arrayudiff
  - function.array-uintersect-uassoc.md: arrayuintersectuassoc »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: arrayuintersectassoc
---
# arrayuintersectassoc

(PHP 5, PHP 7, PHP 8)

arrayuintersectassoc - Обчислює перетин масивів з додатковою перевіркою індексів, використовуючи для порівняння значень callback-функцію

### Опис

```methodsynopsis
array_uintersect_assoc(array $array, array ...$arrays, callable $value_compare_func): array
```

Обчислює перетин масивів з додатковою перевіркою індексів, використовуючи для порівняння значень callback-функцію.

Зверніть увагу, що в порівнянні використовуються ключі, на відміну від [arrayuintersect()](function.array-uintersect.md). Значення порівнюються за допомогою callback-функції.

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

**Приклад #1 Приклад використання **arrayuintersectassoc()****

```php
<?php
$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "GREEN", "B" => "brown", "yellow", "red");

print_r(array_uintersect_assoc($array1, $array2, "strcasecmp"));
?>
```

Результат виконання цього прикладу:

```
Array
(
    [a] => green
)
```

### Дивіться також

-   [arrayuintersect()](function.array-uintersect.md) - обчислює перетин масивів, використовуючи для порівняння значень callback-функцію
-   [arrayintersectassoc()](function.array-intersect-assoc.md) - обчислює сходження масивів з додатковою перевіркою індексу
-   [arrayintersectuassoc()](function.array-intersect-uassoc.md) - обчислює сходження масивів з додатковою перевіркою індексу, що здійснюється за допомогою callback-функції
-   [arrayuintersectuassoc()](function.array-uintersect-uassoc.md) - обчислює перетин масивів з додатковою перевіркою індексу, використовуючи для порівняння індексів та значень індивідуальні callback-функції
