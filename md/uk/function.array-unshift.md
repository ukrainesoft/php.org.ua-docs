---
navigation:
  - function.array-unique.html: « arrayunique
  - function.array-values.html: arrayvalues »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: arrayunshift
---
# arrayunshift

(PHP 4, PHP 5, PHP 7, PHP 8)

arrayunshift — Додає один або кілька елементів на початок масиву

### Опис

```methodsynopsis
array_unshift(array &$array, mixed ...$values): int
```

**arrayunshift()** додає передані як аргументи елементи на початок масиву `array`. Зауважте, що список елементів додається повністю, тобто порядок елементів зберігається. Усі числові ключі будуть змінені таким чином, що нумерація масиву буде починатися з нуля, тоді як рядкові ключі залишаться незмінними.

> **Зауваження**
> 
> Скидає внутрішній покажчик масиву перший елемент.

### Список параметрів

`array`

Вхідний масив

`values`

Значення додавання.

### Значення, що повертаються

Повертає нову кількість елементів у `array`

### список змін

| Версия | Описание |
| --- | --- |
|  | Тепер ця функція може бути викликана одним параметром. Раніше потрібно було мінімум два параметри. |

### Приклади

**Приклад #1 Приклад використання **arrayunshift()****

```php
<?php
$queue = array("orange", "banana");
array_unshift($queue, "apple", "raspberry");
print_r($queue);
?>
```

Результат виконання цього прикладу:

```
Array
(
    [0] => apple
    [1] => raspberry
    [2] => orange
    [3] => banana
)
```

### Дивіться також

-   [arrayshift()](function.array-shift.md) - Витягує перший елемент масиву
-   [arraypush()](function.array-push.md) - Додає один або кілька елементів у кінець масиву
-   [arraypop()](function.array-pop.md) - Витягує останній елемент масиву
