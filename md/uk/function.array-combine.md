Створює новий масив, використовуючи один масив як ключі, а інший для його значень

-   [« array\_column](function.array-column.html)
    
-   [array\_count\_values »](function.array-count-values.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с массивами](ref.array.html)
    
-   Створює новий масив, використовуючи один масив як ключі, а інший для його значень
    

# arraycombine

(PHP 5, PHP 7, PHP 8)

arraycombine — Створює новий масив, використовуючи один масив як ключі, а інший для його значень

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

Починаючи з PHP 8.0.0, видається помилка [ValueError](class.valueerror.html), якщо кількість елементів у `keys` і `values` не збігається. До PHP 8.0.0 натомість видавалася помилка рівня **`E_WARNING`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція **arraycombine()** тепер викидає помилку [ValueError](class.valueerror.html)якщо кількість елементів у масивах не збігається; раніше функція повертала значення **`false`** |

### Приклади

**Приклад #1 Простий приклад використання **arraycombine()****

```php
<?php
$a = array('green', 'red', 'yellow');
$b = array('avocado', 'apple', 'banana');
$c = array_combine($a, $b);

print_r($c);
?>
```

Результат виконання цього прикладу:

```
Array
(
    [green]  => avocado
    [red]    => apple
    [yellow] => banana
)
```

### Дивіться також

-   [array\_merge()](function.array-merge.html) - Зливає один або більше масивів
-   [array\_walk()](function.array-walk.html) - Застосовує задану користувачем функцію до кожного елемента масиву
-   [array\_values()](function.array-values.html) - Вибирає всі значення масиву