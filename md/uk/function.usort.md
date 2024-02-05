---
navigation:
  - function.uksort.md: « uksort
  - book.classobj.md: Класи та об'єкти »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: usort
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# usort

(PHP 4, PHP 5, PHP 7, PHP 8)

usort — Сортує масив за значеннями використовуючи функцію користувача для порівняння елементів

### Опис

```methodsynopsis
usort(array &$array, callable $callback): true
```

Сортує `array`по значениям, используя предоставленную пользователем функцию сравнения для определения порядка.

> **Зауваження** :
> 
> Якщо обидва порівнювані значення еквівалентні, вони зберігають свій початковий порядок. До PHP 8.0.0 їх відносний порядок у відсортованому масиві не було визначено.

> **Зауваження**: Ця функція надає нові ключі елементам `array`. Вона видалить усі існуючі ключі, а не просто переупорядкує їх.

### Список параметрів

`array`

Вхідний масив

`callback`

Функція порівняння повинна повертати ціле, яке менше, дорівнює чи більше нуля, якщо перший аргумент є відповідно меншим, рівним чи більшим, ніж другий.

```methodsynopsis
callback(mixed $a, mixed $b): int
```

**Застереження**

Возвращение*нецілих* значень з функції порівняння, таких як число з плаваючою точкою (float), призведе до внутрішнього приведення значення callback-функції, що повертається, до цілого числа (int). Таким чином, значення `0.99`и`0.1` будуть приведені до цілого значення що дозволить порівняти ці значення як рівні.

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Тип значення, що повертається тепер **`true`**; раніше було bool. |
| 8.0.0 | Тепер функція видасть помилку рівня **`E_WARNING`**, якщо параметр callback-функції, переданої у параметр `callback`, очікує на передачу значення за посиланням. |

### Приклади

**Приклад #1 Приклад використання** usort()\*\*\*\*

```php
<?php
function cmp($a, $b)
{
    if ($a == $b) {
        return 0;
    }
    return ($a < $b) ? -1 : 1;
}

$a = array(3, 2, 5, 6, 1);

usort($a, "cmp");

foreach ($a as $key => $value) {
    echo "$key: $value\n";
}
?>
```

Результат виконання наведеного прикладу:

```
0: 1
1: 2
2: 3
3: 5
4: 6
```

Для більшого спрощення внутрішнього порівняння можна використовувати оператор spaceship (космічний корабель).

```php
<?php
function cmp($a, $b)
{
    return $a <=> $b;
}

$a = array(3, 2, 5, 6, 1);

usort($a, "cmp");

foreach ($a as $key => $value) {
    echo "$key: $value\n";
}
?>
```

> **Зауваження** :
> 
> Очевидно, що для цього тривіального випадку більш підходить функція [sort()](function.sort.md)

**Приклад #2 Приклад використання функції** usort()\*\* з багатовимірними масивами\*\*

```php
<?php
function cmp($a, $b)
{
    return strcmp($a["fruit"], $b["fruit"]);
}

$fruits[0]["fruit"] = "lemons";
$fruits[1]["fruit"] = "apples";
$fruits[2]["fruit"] = "grapes";

usort($fruits, "cmp");

foreach ($fruits as $key => $value) {
    echo "\$fruits[$key]: " . $value["fruit"] . "\n";
}
?>
```

При сортуванні багатовимірного масиву змінні $a і $b містять посилання перші два індексу масиву.

Результат виконання наведеного прикладу:

```
$fruits[0]: apples
$fruits[1]: grapes
$fruits[2]: lemons
```

**Приклад #3 Приклад використання** usort()**с методом класса**

```php
<?php
class TestObj {
    private string $name;

    function __construct($name)
    {
        $this->name = $name;
    }

    /* This is the static comparing function: */
    static function cmp_obj($a, $b)
    {
        return strtolower($a->name) <=> strtolower($b->name);
    }
}

$a[] = new TestObj("c");
$a[] = new TestObj("b");
$a[] = new TestObj("d");

usort($a, [TestObj::class, "cmp_obj"]);

foreach ($a as $item) {
    echo $item->name . "\n";
}
?>
```

Результат виконання наведеного прикладу:

```
b
c
d
```

**Приклад #4 Приклад використання функції** usort()**с применением[анонімної функції](functions.anonymous.md) для сортування багатовимірного масиву**

```php
<?php
$array[0] = array('key_a' => 'z', 'key_b' => 'c');
$array[1] = array('key_a' => 'x', 'key_b' => 'b');
$array[2] = array('key_a' => 'y', 'key_b' => 'a');

function build_sorter($key) {
    return function ($a, $b) use ($key) {
        return strnatcmp($a[$key], $b[$key]);
    };
}

usort($array, build_sorter('key_b'));

foreach ($array as $item) {
    echo $item['key_a'] . ', ' . $item['key_b'] . "\n";
}
?>
```

Результат виконання наведеного прикладу:

```
y, a
x, b
z, c
```

**Приклад #5 Приклад використання** usort()\*\* з оператором spaceship (космічний корабель)\*\*

Оператор spaceship (космічний корабель) дозволяє прямолінійно порівнювати складові значення кількох осях. У наступному прикладі `$people` сортується на прізвище, а потім на ім'я, якщо прізвище збігається.

```php
<?php
$people[0] = ['first' => 'Adam', 'last' => 'West'];
$people[1] = ['first' => 'Alec', 'last' => 'Baldwin'];
$people[2] = ['first' => 'Adam', 'last' => 'Baldwin'];

function sorter(array $a, array $b) {
    return [$a['last'], $a['first']] <=> [$b['last'], $b['first']];
}

usort($people, 'sorter');

foreach ($people as $person) {
    print $person['last'] . ', ' . $person['first'] . PHP_EOL;
}
?>
```

Результат виконання наведеного прикладу:

```
Baldwin, Adam
Baldwin, Alec
West, Adam
```

### Дивіться також

-   [uasort()](function.uasort.md) \- Сортує масив користувальницькою функцією порівняння, зберігаючи асоціацію індексів
-   [uksort()](function.uksort.md) \- Сортує масив за ключами користувальницькою функцією порівняння
-   [Порівняння функцій сортування масивів](array.sorting.md)
