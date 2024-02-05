---
navigation:
  - function.array-udiff-assoc.md: « array\_udiff\_assoc
  - function.array-udiff.md: array\_udiff »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_udiff\_uassoc
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_udiff\_uassoc

(PHP 5, PHP 7, PHP 8)

array\_udiff\_uassoc - Обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи для порівняння значень та індексів callback-функцію

### Опис

```methodsynopsis
array_udiff_uassoc(    array $array,    array ...$arrays,    callable $value_compare_func,    callable $key_compare_func): array
```

Обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи для порівняння значень та індексів callback-функцію.

Обратите внимание, что в отличие от функций[array\_diff()](function.array-diff.md) і [array\_udiff()](function.array-udiff.md) при порівнянні значень порівнюються і ключі.

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

**Застереження**

Возвращение*нецілих* значень з функції порівняння, таких як число з плаваючою точкою (float), призведе до внутрішнього приведення значення callback-функції, що повертається, до цілого числа (int). Таким чином, значення `0.99`и`0.1` будуть приведені до цілого значення що дозволить порівняти ці значення як рівні.

**Застереження**

Callback-функція сортування повинна обробляти будь-яке значення з будь-якого масиву у будь-якому порядку, незалежно від того, в якому порядку вони були надані спочатку. Причина цього у тому, кожен окремий масив спочатку сортується перед порівнянням коїться з іншими масивами. Наприклад:

```php
<?php

$arrayA = ["string", 1];
$arrayB = [["value" => 1]];
// $item1 and $item2 can be any of "string", 1 or ["value" => 1]
$compareFunc = static function ($item1, $item2) {
    $value1 = is_string($item1) ? strlen($item1) : (is_array($item1) ? $item1["value"] : $item1);
    $value2 = is_string($item2) ? strlen($item2) : (is_array($item2) ? $item2["value"] : $item2);
    return $value1 <=> $value2;
};

?>
```

`key_compare_func`

Порівняння ключів (індексів) виконується також callback-функцією `key_compare_func`. Ця поведінка відрізняється від поведінки функції [array\_udiff\_assoc()](function.array-udiff-assoc.md)яка порівнює індекси через внутрішню функцію.

### Значення, що повертаються

Повертає масив (array), що містить елементи аргументу `array`, яких немає в жодному іншому аргументі.

### Приклади

**Приклад #1 Приклад использования функции**array\_udiff\_uassoc()\*\*\*\*

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

Результат виконання наведеного прикладу:

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

У наведеному прикладі видно, що пара `"1" => new cr(4)` є в обох масивах, і тому її немає у висновку функції. Функція буде працювати лише тоді, коли їй надали дві функції зворотного дзвінка.

### Примітки

> **Зауваження**: Зверніть увагу, що функція обробляє лише перший рівень багатовимірного масиву. Значення на вкладених рівнях обробляють, наприклад, так: `array_udiff_uassoc($array1[0], $array2[0], "data_compare_func", "key_compare_func");`

### Дивіться також

-   [array\_diff()](function.array-diff.md) \- обчислює розбіжність масивів
-   [array\_diff\_assoc()](function.array-diff-assoc.md) \- обчислює розбіжність масивів з додатковою перевіркою індексу
-   [array\_udiff()](function.array-udiff.md) \- обчислює розбіжність масивів, використовуючи для порівняння callback-функцію
-   [array\_udiff\_assoc()](function.array-udiff-assoc.md) \- обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи порівняння значень callback-функцию
-   [array\_intersect()](function.array-intersect.md) \- обчислює перетин масивів
-   [array\_intersect\_assoc()](function.array-intersect-assoc.md) \- обчислює перетин масивів з додатковою перевіркою індексу
-   [array\_uintersect()](function.array-uintersect.md) \- обчислює перетин масивів, використовуючи для порівняння значень callback-функцію
-   [array\_uintersect\_assoc()](function.array-uintersect-assoc.md) \- обчислює перетин масивів з додатковою перевіркою індексів, використовуючи для порівняння значень callback-функцію
-   [array\_uintersect\_uassoc()](function.array-uintersect-uassoc.md) \- обчислює перетин масивів з додатковою перевіркою індексу, використовуючи для порівняння індексів та значень окремі callback-функції
