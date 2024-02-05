---
navigation:
  - function.array-keys.md: « array\_keys
  - function.array-merge-recursive.md: array\_merge\_recursive »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_map
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_map

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

array\_map - Застосовує callback-функцію до всіх елементів зазначених масивів

### Опис

```methodsynopsis
array_map(?callable $callback, array $array, array ...$arrays): array
```

Функция**array\_map()** повертає масив (array), що містить результати застосування `callback`\-функції до відповідного елементу `array`(и`arrays`, якщо вказано більше масивів), що використовується як аргумент callback-функції. Кількість параметрів, що передаються `callback`\-функції, що має збігатися з кількістю масивів, переданою функції **array\_map()**. Зайві вхідні масиви ігноруються. Якщо надано недостатню кількість аргументів, викидається [ArgumentCountError](class.argumentcounterror.md)

### Список параметрів

`callback`

[callable](language.types.callable.md), що застосовується до кожного елемента у кожному масиві.

**`null`** може бути переданий як значення `callback` для виконання zip операції з кількома масивами. Якщо вказано тільки `array` **array\_map()** поверне вхідний масив.

`array`

Массив, к которому применяется`callback`\-функція.

`arrays`

Додаткові масиви для обробки `callback`\-функцією.

### Значення, що повертаються

Повертає масив, що містить результати застосування `callback`\-функції до відповідного елементу `array`(и`arrays`, якщо вказано більше масивів), що використовується як аргумент для callback-функції.

Повернений масив збереже ключі аргументу масиву тоді і лише тоді, коли буде передано рівно один масив. Якщо передано більше одного масиву, повернутий масив матиме послідовні цілі ключі.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Тепер функція видасть помилку рівня **`E_WARNING`**, якщо параметр callback-функції, переданої у параметр `callback`, очікує на передачу значення за посиланням. |

### Приклади

**Пример #1 Пример использования**array\_map()\*\*\*\*

```php
<?php
function cube($n)
{
    return ($n * $n * $n);
}

$a = [1, 2, 3, 4, 5];
$b = array_map('cube', $a);
print_r($b);
?>
```

В результаті змінна $b міститиме:

```
Array
(
    [0] => 1
    [1] => 8
    [2] => 27
    [3] => 64
    [4] => 125
)
```

**Пример #2 Использование**array\_map()**вместе с лямбда-функцией**

```php
<?php
$func = function(int $value): int {
    return $value * 2;
};

print_r(array_map($func, range(1, 5)));

// Или с PHP 7.4.0:

print_r(array_map(fn($value): int => $value * 2, range(1, 5)));

?>
```

```
Array
(
    [0] => 2
    [1] => 4
    [2] => 6
    [3] => 8
    [4] => 10
)
```

**Пример #3 Пример использования**array\_map()**: обробка кількох масивів**

```php
<?php
function show_Spanish(int $n, string $m): string
{
    return "Число {$n} по-испански - {$m}";
}

function map_Spanish(int $n, string $m): array
{
    return [$n => $m];
}

$a = [1, 2, 3, 4, 5];
$b = ['uno', 'dos', 'tres', 'cuatro', 'cinco'];

$c = array_map('show_Spanish', $a, $b);
print_r($c);

$d = array_map('map_Spanish', $a , $b);
print_r($d);
?>
```

Результат виконання наведеного прикладу:

```
// вывод $c
Array
(
    [0] => Число 1 по-испански - uno
    [1] => Число 2 по-испански - dos
    [2] => Число 3 по-испански - tres
    [3] => Число 4 по-испански - cuatro
    [4] => Число 5 по-испански - cinco
)

// вывод $d
Array
(
    [0] => Array
        (
            [1] => uno
        )

    [1] => Array
        (
            [2] => dos
        )

    [2] => Array
        (
            [3] => tres
        )

    [3] => Array
        (
            [4] => cuatro
        )

    [4] => Array
        (
            [5] => cinco
        )

)
```

