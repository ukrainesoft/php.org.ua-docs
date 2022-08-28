Обчислює перетин масивів з додатковою перевіркою індексів, використовуючи для порівняння значень callback-функцію

-   [« array\_udiff](function.array-udiff.html)
    
-   [array\_uintersect\_uassoc »](function.array-uintersect-uassoc.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с массивами](ref.array.html)
    
-   Обчислює перетин масивів з додатковою перевіркою індексів, використовуючи для порівняння значень callback-функцію
    

# arrayuintersectassoc

(PHP 5, PHP 7, PHP 8)

arrayuintersectassoc - Обчислює перетин масивів з додатковою перевіркою індексів, використовуючи для порівняння значень callback-функцію

### Опис

```methodsynopsis
array_uintersect_assoc(array $array, array ...$arrays, callable $value_compare_func): array
```

Обчислює перетин масивів з додатковою перевіркою індексів, використовуючи для порівняння значень callback-функцію.

Зверніть увагу, що в порівнянні використовуються ключі, на відміну від [array\_uintersect()](function.array-uintersect.html). Значення порівнюються за допомогою callback-функції.

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
$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "GREEN", "B" => "brown", "yellow", "red");

print_r(array_uintersect_assoc($array1, $array2, "strcasecmp"));
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

-   [array\_uintersect()](function.array-uintersect.html) - обчислює перетин масивів, використовуючи для порівняння значень callback-функцію
-   [array\_intersect\_assoc()](function.array-intersect-assoc.html) - обчислює сходження масивів з додатковою перевіркою індексу
-   [array\_intersect\_uassoc()](function.array-intersect-uassoc.html) - обчислює сходження масивів з додатковою перевіркою індексу, що здійснюється за допомогою callback-функції
-   [array\_uintersect\_uassoc()](function.array-uintersect-uassoc.html) - обчислює перетин масивів з додатковою перевіркою індексу, використовуючи для порівняння індексів та значень індивідуальні callback-функції