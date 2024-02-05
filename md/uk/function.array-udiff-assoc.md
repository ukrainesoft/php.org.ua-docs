---
navigation:
  - function.array-sum.md: « array\_sum
  - function.array-udiff-uassoc.md: array\_udiff\_uassoc »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_udiff\_assoc
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_udiff\_assoc

(PHP 5, PHP 7, PHP 8)

array\_udiff\_assoc - Обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи для порівняння значень callback-функцію

### Опис

```methodsynopsis
array_udiff_assoc(array $array, array ...$arrays, callable $value_compare_func): array
```

Обчислює розбіжність масивів з додатковою перевіркою індексів, використовуючи порівняння значень callback-функцию.

> **Зауваження**: Зверніть увагу, що функція обробляє лише перший рівень багатовимірного масиву. Значення на вкладених рівнях обробляють, наприклад, так: `array_udiff_assoc($array1[0], $array2[0], "some_comparison_func");`

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

### Значення, що повертаються

Функция**array\_udiff\_assoc()** повертає масив (array), що містить елементи аргументу `array`, яких немає в жодному іншому аргументі. Зверніть увагу, що на відміну від функцій [array\_diff()](function.array-diff.md) і [array\_udiff()](function.array-udiff.md) при порівнянні значень порівнюються і ключі. Значення масиву порівнює задана користувачем callback-функція. У цій частині поведінка функції відрізняється від поведінки функції [array\_diff\_assoc()](function.array-diff-assoc.md)яка для порівняння працює з вбудованою функцією.

### Приклади

**Приклад #1 Приклад використання функції** array\_udiff\_assoc()\*\*\*\*

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
}

$a = array("0.1" => new cr(9), "0.5" => new cr(12), 0 => new cr(23), 1=> new cr(4), 2 => new cr(-15),);
$b = array("0.2" => new cr(9), "0.5" => new cr(22), 0 => new cr(3), 1=> new cr(4), 2 => new cr(-15),);

$result = array_udiff_assoc($a, $b, array("cr", "comp_func_cr"));
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

У наведеному прикладі видно, що пара `"1" => new cr(4)` є в обох масивах, і тому її немає у висновку функції.

### Дивіться також

-   [array\_diff()](function.array-diff.md) \- обчислює розбіжність масивів
-   [array\_diff\_assoc()](function.array-diff-assoc.md) \- обчислює розбіжність масивів з додатковою перевіркою індексу
-   [array\_diff\_uassoc()](function.array-diff-uassoc.md) \- Обчислює розбіжність масивів з додатковою перевіркою індексу через пользовательскую callback-функцію
-   [array\_udiff()](function.array-udiff.md) \- обчислює розбіжність масивів, використовуючи для порівняння callback-функцію
-   [array\_udiff\_uassoc()](function.array-udiff-uassoc.md) \- обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи для порівняння значень та індексів callback-функцію
-   [array\_intersect()](function.array-intersect.md) \- обчислює перетин масивів
-   [array\_intersect\_assoc()](function.array-intersect-assoc.md) \- обчислює перетин масивів з додатковою перевіркою індексу
-   [array\_uintersect()](function.array-uintersect.md) \- обчислює перетин масивів, використовуючи для порівняння значень callback-функцію
-   [array\_uintersect\_assoc()](function.array-uintersect-assoc.md) \- обчислює перетин масивів з додатковою перевіркою індексів, використовуючи для порівняння значень callback-функцію
-   [array\_uintersect\_uassoc()](function.array-uintersect-uassoc.md) \- обчислює перетин масивів з додатковою перевіркою індексу, використовуючи для порівняння індексів та значень окремі callback-функції