Зазвичай при обробці двох або більше масивів вони мають однакову довжину, так як callback-функція застосовується паралельно до відповідних елементів масивів. Якщо масиви мають різну довжину, більш короткі їх доповнюється елементами з порожніми значеннями до довжини найдовшого масиву.

Цікавим ефектом при використанні цієї функції є створення масиву масивів, що може бути досягнуто шляхом використання значення \*\*`null`\*\*в качестве имени callback-функции.

**Приклад #4 Виконання zip операції з масивами**

```php
<?php
$a = [1, 2, 3, 4, 5];
$b = ['one', 'two', 'three', 'four', 'five'];
$c = ['uno', 'dos', 'tres', 'cuatro', 'cinco'];

$d = array_map(null, $a, $b, $c);
print_r($d);
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [0] => Array
        (
            [0] => 1
            [1] => one
            [2] => uno
        )

    [1] => Array
        (
            [0] => 2
            [1] => two
            [2] => dos
        )

    [2] => Array
        (
            [0] => 3
            [1] => three
            [2] => tres
        )

    [3] => Array
        (
            [0] => 4
            [1] => four
            [2] => cuatro
        )

    [4] => Array
        (
            [0] => 5
            [1] => five
            [2] => cinco
        )

)
```

**Пример #5**`null`\*\* `callback` тільки з `array`\*\*

```php
<?php
$array = [1, 2, 3];
var_dump(array_map(null, $array));
?>
```

Результат виконання наведеного прикладу:

```
array(3) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
}
```

**Пример #6 Использование**array\_map()\*\* з рядковими ключами\*\*

```php
<?php
$arr = ['stringkey' => 'value'];
function cb1($a) {
    return [$a];
}
function cb2($a, $b) {
    return [$a, $b];
}
var_dump(array_map('cb1', $arr));
var_dump(array_map('cb2', $arr, $arr));
var_dump(array_map(null,  $arr));
var_dump(array_map(null, $arr, $arr));
?>
```

Результат виконання наведеного прикладу:

```
array(1) {
  ["stringkey"]=>
  array(1) {
    [0]=>
    string(5) "value"
  }
}
array(1) {
  [0]=>
  array(2) {
    [0]=>
    string(5) "value"
    [1]=>
    string(5) "value"
  }
}
array(1) {
  ["stringkey"]=>
  string(5) "value"
}
array(1) {
  [0]=>
  array(2) {
    [0]=>
    string(5) "value"
    [1]=>
    string(5) "value"
  }
}
```

**Пример #7**array\_map()\*\* - асоціативні масиви\*\*

Хотя**array\_map()** безпосередньо не підтримує використання ключа масиву як вхідні дані, це можна змоделювати за допомогою [array\_keys()](function.array-keys.md)

```php
<?php
$arr = [
    'v1' => 'Первый выпуск',
    'v2' => 'Второй выпуск',
    'v3' => 'Третий выпуск',
];

// Примечание: До версии 7.4.0 вместо этого используйте более длинный синтаксис для анонимных функций.
$callback = fn(string $k, string $v): string => "$k - это $v";

$result = array_map($callback, array_keys($arr), array_values($arr));

var_dump($result);
?>
```

Результат виконання наведеного прикладу:

```
array(3) {
  [0]=>
  string(24) "v1 - это Первый выпуск"
  [1]=>
  string(25) "v2 - это Второй выпуск"
  [2]=>
  string(24) "v3 - это Третий выпуск"
}
```

### Дивіться також

-   [array\_filter()](function.array-filter.md) \- Фільтрує елементи масиву за допомогою callback-функції
-   [array\_reduce()](function.array-reduce.md) \- Ітеративно зменшує масив до єдиного значення, використовуючи callback-функцію
-   [array\_walk()](function.array-walk.md) \- Застосовує задану користувачем функцію кожного елемента масиву
