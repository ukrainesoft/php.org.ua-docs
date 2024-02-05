---
navigation:
  - function.array-intersect-ukey.md: « array\_intersect\_ukey
  - function.array-is-list.md: array\_is\_list »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_intersect
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_intersect

(PHP 4 >= 4.0.1, PHP 5, PHP 7, PHP 8)

array\_intersect — Обчислює перетин масивів

### Опис

```methodsynopsis
array_intersect(array $array, array ...$arrays): array
```

Функция**array\_intersect()** повертає масив, що містить усі значення масиву `array`, що містяться у всіх аргументах. Зверніть увагу, що ключі зберігаються.

### Список параметрів

`array`

Основний масив, що перевіряється

`arrays`

Масиви, з якими йде порівняння значень

### Значення, що повертаються

Повертає масив, що містить усі значення параметра `array`, які існують у всіх переданих аргументах.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Тепер функцію можна викликати лише з одним параметром. Раніше потрібно не менше двох параметрів. |

### Приклади

**Приклад #1 Приклад використання функції** array\_intersect()\*\*\*\*

```php
<?php
$array1 = array("a" => "green", "red", "blue");
$array2 = array("b" => "green", "yellow", "red");
$result = array_intersect($array1, $array2);
print_r($result);
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [a] => green
    [0] => red
)
```

### Примітки

> **Зауваження**: Два елементи визнаються однаковими тоді і лише тоді, коли вираз `(string) $elem1 === (string) $elem2` істинно. Простіше кажучи: коли їх рядкові уявлення ідентичні.

### Дивіться також

-   [array\_intersect\_assoc()](function.array-intersect-assoc.md) \- обчислює перетин масивів з додатковою перевіркою індексу
-   [array\_diff()](function.array-diff.md) \- обчислює розбіжність масивів
-   [array\_diff\_assoc()](function.array-diff-assoc.md) \- обчислює розбіжність масивів з додатковою перевіркою індексу
