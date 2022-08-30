Обчислює сходження масивів з додатковою перевіркою індексу, що здійснюється за допомогою callback-функції

-   [« arrayintersectkey](function.array-intersect-key.html)
    
-   [arrayintersectukey »](function.array-intersect-ukey.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з масивами](ref.array.html)
    
-   Обчислює сходження масивів з додатковою перевіркою індексу, що здійснюється за допомогою callback-функції
    

# arrayintersectuassoc

(PHP 5, PHP 7, PHP 8)

arrayintersectuassoc - Обчислює сходження масивів з додатковою перевіркою індексу, що здійснюється за допомогою callback-функції

### Опис

```methodsynopsis
array_intersect_uassoc(array $array, array ...$arrays, callable $key_compare_func): array
```

**arrayintersectuassoc()** повертає масив, що містить значення `array`, що містяться у всіх наступних параметрах. Зверніть увагу, що на відміну від [arrayintersect()](function.array-intersect.html)для порівняння використовуються ключі.

### Список параметрів

`array`

Початковий порівнюваний масив

`arrays`

Масиви, з якими порівнюються ключі.

`key_compare_func`

Функція порівняння повинна повертати ціле, яке менше, дорівнює чи більше нуля, якщо перший аргумент є відповідно меншим, рівним чи більшим, ніж другий.

```methodsynopsis
callback(mixed $a, mixed $b): int
```

### Значення, що повертаються

Повертає всі елементи `array`чиї значення існують у всіх аргументах.

### Приклади

**Приклад #1 Приклад використання **arrayintersectuassoc()****

```php
<?php
$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "GREEN", "B" => "brown", "yellow", "red");

print_r(array_intersect_uassoc($array1, $array2, "strcasecmp"));
?>
```

Результат виконання цього прикладу:

```
Array
(
    [b] => brown
)
```

### Дивіться також

-   [arrayintersect()](function.array-intersect.html) - обчислює сходження масивів
-   [arrayintersectassoc()](function.array-intersect-assoc.html) - обчислює сходження масивів з додатковою перевіркою індексу
-   [arrayuintersectassoc()](function.array-uintersect-assoc.html) - обчислює перетин масивів з додатковою перевіркою індексів, використовуючи для порівняння значень callback-функцію
-   [arrayuintersectuassoc()](function.array-uintersect-uassoc.html) - обчислює перетин масивів з додатковою перевіркою індексу, використовуючи для порівняння індексів та значень індивідуальні callback-функції
-   [arrayintersectkey()](function.array-intersect-key.html) - Обчислити перетин масивів, порівнюючи ключі
-   [arrayintersectukey()](function.array-intersect-ukey.html) - обчислює сходження масивів, використовуючи callback-функцію для порівняння ключів