---
navigation:
  - function.array-udiff-uassoc.md: « array\_udiff\_uassoc
  - function.array-uintersect-assoc.md: array\_uintersect\_assoc »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_udiff
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_udiff

(PHP 5, PHP 7, PHP 8)

array\_udiff - Обчислює розбіжність масивів, використовуючи для порівняння callback-функцію

### Опис

```methodsynopsis
array_udiff(array $array, array ...$arrays, callable $value_compare_func): array
```

Обчислює розбіжність масивів, використовуючи порівняння даних callback-функцию. Поведінка цієї функції відрізняється від поведінки функції [array\_diff()](function.array-diff.md)яка порівнює дані через внутрішню функцію.

### Список параметрів

`array`

Перший масив.

`arrays`

Масиви для порівняння.

`value_compare_func`

Функція порівняння повинна повертати ціле, яке менше, дорівнює чи більше нуля, якщо перший аргумент є відповідно меншим, рівним чи більшим, ніж другий.

```methodsynopsis
callback(mixed $a, mixed $b): int
```

**Застереження**

Возвращение*нецілих* значень з функції порівняння, таких як число з плаваючою точкою (float), призведе до внутрішнього приведення значення callback-функції, що повертається, до цілого числа (int). Таким чином, значення `0.99`и`0.1` будуть приведені до цілого значення що дозволить порівняти ці значення як рівні.

**Застереження**

Callback-функція сортування повинна обробляти будь-яке значення з будь-якого масиву у будь-якому порядку, незалежно від того, в якому порядку вони були надані спочатку. Причина цього у тому, кожен окремий масив спочатку сортується перед порівнянням коїться з іншими масивами. Наприклад:

```php
<?php

$arrayA = ["string", 1];
$arrayB = [["value" => 1]];
// $item1 and $item2 can be any of "string", 1 or ["value" => 1]
$compareFunc = static function ($item1, $item2) {
    $value1 = is_string($item1) ? strlen($item1) : (is_array($item1) ? $item1["value"] : $item1);
    $value2 = is_string($item2) ? strlen($item2) : (is_array($item2) ? $item2["value"] : $item2);
    return $value1 <=> $value2;
};

?>
```

### Значення, що повертаються

Повертає масив (array), що містить елементи аргументу `array`, яких немає в жодному іншому аргументі.

### Приклади

**Приклад #1 Приклад використання функції** array\_udiff()\*\* з об'єктами класу stdClass\*\*

```php
<?php

// Массивы для сравнения
$array1 = array(new stdClass, new stdClass,
                new stdClass, new stdClass,
               );

$array2 = array(
                new stdClass, new stdClass,
               );

// Проставление свойств для объектов
$array1[0]->width = 11; $array1[0]->height = 3;
$array1[1]->width = 7;  $array1[1]->height = 1;
$array1[2]->width = 2;  $array1[2]->height = 9;
$array1[3]->width = 5;  $array1[3]->height = 7;

$array2[0]->width = 7;  $array2[0]->height = 5;
$array2[1]->width = 9;  $array2[1]->height = 2;

function compare_by_area($a, $b) {
    $areaA = $a->width * $a->height;
    $areaB = $b->width * $b->height;

    if ($areaA < $areaB) {
        return -1;
    } elseif ($areaA > $areaB) {
        return 1;
    } else {
        return 0;
    }
}

print_r(array_udiff($array1, $array2, 'compare_by_area'));

?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [0] => stdClass Object
        (
            [width] => 11
            [height] => 3
        )

    [1] => stdClass Object
        (
            [width] => 7
            [height] => 1
        )

)
```

**Приклад #2 Приклад використання функції** array\_udiff()\*\* з об'єктами класу DateTime\*\*

```php
<?php

class MyCalendar {
    public $free = array();
    public $booked = array();

    public function __construct($week = 'now') {
        $start = new DateTime($week);
        $start->modify('Monday this week midnight');
        $end = clone $start;
        $end->modify('Friday this week midnight');
        $interval = new DateInterval('P1D');
        foreach (new DatePeriod($start, $interval, $end) as $freeTime) {
            $this->free[] = $freeTime;
        }
    }

    public function bookAppointment(DateTime $date, $note) {
        $this->booked[] = array('date' => $date->modify('midnight'), 'note' => $note);
    }

    public function checkAvailability() {
        return array_udiff($this->free, $this->booked, array($this, 'customCompare'));
    }

    public function customCompare($free, $booked) {
        if (is_array($free)) $a = $free['date'];
        else $a = $free;
        if (is_array($booked)) $b = $booked['date'];
        else $b = $booked;
        if ($a == $b) {
            return 0;
        } elseif ($a > $b) {
            return 1;
        } else {
            return -1;
        }
    }
}

// Создание календаря еженедельных встреч
$myCalendar = new MyCalendar;

// Запись еженедельных встреч
$myCalendar->bookAppointment(new DateTime('Monday this week'), "Уборка квартиры сотрудника Google.");
$myCalendar->bookAppointment(new DateTime('Wednesday this week'), "Катание на сноуборде.");
$myCalendar->bookAppointment(new DateTime('Friday this week'), "Борьба с багами в коде.");

// Проверка доступности дней путём сравнения дат в переменной $booked с датами переменной $free
echo "Я доступен в следующие дни на этой неделе...\n\n";
foreach ($myCalendar->checkAvailability() as $free) {
    echo $free->format('l'), "\n";
}
echo "\n\n";
echo "Я занят в следующие дни на этой неделе...\n\n";
foreach ($myCalendar->booked as $booked) {
    echo $booked['date']->format('l'), ": ", $booked['note'], "\n";
}

?>
```

Результат виконання наведеного прикладу:

```
Я доступен в следующие дни на этой неделе...

Tuesday
Thursday


Я занят в следующие дни на этой неделе...

Monday: Уборка квартиры сотрудника Google.
Wednesday: Катание на сноуборде.
Friday: Борьба с багами в коде.
```

### Примітки

> **Зауваження**: Зверніть увагу, що функція обробляє лише перший рівень багатовимірного масиву. Значення на вкладених рівнях обробляють, наприклад, так: `array_udiff($array1[0], $array2[0], "data_compare_func");`

### Дивіться також

-   [array\_diff()](function.array-diff.md) \- обчислює розбіжність масивів
-   [array\_diff\_assoc()](function.array-diff-assoc.md) \- обчислює розбіжність масивів з додатковою перевіркою індексу
-   [array\_diff\_uassoc()](function.array-diff-uassoc.md) \- Обчислює розбіжність масивів з додатковою перевіркою індексу через пользовательскую callback-функцію
-   [array\_udiff\_assoc()](function.array-udiff-assoc.md) \- обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи порівняння значень callback-функцию
-   [array\_udiff\_uassoc()](function.array-udiff-uassoc.md) \- обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи для порівняння значень та індексів callback-функцію
-   [array\_intersect()](function.array-intersect.md) \- обчислює перетин масивів
-   [array\_intersect\_assoc()](function.array-intersect-assoc.md) \- обчислює перетин масивів з додатковою перевіркою індексу
-   [array\_uintersect()](function.array-uintersect.md) \- обчислює перетин масивів, використовуючи для порівняння значень callback-функцію
-   [array\_uintersect\_assoc()](function.array-uintersect-assoc.md) \- обчислює перетин масивів з додатковою перевіркою індексів, використовуючи для порівняння значень callback-функцію
-   [array\_uintersect\_uassoc()](function.array-uintersect-uassoc.md) \- обчислює перетин масивів з додатковою перевіркою індексу, використовуючи для порівняння індексів та значень окремі callback-функції
