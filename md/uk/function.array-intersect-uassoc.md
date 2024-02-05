---
navigation:
  - function.array-intersect-key.md: « array\_intersect\_key
  - function.array-intersect-ukey.md: array\_intersect\_ukey »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_intersect\_uassoc
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_intersect\_uassoc

(PHP 5, PHP 7, PHP 8)

array\_intersect\_uassoc - Обчислює перетин масивів з додатковою перевіркою індексу, порівнюючи індекси через callback-функцію

### Опис

```methodsynopsis
array_intersect_uassoc(array $array, array ...$arrays, callable $key_compare_func): array
```

Функция**array\_intersect\_uassoc()** повертає масив, що складається із значень масиву `array`, що містяться у всіх переданих аргументах. Зауважте, що, на відміну від функції [array\_intersect()](function.array-intersect.md), порівнюються ключі.

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

**Застереження**

Возвращение*нецілих* значень з функції порівняння, таких як число з плаваючою точкою (float), призведе до внутрішнього приведення значення callback-функції, що повертається, до цілого числа (int). Таким чином, значення `0.99`и`0.1` будуть приведені до цілого значення що дозволить порівняти ці значення як рівні.

### Значення, що повертаються

Повертає елементи масиву `array`, чиї значення містяться у всіх переданих аргументах.

### Приклади

**Пример #1 Пример использования функции**array\_intersect\_uassoc()\*\*\*\*

```php
<?php
$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "GREEN", "B" => "brown", "yellow", "red");

print_r(array_intersect_uassoc($array1, $array2, "strcasecmp"));
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [b] => brown
)
```

### Дивіться також

-   [array\_intersect()](function.array-intersect.md) \- обчислює перетин масивів
-   [array\_intersect\_assoc()](function.array-intersect-assoc.md) \- обчислює перетин масивів з додатковою перевіркою індексу
-   [array\_uintersect\_assoc()](function.array-uintersect-assoc.md) \- обчислює перетин масивів з додатковою перевіркою індексів, використовуючи для порівняння значень callback-функцію
-   [array\_uintersect\_uassoc()](function.array-uintersect-uassoc.md) \- обчислює перетин масивів з додатковою перевіркою індексу, використовуючи для порівняння індексів та значень окремі callback-функції
-   [array\_intersect\_key()](function.array-intersect-key.md) \- обчислює перетин масивів, порівнюючи ключі
-   [array\_intersect\_ukey()](function.array-intersect-ukey.md) \- обчислює перетин масивів, використовуючи callback-функцію для порівняння ключів
