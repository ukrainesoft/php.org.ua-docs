---
navigation:
  - function.array-fill.md: « arrayfill
  - function.array-flip.md: arrayflip »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: arrayfilter
---
# arrayfilter

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

arrayfilter - Фільтрує елементи масиву за допомогою callback-функції

### Опис

```methodsynopsis
array_filter(array $array, ?callable $callback = null, int $mode = 0): array
```

Обходить кожне значення масиву `array`, передаючи його в `callback`функцію. Якщо `callback`функція повертає **`true`**, це значення з `array` повертається в результуючий array.

Ключі масиву зберігаються і можуть призвести до перепусток, якщо `array` був проіндексований. Результат масиву (array) можна переіндексувати за допомогою функції [arrayvalues()](function.array-values.md)

### Список параметрів

`array`

Ітерований масив

`callback`

Callback-функція, що використовується

Якщо `callback`функція не передана, всі порожні значення масиву `array` будуть видалені. Дивіться [empty()](function.empty.md)Щоб дізнатися, як PHP визначає порожнє значення в цьому випадку.

`mode`

Прапор, який визначає, які аргументи передавати в `callback`

-   **`ARRAY_FILTER_USE_KEY`** - передавати тільки ключ масиву як аргумент для `callback` замість значення
-   **`ARRAY_FILTER_USE_BOTH`** - передавати і ключ, і значення `callback` замість тільки значення

За замовчуванням `0`що означає, що в `callback`функцію передаватиметься лише значення як єдиний аргумент.

### Значення, що повертаються

Повертає відфільтрований масив.

### список змін

| Версия | Описание |
| --- | --- |
|  | `callback` тепер допускає значення null. |
|  | Якщо параметр `callback` очікує, що буде передано значення за посиланням, функція тепер видасть помилку рівня **`E_WARNING`** |

### Приклади

**Приклад #1 Приклад використання **arrayfilter()****

```php
<?php
function odd($var)
{
    // является ли переданное число нечётным
    return $var & 1;
}

function even($var)
{
    // является ли переданное число чётным
    return !($var & 1);
}

$array1 = ['a' => 1, 'b' => 2, 'c' => 3, 'd' => 4, 'e' => 5];
$array2 = [6, 7, 8, 9, 10, 11, 12];

echo "Нечётные:\n";
print_r(array_filter($array1, "odd"));
echo "Чётные:\n";
print_r(array_filter($array2, "even"));
?>
```

Результат виконання цього прикладу:

```
Нечётные:
Array
(
    [a] => 1
    [c] => 3
    [e] => 5
)
Чётные:
Array
(
    [0] => 6
    [2] => 8
    [4] => 10
    [6] => 12
)
```

**Приклад #2 Використання **arrayfilter()** без `callback`функції**

```php
<?php

$entry = [
    0 => 'foo',
    1 => false,
    2 => -1,
    3 => null,
    4 => '',
    5 => '0',
    6 => 0,
];

print_r(array_filter($entry));
?>
```

Результат виконання цього прикладу:

```
Array
(
    [0] => foo
    [2] => -1
)
```

**Приклад #3 **arrayfilter()** із зазначеним `mode`**

```php
<?php

$arr = ['a' => 1, 'b' => 2, 'c' => 3, 'd' => 4];

var_dump(array_filter($arr, function($k) {
    return $k == 'b';
}, ARRAY_FILTER_USE_KEY));

var_dump(array_filter($arr, function($v, $k) {
    return $k == 'b' || $v == 4;
}, ARRAY_FILTER_USE_BOTH));
?>
```

Результат виконання цього прикладу:

```
array(1) {
  ["b"]=>
  int(2)
}
array(2) {
  ["b"]=>
  int(2)
  ["d"]=>
  int(4)
}
```

### Примітки

**Застереження**

Якщо callback-функція змінює масив (наприклад, додає чи видаляє елементи), поведінка цієї функції невизначена.

### Дивіться також

-   [arrayintersect()](function.array-intersect.md) - обчислює сходження масивів
-   [arraymap()](function.array-map.md) - Застосовує callback-функцію до всіх елементів зазначених масивів
-   [arrayreduce()](function.array-reduce.md) - Ітеративно зменшує масив до єдиного значення, використовуючи callback-функцію
-   [arraywalk()](function.array-walk.md) - Застосовує задану користувачем функцію кожного елемента масиву
