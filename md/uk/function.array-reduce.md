---
navigation:
  - function.array-rand.md: « arrayrand
  - function.array-replace-recursive.md: arrayreplacerecursive »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: arrayreduce
---
# arrayreduce

(PHP 4> = 4.0.5, PHP 5, PHP 7, PHP 8)

arrayreduce - Ітеративно зменшує масив до єдиного значення, використовуючи callback-функцію

### Опис

```methodsynopsis
array_reduce(array $array, callable $callback, mixed $initial = null): mixed
```

**arrayreduce()** ітеративно застосовує callback-функцію `callback` до елементів масиву `array` і таким чином зводить масив до єдиного значення.

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

Якщо передано необов'язковий параметр `initial`, то він буде використаний на початку процесу, або як остаточний результат у разі порожнього масиву.

### Значення, що повертаються

Повертає значення, що вийшло.

Якщо масив порожній і не передано параметр `initial` **arrayreduce()** поверне **`null`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Якщо параметр `callback` очікує, що буде передано значення за посиланням, функція тепер видасть помилку рівня **`E_WARNING`** |

### Приклади

**Приклад #1 Приклад використання **arrayreduce()****

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

-   [arrayfilter()](function.array-filter.md) - Фільтрує елементи масиву за допомогою callback-функції
-   [arraymap()](function.array-map.md) - Застосовує callback-функцію до всіх елементів зазначених масивів
-   [arrayunique()](function.array-unique.md) - Прибирає значення, що повторюються, з масиву
-   [arraycountvalues()](function.array-count-values.md) - підраховує кількість усіх значень масиву
