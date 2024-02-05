---
navigation:
  - function.array-column.md: « array\_column
  - function.array-count-values.md: array\_count\_values »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_combine
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_combine

(PHP 5, PHP 7, PHP 8)

array\_combine — Створює новий масив, використовуючи один масив як ключі, а інший для його значень

### Опис

```methodsynopsis
array_combine(array $keys, array $values): array
```

Створює масив (array), використовуючи значення масиву `keys` як ключі та значення масиву `values` як відповідні значення.

### Список параметрів

`keys`

Масив ключів. Некоректні значення для ключів будуть перетворені на рядок (string).

`values`

Масив значень

### Значення, що повертаються

Повертає комбінований масив (array).

### Помилки

Починаючи з PHP 8.0.0, видається помилка [ValueError](class.valueerror.md), якщо кількість елементів у `keys`и`values` не збігається. До PHP 8.0.0 натомість видавалася помилка рівня **`E_WARNING`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функция**array\_combine()** тепер викидає помилку [ValueError](class.valueerror.md)якщо кількість елементів у масивах не збігається; раніше функція повертала значення **`false`** |

### Приклади

**Приклад #1 Простий приклад використання **array\_combine()****

```php
<?php
$a = array('green', 'red', 'yellow');
$b = array('avocado', 'apple', 'banana');
$c = array_combine($a, $b);

print_r($c);
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [green]  => avocado
    [red]    => apple
    [yellow] => banana
)
```

### Дивіться також

-   [array\_merge()](function.array-merge.md) \- Зливає один або більше масивів
-   [array\_walk()](function.array-walk.md) \- Застосовує задану користувачем функцію кожного елемента масиву
-   [array\_values()](function.array-values.md) \- Повертає всі значення масиву
-   [array\_map()](function.array-map.md) \- Застосовує callback-функцію до всіх елементів зазначених масивів
