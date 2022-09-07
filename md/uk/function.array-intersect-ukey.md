---
navigation:
  - function.array-intersect-uassoc.md: « arrayintersectuassoc
  - function.array-intersect.md: arrayintersect »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: arrayintersectukey
---
# arrayintersectukey

(PHP 5> = 5.1.0, PHP 7, PHP 8)

arrayintersectukey - обчислює сходження масивів, використовуючи callback-функцію для порівняння ключів

### Опис

```methodsynopsis
array_intersect_ukey(array $array, array ...$arrays, callable $key_compare_func): array
```

**arrayintersectukey()** повертає масив, що містить значення `array`, що мають ключі, які містяться у всіх наступних параметрах.

### Список параметрів

`array`

Основний масив, що перевіряється.

`arrays`

Масиви, з якими порівнюються ключі.

`key_compare_func`

Функція порівняння повинна повертати ціле, яке менше, дорівнює чи більше нуля, якщо перший аргумент є відповідно меншим, рівним чи більшим, ніж другий.

```methodsynopsis
callback(mixed $a, mixed $b): int
```

### Значення, що повертаються

Повертає всі елементи `array`, чиї ключі існують у всіх переданих аргументах.

### Приклади

**Приклад #1 Приклад використання **arrayintersectukey()****

```php
<?php
function key_compare_func($key1, $key2)
{
    if ($key1 == $key2)
        return 0;
    else if ($key1 > $key2)
        return 1;
    else
        return -1;
}

$array1 = array('blue'  => 1, 'red'  => 2, 'green'  => 3, 'purple' => 4);
$array2 = array('green' => 5, 'blue' => 6, 'yellow' => 7, 'cyan'   => 8);

var_dump(array_intersect_ukey($array1, $array2, 'key_compare_func'));
?>
```

Результат виконання цього прикладу:

```
array(2) {
  ["blue"]=>
  int(1)
  ["green"]=>
  int(3)
}
```

У нашому прикладі лише ключі `'blue'` і `'green'` містяться в обох масивах і тому повертаються. Також зверніть увагу, що значення, що відповідають ключам `'blue'` і `'green'` відрізняються між масивами. Збіг все одно відбувається, оскільки порівнюються лише ключі. Значення, що повертаються, беруться з `array`

### Дивіться також

-   [arraydiff()](function.array-diff.md) - Обчислити розбіжність масивів
-   [arrayudiff()](function.array-udiff.md) - обчислює розбіжність масивів, використовуючи для порівняння callback-функцію
-   [arraydiffassoc()](function.array-diff-assoc.md) - обчислює розбіжність масивів з додатковою перевіркою індексу
-   [arraydiffuassoc()](function.array-diff-uassoc.md) - обчислює розбіжність масивів з додатковою перевіркою індексу, що здійснюється за допомогою callback-функції
-   [arrayudiffassoc()](function.array-udiff-assoc.md) - обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи порівняння значень callback-функцию
-   [arrayudiffuassoc()](function.array-udiff-uassoc.md) - обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи для порівняння значень та індексів callback-функцію
-   [arraydiffkey()](function.array-diff-key.md) - обчислює розбіжність масивів, порівнюючи ключі
-   [arraydiffukey()](function.array-diff-ukey.md) - обчислює розбіжність масивів, використовуючи callback-функцію для порівняння ключів
-   [arrayintersect()](function.array-intersect.md) - обчислює сходження масивів
-   [arrayintersectassoc()](function.array-intersect-assoc.md) - обчислює сходження масивів з додатковою перевіркою індексу
-   [arrayintersectuassoc()](function.array-intersect-uassoc.md) - обчислює сходження масивів з додатковою перевіркою індексу, що здійснюється за допомогою callback-функції
-   [arrayintersectkey()](function.array-intersect-key.md) - Обчислити перетин масивів, порівнюючи ключі
