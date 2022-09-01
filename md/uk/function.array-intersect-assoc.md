---
navigation:
  - function.array-flip.html: « arrayflip
  - function.array-intersect-key.html: arrayintersectkey »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: arrayintersectassoc
---
# arrayintersectassoc

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

arrayintersectassoc - Обчислює сходження масивів з додатковою перевіркою індексу

### Опис

```methodsynopsis
array_intersect_assoc(array $array, array ...$arrays): array
```

Функція **arrayintersectassoc()** повертає масив, що містить усі значення масиву `array`, що містяться у всіх зазначених аргументах. Зауважте, що при порівнянні використовуються ключі, на відміну від функції [arrayintersect()](function.array-intersect.md)

### Список параметрів

`array`

Основний масив, що перевіряється.

`arrays`

Масиви, з якими йде порівняння.

### Значення, що повертаються

Повертає асоціативний масив, що містить усі елементи масиву `array`, які існують у всіх переданих аргументах.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція тепер може бути викликана лише з одним параметром. Раніше потрібно не менше двох параметрів. |

### Приклади

**Приклад #1 Приклад використання **arrayintersectassoc()****

```php
<?php
$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "green", "b" => "yellow", "blue", "red");
$result_array = array_intersect_assoc($array1, $array2);
print_r($result_array);
?>
```

Результат виконання цього прикладу:

```
Array
(
    [a] => green
)
```

У нашому прикладі видно, що тільки пара `"a" => "green"`міститься в обох масивах і таким чином повертається. Значення `"red"` не повертається, тому що в масиві $array1 його ключ - `0`, в той час як ключ значення "red" у масиві $array2 - `1`, а ключ `"b"` не повертається тому, що його значення різні у кожному масиві.

Два значення пар `key => value` вважаються рівними тільки, якщо `(string) $elem1 === (string) $elem2` . Іншими словами, застосовується сувора перевірка, що означає, що рядкові уявлення повинні бути однаковими.

### Дивіться також

-   [arrayintersect()](function.array-intersect.md) - обчислює сходження масивів
-   [arrayuintersectassoc()](function.array-uintersect-assoc.md) - обчислює перетин масивів з додатковою перевіркою індексів, використовуючи для порівняння значень callback-функцію
-   [arrayintersectuassoc()](function.array-intersect-uassoc.md) - обчислює сходження масивів з додатковою перевіркою індексу, що здійснюється за допомогою callback-функції
-   [arrayuintersectuassoc()](function.array-uintersect-uassoc.md) - обчислює перетин масивів з додатковою перевіркою індексу, використовуючи для порівняння індексів та значень індивідуальні callback-функції
-   [arraydiff()](function.array-diff.md) - Обчислити розбіжність масивів
-   [arraydiffassoc()](function.array-diff-assoc.md) - обчислює розбіжність масивів з додатковою перевіркою індексу
