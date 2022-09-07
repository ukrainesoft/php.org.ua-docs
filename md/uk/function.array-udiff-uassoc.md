---
navigation:
  - function.array-udiff-assoc.md: « arrayudiffassoc
  - function.array-udiff.md: arrayudiff »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: arrayudiffuassoc
---
# arrayudiffuassoc

(PHP 5, PHP 7, PHP 8)

arrayudiffuassoc - Обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи для порівняння значень та індексів callback-функцію

### Опис

```methodsynopsis
array_udiff_uassoc(    array $array,    array ...$arrays,    callable $value_compare_func,    callable $key_compare_func): array
```

Обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи для порівняння значень та індексів callback-функцію.

Зверніть увагу, що для порівняння використовуються ключі, на відміну від [arraydiff()](function.array-diff.md) і [arrayudiff()](function.array-udiff.md)

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

`key_compare_func`

Порівняння ключів (індексів) також здійснюється за допомогою callback-функції `key_compare_func`. Це відрізняється від поведінки [arrayudiffassoc()](function.array-udiff-assoc.md)яка порівнює індекси за допомогою вбудованої функції.

### Значення, що повертаються

Повертає масив (array), що містить усі елементи `array`, яких немає у якомусь із інших аргументів.

### Приклади

**Приклад #1 Приклад використання **arrayudiffuassoc()****

```php
<?php
class cr {
    private $priv_member;
    function __construct($val)
    {
        $this->priv_member = $val;
    }

    static function comp_func_cr($a, $b)
    {
        if ($a->priv_member === $b->priv_member) return 0;
        return ($a->priv_member > $b->priv_member)? 1:-1;
    }

    static function comp_func_key($a, $b)
    {
        if ($a === $b) return 0;
        return ($a > $b)? 1:-1;
    }
}
$a = array("0.1" => new cr(9), "0.5" => new cr(12), 0 => new cr(23), 1=> new cr(4), 2 => new cr(-15),);
$b = array("0.2" => new cr(9), "0.5" => new cr(22), 0 => new cr(3), 1=> new cr(4), 2 => new cr(-15),);

$result = array_udiff_uassoc($a, $b, array("cr", "comp_func_cr"), array("cr", "comp_func_key"));
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

У наведеному вище прикладі ви можете бачити, що пара `"1" => new cr(4)` є в обох масивах і тому відсутня у виведенні функції. Пам'ятайте, що потрібно використовувати дві функції зворотного дзвінка.

### Примітки

> **Зауваження**: Будь ласка, зверніть увагу, що ця функція обробляє лише один вимір багатовимірного масиву. Зрозуміло, ви можете обробити більше одного виміру, використовуючи `array_udiff_uassoc($array1[0], $array2[0], "data_compare_func", "key_compare_func");`

### Дивіться також

-   [arraydiff()](function.array-diff.md) - Обчислити розбіжність масивів
-   [arraydiffassoc()](function.array-diff-assoc.md) - обчислює розбіжність масивів з додатковою перевіркою індексу
-   [arrayudiff()](function.array-udiff.md) - обчислює розбіжність масивів, використовуючи для порівняння callback-функцію
-   [arrayudiffassoc()](function.array-udiff-assoc.md) - обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи порівняння значень callback-функцию
-   [arrayintersect()](function.array-intersect.md) - обчислює сходження масивів
-   [arrayintersectassoc()](function.array-intersect-assoc.md) - обчислює сходження масивів з додатковою перевіркою індексу
-   [arrayuintersect()](function.array-uintersect.md) - обчислює перетин масивів, використовуючи для порівняння значень callback-функцію
-   [arrayuintersectassoc()](function.array-uintersect-assoc.md) - обчислює перетин масивів з додатковою перевіркою індексів, використовуючи для порівняння значень callback-функцію
-   [arrayuintersectuassoc()](function.array-uintersect-uassoc.md) - обчислює перетин масивів з додатковою перевіркою індексу, використовуючи для порівняння індексів та значень індивідуальні callback-функції
