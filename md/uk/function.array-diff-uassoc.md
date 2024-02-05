---
navigation:
  - function.array-diff-key.md: « array\_diff\_key
  - function.array-diff-ukey.md: array\_diff\_ukey »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_diff\_uassoc
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_diff\_uassoc

(PHP 5, PHP 7, PHP 8)

array\_diff\_uassoc — Обчислює розбіжність масивів з додатковою перевіркою індексу через пользовательскую callback-функцію

### Опис

```methodsynopsis
array_diff_uassoc(array $array, array ...$arrays, callable $key_compare_func): array
```

Порівнює значення масиву `array` зі значеннями масивів `arrays` та повертає різницю. У цій функції, на відміну від функції [array\_diff()](function.array-diff.md), ключі масиву також беруть участь у порівнянні.

В отличие от функции[array\_diff\_assoc()](function.array-diff-assoc.md), у цій функції ключі порівнюються спеціальною функцією зворотного виклику, а не вбудованою.

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

**Застереження**

Возвращение*нецілих* значень з функції порівняння, таких як число з плаваючою точкою (float), призведе до внутрішнього приведення значення callback-функції, що повертається, до цілого числа (int). Таким чином, значення `0.99`и`0.1` будуть приведені до цілого значення що дозволить порівняти ці значення як рівні.

### Значення, що повертаються

Повертає масив (array), що містить усі елементи масиву `array`, яких немає в інших порівнюваних масивах.

### Приклади

**Пример #1 Пример использования**array\_diff\_uassoc()\*\*\*\*

У цьому прикладі пара `"a" => "green"` існує в обох міститься в обох масивах, і тому її немає у висновку функції. Але пара `0 => "red"` міститься у виведенні функції, тому що значенням `"red"` у першому масиві автоматично надається ключ , а в другому масиві тому ж значенню буде надано ключ оскільки ключ уже занят значением`yellow`

```php
<?php
function key_compare_func($a, $b)
{
    if ($a === $b) {
        return 0;
    }
    return $a <=> $b;
}

$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "green", "yellow", "red");
$result = array_diff_uassoc($array1, $array2, "key_compare_func");
print_r($result);
?>
```

Результат виконання наведеного прикладу:

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

> **Зауваження** :
> 
> Ця функція перевіряє лише один рівень n-мірного масиву. Порівняти вкладені масиви можна, вказавши глибший рівень, наприклад: `array_diff_uassoc($array1[0], $array2[0], "key_compare_func");`

### Дивіться також

-   [array\_diff()](function.array-diff.md) \- обчислює розбіжність масивів
-   [array\_diff\_assoc()](function.array-diff-assoc.md) \- обчислює розбіжність масивів з додатковою перевіркою індексу
-   [array\_udiff()](function.array-udiff.md) \- обчислює розбіжність масивів, використовуючи для порівняння callback-функцію
-   [array\_udiff\_assoc()](function.array-udiff-assoc.md) \- обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи порівняння значень callback-функцию
-   [array\_udiff\_uassoc()](function.array-udiff-uassoc.md) \- обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи для порівняння значень та індексів callback-функцію
-   [array\_intersect()](function.array-intersect.md) \- обчислює перетин масивів
-   [array\_intersect\_assoc()](function.array-intersect-assoc.md) \- обчислює перетин масивів з додатковою перевіркою індексу
-   [array\_uintersect()](function.array-uintersect.md) \- обчислює перетин масивів, використовуючи для порівняння значень callback-функцію
-   [array\_uintersect\_assoc()](function.array-uintersect-assoc.md) \- обчислює перетин масивів з додатковою перевіркою індексів, використовуючи для порівняння значень callback-функцію
-   [array\_uintersect\_uassoc()](function.array-uintersect-uassoc.md) \- обчислює перетин масивів з додатковою перевіркою індексу, використовуючи для порівняння індексів та значень окремі callback-функції
