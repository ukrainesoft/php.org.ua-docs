---
navigation:
  - function.array-uintersect-uassoc.md: « array\_uintersect\_uassoc
  - function.array-unique.md: array\_unique »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_uintersect
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_uintersect

(PHP 5, PHP 7, PHP 8)

array\_uintersect — Обчислює перетин масивів, використовуючи для порівняння значень callback-функцію

### Опис

```methodsynopsis
array_uintersect(array $array, array ...$arrays, callable $value_compare_func): array
```

Обчислює перетин масивів, використовуючи для порівняння значень callback-функцію.

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

Повертає масив (array), що містить елементи аргументу `array`які є в кожному іншому аргументі.

### Приклади

**Приклад #1 Приклад використання функції** array\_uintersect()\*\*\*\*

```php
<?php

$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "GREEN", "B" => "brown", "yellow", "red");

print_r(array_uintersect($array1, $array2, "strcasecmp"));

?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [a] => green
    [b] => brown
    [0] => red
)
```

### Дивіться також

-   [array\_intersect()](function.array-intersect.md) \- обчислює перетин масивів
-   [array\_intersect\_assoc()](function.array-intersect-assoc.md) \- обчислює перетин масивів з додатковою перевіркою індексу
-   [array\_uintersect\_assoc()](function.array-uintersect-assoc.md) \- обчислює перетин масивів з додатковою перевіркою індексів, використовуючи для порівняння значень callback-функцію
-   [array\_uintersect\_uassoc()](function.array-uintersect-uassoc.md) \- обчислює перетин масивів з додатковою перевіркою індексу, використовуючи для порівняння індексів та значень окремі callback-функції
