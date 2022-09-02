---
navigation:
  - function.array-sum.md: « arraysum
  - function.array-udiff-uassoc.md: arrayudiffuassoc »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: arrayudiffassoc
---
# arrayudiffassoc

(PHP 5, PHP 7, PHP 8)

arrayudiffassoc - Обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи для порівняння значень callback-функцію

### Опис

```methodsynopsis
array_udiff_assoc(array $array, array ...$arrays, callable $value_compare_func): array
```

Обчислює розбіжність масивів з додатковою перевіркою індексів, використовуючи порівняння значень callback-функцию.

> **Зауваження**: Будь ласка, зверніть увагу, що ця функція обробляє лише один вимір багатовимірного масиву. Зрозуміло, ви можете обробити більше одного виміру, використовуючи, наприклад, `array_udiff_assoc($array1[0], $array2[0], "some_comparison_func");`

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

**arrayudiffassoc()** повертає масив (array), що містить усі елементи `array`, яких немає у якомусь із решти аргументів. Зверніть увагу, що на відміну від [arraydiff()](function.array-diff.md) і [arrayudiff()](function.array-udiff.md) у порівнянні використовуються ключі. Порівняння даних масиву здійснюється за допомогою callback-функції, наданої користувачем. У цьому сенсі поведінка цієї функції відрізняється від [arraydiffassoc()](function.array-diff-assoc.md), яка використовується вбудовану функцію для порівняння.

### Приклади

**Приклад #1 Приклад використання **arrayudiffassoc()****

```php
<?php
class cr {
    private $priv_member;
    function __construct($val)
    {
        $this->priv_member = $val;
    }

    static function comp_func_cr($a, $b)
    {
        if ($a->priv_member === $b->priv_member) return 0;
        return ($a->priv_member > $b->priv_member)? 1:-1;
    }
}

$a = array("0.1" => new cr(9), "0.5" => new cr(12), 0 => new cr(23), 1=> new cr(4), 2 => new cr(-15),);
$b = array("0.2" => new cr(9), "0.5" => new cr(22), 0 => new cr(3), 1=> new cr(4), 2 => new cr(-15),);

$result = array_udiff_assoc($a, $b, array("cr", "comp_func_cr"));
print_r($result);
?>
```

Результат виконання цього прикладу:

```
Array
(
    [0.1] => cr Object
        (
            [priv_member:private] => 9
        )

    [0.5] => cr Object
        (
            [priv_member:private] => 12
        )

    [0] => cr Object
        (
            [priv_member:private] => 23
        )
)
```

У прикладі вище ви бачите, що пара `"1" => new cr(4)` є в обох масивах і тому її немає у висновку функції.

### Дивіться також

-   [arraydiff()](function.array-diff.md) - Обчислити розбіжність масивів
-   [arraydiffassoc()](function.array-diff-assoc.md) - обчислює розбіжність масивів з додатковою перевіркою індексу
-   [arraydiffuassoc()](function.array-diff-uassoc.md) - обчислює розбіжність масивів з додатковою перевіркою індексу, що здійснюється за допомогою callback-функції
-   [arrayudiff()](function.array-udiff.md) - обчислює розбіжність масивів, використовуючи для порівняння callback-функцію
-   [arrayudiffuassoc()](function.array-udiff-uassoc.md) - обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи для порівняння значень та індексів callback-функцію
-   [arrayintersect()](function.array-intersect.md) - обчислює сходження масивів
-   [arrayintersectassoc()](function.array-intersect-assoc.md) - обчислює сходження масивів з додатковою перевіркою індексу
-   [arrayuintersect()](function.array-uintersect.md) - обчислює перетин масивів, використовуючи для порівняння значень callback-функцію
-   [arrayuintersectassoc()](function.array-uintersect-assoc.md) - обчислює перетин масивів з додатковою перевіркою індексів, використовуючи для порівняння значень callback-функцію
-   [arrayuintersectuassoc()](function.array-uintersect-uassoc.md) - обчислює перетин масивів з додатковою перевіркою індексу, використовуючи для порівняння індексів та значень індивідуальні callback-функції
