---
navigation:
  - function.array-diff-key.html: « arraydiffkey
  - function.array-diff-ukey.html: arraydiffukey »
  - index.html: PHP Manual
  - ref.array.html: Функції для роботи з масивами
title: arraydiffuassoc
---
# arraydiffuassoc

(PHP 5, PHP 7, PHP 8)

arraydiffuassoc - Обчислює розбіжність масивів з додатковою перевіркою індексу, що здійснюється за допомогою callback-функції

### Опис

```methodsynopsis
array_diff_uassoc(array $array, array ...$arrays, callable $key_compare_func): array
```

Порівнює `array` з `arrays` та повертає різницю. На відміну від [arraydiff()](function.array-diff.html)для порівняння використовуються ключі.

На відміну від [arraydiffassoc()](function.array-diff-assoc.html), для порівняння ключів використовується функція користувача, а не вбудована.

### Список параметрів

`array`

Вихідний масив

`arrays`

Масиви, з якими йде порівняння

`key_compare_func`

Функція порівняння повинна повертати ціле, яке менше, дорівнює чи більше нуля, якщо перший аргумент є відповідно меншим, рівним чи більшим, ніж другий.

```methodsynopsis
callback(mixed $a, mixed $b): int
```

### Значення, що повертаються

Повертає масив (array), що містить усі елементи `array`, яких немає у всіх інших масивах.

### Приклади

**Приклад #1 Приклад використання **arraydiffuassoc()****

Пара `"a" => "green"` існує в обох масивах і тому відсутня у виведенні функції. Навпаки, пара `0 => "red"` перебуває у висновку функції, оскільки другий аргумент `"red"` має ключ, рівний `1`

```php
<?php
function key_compare_func($a, $b)
{
    if ($a === $b) {
        return 0;
    }
    return ($a > $b)? 1:-1;
}

$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "green", "yellow", "red");
$result = array_diff_uassoc($array1, $array2, "key_compare_func");
print_r($result);
?>
```

Результат виконання цього прикладу:

```
Array
(
    [b] => brown
    [c] => blue
    [0] => red
)
```

Рівність 2 індексів перевіряється функцією, що надається користувачем.

### Примітки

> **Зауваження**
> 
> Ця функція обробляє лише один вимір n-розмірного масиву. Звичайно, ви можете обробляти і більш глибокі рівні вкладеності, наприклад, використовуючи `array_diff_uassoc($array1[0], $array2[0], "key_compare_func");`

### Дивіться також

-   [arraydiff()](function.array-diff.html) - Обчислити розбіжність масивів
-   [arraydiffassoc()](function.array-diff-assoc.html) - обчислює розбіжність масивів з додатковою перевіркою індексу
-   [arrayudiff()](function.array-udiff.html) - обчислює розбіжність масивів, використовуючи для порівняння callback-функцію
-   [arrayudiffassoc()](function.array-udiff-assoc.html) - обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи порівняння значень callback-функцию
-   [arrayudiffuassoc()](function.array-udiff-uassoc.html) - обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи для порівняння значень та індексів callback-функцію
-   [arrayintersect()](function.array-intersect.html) - обчислює сходження масивів
-   [arrayintersectassoc()](function.array-intersect-assoc.html) - обчислює сходження масивів з додатковою перевіркою індексу
-   [arrayuintersect()](function.array-uintersect.html) - обчислює перетин масивів, використовуючи для порівняння значень callback-функцію
-   [arrayuintersectassoc()](function.array-uintersect-assoc.html) - обчислює перетин масивів з додатковою перевіркою індексів, використовуючи для порівняння значень callback-функцію
-   [arrayuintersectuassoc()](function.array-uintersect-uassoc.html) - обчислює перетин масивів з додатковою перевіркою індексу, використовуючи для порівняння індексів та значень індивідуальні callback-функції
