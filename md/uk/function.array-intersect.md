Обчислює сходження масивів

-   [« array\_intersect\_ukey](function.array-intersect-ukey.html)
    
-   [array\_is\_list »](function.array-is-list.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с массивами](ref.array.html)
    
-   Обчислює сходження масивів
    

# arrayintersect

(PHP 4> = 4.0.1, PHP 5, PHP 7, PHP 8)

arrayintersect - Обчислює сходження масивів

### Опис

```methodsynopsis
array_intersect(array $array, array ...$arrays): array
```

Функція **arrayintersect()** повертає масив, що містить усі значення масиву `array`, що містяться у всіх аргументах. Зверніть увагу, що ключі зберігаються.

### Список параметрів

`array`

Основний масив, що перевіряється

`arrays`

Масиви, з якими йде порівняння значень

### Значення, що повертаються

Повертає масив, що містить усі значення `array`, які існують у всіх переданих аргументах.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція тепер може бути викликана лише з одним параметром. Раніше потрібно не менше двох параметрів. |

### Приклади

**Приклад #1 Приклад використання **arrayintersect()****

```php
<?php
$array1 = array("a" => "green", "red", "blue");
$array2 = array("b" => "green", "yellow", "red");
$result = array_intersect($array1, $array2);
print_r($result);
?>
```

Результат виконання цього прикладу:

```
Array
(
    [a] => green
    [0] => red
)
```

### Примітки

> **Зауваження**: Два елементи вважаються однаковими тоді і тільки тоді, коли `(string) $elem1 === (string) $elem2`. Інакше кажучи, коли їх рядкові уявлення ідентичні.

### Дивіться також

-   [array\_intersect\_assoc()](function.array-intersect-assoc.html) - обчислює сходження масивів з додатковою перевіркою індексу
-   [array\_diff()](function.array-diff.html) - Обчислити розбіжність масивів
-   [array\_diff\_assoc()](function.array-diff-assoc.html) - обчислює розбіжність масивів з додатковою перевіркою індексу