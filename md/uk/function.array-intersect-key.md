---
navigation:
  - function.array-intersect-assoc.md: « array\_intersect\_assoc
  - function.array-intersect-uassoc.md: array\_intersect\_uassoc »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_intersect\_key
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_intersect\_key

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

array\_intersect\_key — обчислює перетин масивів, порівнюючи ключі

### Опис

```methodsynopsis
array_intersect_key(array $array, array ...$arrays): array
```

Функция**array\_intersect\_key()** повертає масив, що містить усі елементи масиву `array`, що мають ключі, що містяться у всіх інших параметрах.

### Список параметрів

`array`

Основний масив, що перевіряється.

`arrays`

Масив, з яким йде порівняння.

### Значення, що повертаються

Повертає асоціативний масив, що містить усі елементи масиву `array`, що мають ключі, що містяться у всіх інших параметрах.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Тепер функцію можна викликати лише з одним параметром. Раніше потрібно не менше двох параметрів. |

### Приклади

**Приклад #1 Приклад использования функции**array\_intersect\_key()\*\*\*\*

```php
<?php
$array1 = array('blue'  => 1, 'red'  => 2, 'green'  => 3, 'purple' => 4);
$array2 = array('green' => 5, 'blue' => 6, 'yellow' => 7, 'cyan'   => 8);

var_dump(array_intersect_key($array1, $array2));
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

У цьому прикладі тільки ключі `'blue'`и`'green'` містяться в обох масивах і тому повертаються. Зверніть увагу, що значення клюєм `'blue'`и`'green'` неоднакові у двох масивах. Збіг все одно є, тому що порівнюються лише ключі. Значення, що повертаються, беруться з масиву `array`

Два ключа пар`key => value` визнаються рівними, тільки якщо вираз `(string) $key1 === (string) $key2` істинно. Простіше кажучи, виконується строга перевірка рядкових уявлень, які мають бути однаковими.

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
-   [array\_intersect\_ukey()](function.array-intersect-ukey.md) \- обчислює перетин масивів, використовуючи callback-функцію для порівняння ключів
