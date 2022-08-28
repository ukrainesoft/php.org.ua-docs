Обчислити перетин масивів, порівнюючи ключі

-   [« array\_intersect\_assoc](function.array-intersect-assoc.html)
    
-   [array\_intersect\_uassoc »](function.array-intersect-uassoc.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с массивами](ref.array.html)
    
-   Обчислити перетин масивів, порівнюючи ключі
    

# arrayintersectkey

(PHP 5> = 5.1.0, PHP 7, PHP 8)

arrayintersectkey — Обчислити перетин масивів, порівнюючи ключі

### Опис

```methodsynopsis
array_intersect_key(array $array, array ...$arrays): array
```

**arrayintersectkey()** повертає масив, що містить усі елементи `array`, що мають ключі, які містяться у всіх наступних параметрах.

### Список параметрів

`array`

Основний масив, що перевіряється.

`arrays`

Масив, з яким йде порівняння.

### Значення, що повертаються

Повертає асоціативний масив, що містить усі елементи `array`, що мають ключі, що містяться у всіх інших параметрах.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція тепер може бути викликана лише з одним параметром. Раніше потрібно не менше двох параметрів. |

### Приклади

**Приклад #1 Приклад використання **arrayintersectkey()****

```php
<?php
$array1 = array('blue'  => 1, 'red'  => 2, 'green'  => 3, 'purple' => 4);
$array2 = array('green' => 5, 'blue' => 6, 'yellow' => 7, 'cyan'   => 8);

var_dump(array_intersect_key($array1, $array2));
?>
```

Результат виконання цього прикладу:

```
array(2) {
  ["blue"]=>
  int(1)
  ["green"]=>
  int(3)
}
```

У цьому прикладі тільки ключі `'blue'` і `'green'` містяться в обох масивах і тому повертаються. Також зверніть увагу, що значення, що відповідають ключам `'blue'` і `'green'`, Різні у вихідних масивах. Збіг все одно відбувається, оскільки порівнюються лише ключі. Значення, що повертаються, беруться з `array`

Два ключі пар `key => value` вважаються рівними, тільки якщо `(string) $key1 === (string) $key2` . Іншими словами, застосовується сувора перевірка, що означає, що строкові уявлення мають бути однаковими.

### Дивіться також

-   [array\_diff()](function.array-diff.html) - Обчислити розбіжність масивів
-   [array\_udiff()](function.array-udiff.html) - обчислює розбіжність масивів, використовуючи для порівняння callback-функцію
-   [array\_diff\_assoc()](function.array-diff-assoc.html) - обчислює розбіжність масивів з додатковою перевіркою індексу
-   [array\_diff\_uassoc()](function.array-diff-uassoc.html) - обчислює розбіжність масивів з додатковою перевіркою індексу, що здійснюється за допомогою callback-функції
-   [array\_udiff\_assoc()](function.array-udiff-assoc.html) - обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи порівняння значень callback-функцию
-   [array\_udiff\_uassoc()](function.array-udiff-uassoc.html) - обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи для порівняння значень та індексів callback-функцію
-   [array\_diff\_key()](function.array-diff-key.html) - обчислює розбіжність масивів, порівнюючи ключі
-   [array\_diff\_ukey()](function.array-diff-ukey.html) - обчислює розбіжність масивів, використовуючи callback-функцію для порівняння ключів
-   [array\_intersect()](function.array-intersect.html) - обчислює сходження масивів
-   [array\_intersect\_assoc()](function.array-intersect-assoc.html) - обчислює сходження масивів з додатковою перевіркою індексу
-   [array\_intersect\_uassoc()](function.array-intersect-uassoc.html) - обчислює сходження масивів з додатковою перевіркою індексу, що здійснюється за допомогою callback-функції
-   [array\_intersect\_ukey()](function.array-intersect-ukey.html) - обчислює сходження масивів, використовуючи callback-функцію для порівняння ключів