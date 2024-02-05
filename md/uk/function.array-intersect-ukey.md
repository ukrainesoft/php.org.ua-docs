---
navigation:
  - function.array-intersect-uassoc.md: « array\_intersect\_uassoc
  - function.array-intersect.md: array\_intersect »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_intersect\_ukey
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_intersect\_ukey

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

array\_intersect\_ukey - обчислює перетин масивів, використовуючи callback-функцію для порівняння ключів

### Опис

```methodsynopsis
array_intersect_ukey(array $array, array ...$arrays, callable $key_compare_func): array
```

Функция**array\_intersect\_ukey()** повертає масив, що складається із значень масиву `array`ключі яких містяться у всіх аргументах.

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

**Застереження**

Возвращение*нецілих* значень з функції порівняння, таких як число з плаваючою точкою (float), призведе до внутрішнього приведення значення callback-функції, що повертається, до цілого числа (int). Таким чином, значення `0.99`и`0.1` будуть приведені до цілого значення що дозволить порівняти ці значення як рівні.

### Значення, що повертаються

Повертає асоціативний масив, що складається із значень масиву `array`, ключі яких містяться у всіх аргументах.

### Приклади

**Приклад #1 Приклад использования фукции**array\_intersect\_ukey()\*\*\*\*

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

Результат виконання наведеного прикладу:

```
array(2) {
  ["blue"]=>
  int(1)
  ["green"]=>
  int(3)
}
```

У нашому прикладі лише ключі `'blue'`и`'green'` містяться в обох масивах і тому повертаються. Зверніть увагу, що значення, які відповідають ключам `'blue'`и`'green'`, неоднакові у двох масивах. Збіг все одно є, тому що порівнюються лише ключі. Значення, що повертаються, беруться з масиву `array`

### Дивіться також

-   [array\_diff()](function.array-diff.md) \- обчислює розбіжність масивів
-   [array\_udiff()](function.array-udiff.md) \- обчислює розбіжність масивів, використовуючи для порівняння callback-функцію
-   [array\_diff\_assoc()](function.array-diff-assoc.md) \- обчислює розбіжність масивів з додатковою перевіркою індексу
-   [array\_diff\_uassoc()](function.array-diff-uassoc.md) \- Обчислює розбіжність масивів з додатковою перевіркою індексу через пользовательскую callback-функцію
-   [array\_udiff\_assoc()](function.array-udiff-assoc.md) \- обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи порівняння значень callback-функцию
-   [array\_udiff\_uassoc()](function.array-udiff-uassoc.md) \- обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи для порівняння значень та індексів callback-функцію
-   [array\_diff\_key()](function.array-diff-key.md) \- обчислює розбіжність масивів, порівнюючи ключі
-   [array\_diff\_ukey()](function.array-diff-ukey.md) \- обчислює розбіжність масивів, використовуючи callback-функцію для порівняння ключів
-   [array\_intersect()](function.array-intersect.md) \- обчислює перетин масивів
-   [array\_intersect\_assoc()](function.array-intersect-assoc.md) \- обчислює перетин масивів з додатковою перевіркою індексу
-   [array\_intersect\_uassoc()](function.array-intersect-uassoc.md) \- обчислює перетин масивів з додатковою перевіркою індексу, порівнюючи індекси через callback-функцію
-   [array\_intersect\_key()](function.array-intersect-key.md) \- обчислює перетин масивів, порівнюючи ключі
