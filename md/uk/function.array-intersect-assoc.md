---
navigation:
  - function.array-flip.md: « array\_flip
  - function.array-intersect-key.md: array\_intersect\_key »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_intersect\_assoc
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_intersect\_assoc

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

array\_intersect\_assoc - Обчислює перетин масивів з додатковою перевіркою індексу

### Опис

```methodsynopsis
array_intersect_assoc(array $array, array ...$arrays): array
```

Функция**array\_intersect\_assoc()** повертає масив, що містить усі значення масиву `array`, що містяться у всіх переданих аргументах. Зверніть увагу, що порівнюються ключі, на відміну функції [array\_intersect()](function.array-intersect.md)

### Список параметрів

`array`

Основний масив, що перевіряється.

`arrays`

Масиви, з якими йде порівняння.

### Значення, що повертаються

Повертає асоціативний масив, що містить усі елементи масиву `array`, які існують у всіх переданих аргументах.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Тепер функцію можна викликати лише з одним параметром. Раніше потрібно не менше двох параметрів. |

### Приклади

**Приклад #1 Приклад використання функції** array\_intersect\_assoc()\*\*\*\*

```php
<?php
$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "green", "b" => "yellow", "blue", "red");
$result_array = array_intersect_assoc($array1, $array2);
print_r($result_array);
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [a] => green
)
```

У нашому прикладі видно, що тільки пара `"a" => "green"`міститься в обох масивах і таким чином повертається. Значення `"red"` не повертається, тому що в масиві $array1 його ключ - , в той час як ключ значення "red" у масиві $array2 - , а ключ`"b"` не повертається тому, що його значення різні у кожному масиві.

Два значения пар`key => value` визнаються рівними, тільки якщо вираз `(string) $elem1 === (string) $elem2` істинно. Простіше кажучи: коли їх рядкові уявлення ідентичні.

### Дивіться також

-   [array\_intersect()](function.array-intersect.md) \- обчислює перетин масивів
-   [array\_uintersect\_assoc()](function.array-uintersect-assoc.md) \- обчислює перетин масивів з додатковою перевіркою індексів, використовуючи для порівняння значень callback-функцію
-   [array\_intersect\_uassoc()](function.array-intersect-uassoc.md) \- обчислює перетин масивів з додатковою перевіркою індексу, порівнюючи індекси через callback-функцію
-   [array\_uintersect\_uassoc()](function.array-uintersect-uassoc.md) \- обчислює перетин масивів з додатковою перевіркою індексу, використовуючи для порівняння індексів та значень окремі callback-функції
-   [array\_diff()](function.array-diff.md) \- обчислює розбіжність масивів
-   [array\_diff\_assoc()](function.array-diff-assoc.md) \- обчислює розбіжність масивів з додатковою перевіркою індексу
