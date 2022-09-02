---
navigation:
  - function.array-uintersect-assoc.md: « arrayuintersectassoc
  - function.array-uintersect.md: arrayuintersect »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: arrayuintersectuassoc
---
# arrayuintersectuassoc

(PHP 5, PHP 7, PHP 8)

arrayuintersectuassoc - Обчислює перетин масивів з додатковою перевіркою індексу, використовуючи для порівняння індексів та значень індивідуальні callback-функції

### Опис

```methodsynopsis
array_uintersect_uassoc(    array $array1,    array ...$arrays,    callable $value_compare_func,    callable $key_compare_func): array
```

Обчислює перетин масивів з додатковою перевіркою індексу, використовуючи для порівняння ключів та значень різні callback-функції. Тобто значення порівнюються однією callback-функцією, а індекси іншою.

### Список параметрів

`array1`

Перший масив.

`arrays`

Додаткові масиви.

`value_compare_func`

Функція порівняння повинна повертати ціле, яке менше, дорівнює чи більше нуля, якщо перший аргумент є відповідно меншим, рівним чи більшим, ніж другий.

```methodsynopsis
callback(mixed $a, mixed $b): int
```

`key_compare_func`

Callback-функція порівняння ключів.

### Значення, що повертаються

Повертає масив, що містить усі елементи `array1`, які існують у всіх інших аргументах.

### Приклади

**Приклад #1 Приклад використання **arrayuintersectuassoc()****

```php
<?php
$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "GREEN", "B" => "brown", "yellow", "red");

print_r(array_uintersect_uassoc($array1, $array2, "strcasecmp", "strcasecmp"));
?>
```

Результат виконання цього прикладу:

```
Array
(
    [a] => green
    [b] => brown
)
```

### Дивіться також

-   [arrayuintersect()](function.array-uintersect.md) - обчислює перетин масивів, використовуючи для порівняння значень callback-функцію
-   [arrayintersectassoc()](function.array-intersect-assoc.md) - обчислює сходження масивів з додатковою перевіркою індексу
-   [arrayintersectuassoc()](function.array-intersect-uassoc.md) - обчислює сходження масивів з додатковою перевіркою індексу, що здійснюється за допомогою callback-функції
-   [arrayuintersectassoc()](function.array-uintersect-assoc.md) - обчислює перетин масивів з додатковою перевіркою індексів, використовуючи для порівняння значень callback-функцію
