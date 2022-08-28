Обчислює сходження масивів, використовуючи callback-функцію для порівняння ключів

-   [« array\_intersect\_uassoc](function.array-intersect-uassoc.html)
    
-   [array\_intersect »](function.array-intersect.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с массивами](ref.array.html)
    
-   Обчислює сходження масивів, використовуючи callback-функцію для порівняння ключів
    

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
function key_compare_func($key1, $key2)
{
    if ($key1 == $key2)
        return 0;
    else if ($key1 > $key2)
        return 1;
    else
        return -1;
}

$array1 = array('blue'  => 1, 'red'  => 2, 'green'  => 3, 'purple' => 4);
$array2 = array('green' => 5, 'blue' => 6, 'yellow' => 7, 'cyan'   => 8);

var_dump(array_intersect_ukey($array1, $array2, 'key_compare_func'));
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

-   [array\_diff()](function.array-diff.html) - Обчислити розбіжність масивів
-   [array\_udiff()](function.array-udiff.html) - обчислює розбіжність масивів, використовуючи для порівняння callback-функцію
-   [array\_diff\_assoc()](function.array-diff-assoc.html) - обчислює розбіжність масивів з додатковою перевіркою індексу
-   [array\_diff\_uassoc()](function.array-diff-uassoc.html) - обчислює розбіжність масивів з додатковою перевіркою індексу, що здійснюється за допомогою callback-функції
-   [array\_udiff\_assoc()](function.array-udiff-assoc.html) - обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи порівняння значень callback-функцию
-   [array\_udiff\_uassoc()](function.array-udiff-uassoc.html) - обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи для порівняння значень та індексів callback-функцію
-   [array\_diff\_key()](function.array-diff-key.html) - обчислює розбіжність масивів, порівнюючи ключі
-   [array\_diff\_ukey()](function.array-diff-ukey.html) - обчислює розбіжність масивів, використовуючи callback-функцію для порівняння ключів
-   [array\_intersect()](function.array-intersect.html) - обчислює сходження масивів
-   [array\_intersect\_assoc()](function.array-intersect-assoc.html) - обчислює сходження масивів з додатковою перевіркою індексу
-   [array\_intersect\_uassoc()](function.array-intersect-uassoc.html) - обчислює сходження масивів з додатковою перевіркою індексу, що здійснюється за допомогою callback-функції
-   [array\_intersect\_key()](function.array-intersect-key.html) - Обчислити перетин масивів, порівнюючи ключі