---
navigation:
  - function.array-rand.md: « array\_rand
  - function.array-replace-recursive.md: array\_replace\_recursive »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_reduce
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_reduce

(PHP 4 >= 4.0.5, PHP 5, PHP 7, PHP 8)

array\_reduce - Ітеративно зменшує масив до єдиного значення, використовуючи callback-функцію

### Опис

```methodsynopsis
array_reduce(array $array, callable $callback, mixed $initial = null): mixed
```

**array\_reduce()** ітеративно застосовує callback-функцію `callback` до елементів масиву `array`и, таким образом, сводит массив к единственному значению.

### Список параметрів

`array`

Вхідний масив

`callback`

```methodsynopsis
callback(mixed $carry, mixed $item): mixed
```

`carry`

Містить результуюче значення попередньої ітерації; у разі першої ітерації містить значення параметра `initial`

`item`

Містить поточну ітерацію.

`initial`

Якщо передано необов'язковий параметр `initial`, то він буде використаний на початку процесу, або як остаточний результат у випадку порожнього масиву.

### Значення, що повертаються

Повертає значення, що вийшло.

Якщо масив порожній і не передано параметр `initial` **array\_reduce()** поверне **`null`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Тепер функція видасть помилку рівня **`E_WARNING`**, якщо параметр callback-функції, переданої у параметр `callback`, очікує на передачу значення за посиланням. |

### Приклади

**Пример #1 Пример использования**array\_reduce()\*\*\*\*

```php
<?php
function sum($carry, $item)
{
    $carry += $item;
    return $carry;
}

function product($carry, $item)
{
    $carry *= $item;
    return $carry;
}

$a = array(1, 2, 3, 4, 5);
$x = array();

var_dump(array_reduce($a, "sum")); // int(15)
var_dump(array_reduce($a, "product", 10)); // int(1200), потому что: 10*1*2*3*4*5
var_dump(array_reduce($x, "sum", "Нет данных")); // string(19) "Нет данных"
?>
```

### Дивіться також

-   [array\_filter()](function.array-filter.md) \- Фільтрує елементи масиву за допомогою callback-функції
-   [array\_map()](function.array-map.md) \- Застосовує callback-функцію до всіх елементів зазначених масивів
-   [array\_unique()](function.array-unique.md) \- Прибирає значення, що повторюються, з масиву
-   [array\_count\_values()](function.array-count-values.md) \- Підраховує кількість входжень кожного окремого значення у масиві
