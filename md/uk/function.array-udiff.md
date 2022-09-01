---
navigation:
  - function.array-udiff-uassoc.html: « arrayudiffuassoc
  - function.array-uintersect-assoc.html: arrayuintersectassoc »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: arrayudiff
---
# arrayudiff

(PHP 5, PHP 7, PHP 8)

arrayudiff - Обчислює розбіжність масивів, використовуючи для порівняння callback-функцію

### Опис

```methodsynopsis
array_udiff(array $array, array ...$arrays, callable $value_compare_func): array
```

Обчислює розбіжність масивів, використовуючи порівняння даних callback-функцию. Це відрізняється від поведінки [arraydiff()](function.array-diff.html)яка використовує вбудовану функцію для порівняння даних.

### Список параметрів

`array`

Перший масив.

`arrays`

Масиви для порівняння.

`value_compare_func`

Callback-функція, що використовується для порівняння.

Функція порівняння повинна повертати ціле, яке менше, дорівнює чи більше нуля, якщо перший аргумент є відповідно меншим, рівним чи більшим, ніж другий.

```methodsynopsis
callback(mixed $a, mixed $b): int
```

### Значення, що повертаються

Повертає масив, що містить усі елементи `array`, які не існують у жодному з інших аргументів.

### Приклади

**Приклад #1 Приклад використання **arrayudiff()** з об'єктами класу stdClass**

```php
<?php
// Масиви для сравнения
$array1 = array(new stdclass, new stdclass,
                new stdclass, new stdclass,
               );

$array2 = array(
                new stdclass, new stdclass,
               );

// проставление некоторых свойств для объектов
$array1[0]->width = 11; $array1[0]->height = 3;
$array1[1]->width = 7;  $array1[1]->height = 1;
$array1[2]->width = 2;  $array1[2]->height = 9;
$array1[3]->width = 5;  $array1[3]->height = 7;

$array2[0]->width = 7;  $array2[0]->height = 5;
$array2[1]->width = 9;  $array2[1]->height = 2;

function compare_by_area($a, $b) {
    $areaA = $a->width * $a->height;
    $areaB = $b->width * $b->height;

    if ($areaA < $areaB) {
        return -1;
    } elseif ($areaA > $areaB) {
        return 1;
    } else {
        return 0;
    }
}

print_r(array_udiff($array1, $array2, 'compare_by_area'));
?>
```

Результат виконання цього прикладу:

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

**Приклад #2 Приклад використання **arrayudiff()** з об'єктами класу DateTime**

```php
<?php
class MyCalendar {
    public $free = array();
    public $booked = array();

    public function __construct($week = 'now') {
        $start = new DateTime($week);
        $start->modify('Monday this week midnight');
        $end = clone $start;
        $end->modify('Friday this week midnight');
        $interval = new DateInterval('P1D');
        foreach (new DatePeriod($start, $interval, $end) as $freeTime) {
            $this->free[] = $freeTime;
        }
    }

    public function bookAppointment(DateTime $date, $note) {
        $this->booked[] = array('date' => $date->modify('midnight'), 'note' => $note);
    }

    public function checkAvailability() {
        return array_udiff($this->free, $this->booked, array($this, 'customCompare'));
    }

    public function customCompare($free, $booked) {
        if (is_array($free)) $a = $free['date'];
        else $a = $free;
        if (is_array($booked)) $b = $booked['date'];
        else $b = $booked;
        if ($a == $b) {
            return 0;
        } elseif ($a > $b) {
            return 1;
        } else {
            return -1;
        }
    }
}

// Создание календаря еженедельных встреч
$myCalendar = new MyCalendar;

// Запись некоторых еженедельных встреч
$myCalendar->bookAppointment(new DateTime('Monday this week'), "Уборка квартиры сотрудника Google.");
$myCalendar->bookAppointment(new DateTime('Wednesday this week'), "Катание на сноуборде.");
$myCalendar->bookAppointment(new DateTime('Friday this week'), "Борьба с багами в коде.");

// Проверка доступности дней путём сравнения дат в $booked с датами из $free
echo "Я доступен в следующие дни на этой неделе...\n\n";
foreach ($myCalendar->checkAvailability() as $free) {
    echo $free->format('l'), "\n";
}
echo "\n\n";
echo "Я занят в следующие дни на этой неделе...\n\n";
foreach ($myCalendar->booked as $booked) {
    echo $booked['date']->format('l'), ": ", $booked['note'], "\n";
}
?>
```

Результат виконання цього прикладу:

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

> **Зауваження**: Зверніть увагу, що ця функція обробляє лише один вимір багатовимірного масиву. Зрозуміло, ви можете обробити більше одного виміру, використовуючи `array_udiff($array1[0], $array2[0], "data_compare_func");`

### Дивіться також

-   [arraydiff()](function.array-diff.html) - Обчислити розбіжність масивів
-   [arraydiffassoc()](function.array-diff-assoc.html) - обчислює розбіжність масивів з додатковою перевіркою індексу
-   [arraydiffuassoc()](function.array-diff-uassoc.html) - обчислює розбіжність масивів з додатковою перевіркою індексу, що здійснюється за допомогою callback-функції
-   [arrayudiffassoc()](function.array-udiff-assoc.html) - обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи порівняння значень callback-функцию
-   [arrayudiffuassoc()](function.array-udiff-uassoc.html) - обчислює розбіжність у масивах з додатковою перевіркою індексів, використовуючи для порівняння значень та індексів callback-функцію
-   [arrayintersect()](function.array-intersect.html) - обчислює сходження масивів
-   [arrayintersectassoc()](function.array-intersect-assoc.html) - обчислює сходження масивів з додатковою перевіркою індексу
-   [arrayuintersect()](function.array-uintersect.html) - обчислює перетин масивів, використовуючи для порівняння значень callback-функцію
-   [arrayuintersectassoc()](function.array-uintersect-assoc.html) - обчислює перетин масивів з додатковою перевіркою індексів, використовуючи для порівняння значень callback-функцію
-   [arrayuintersectuassoc()](function.array-uintersect-uassoc.html) - обчислює перетин масивів з додатковою перевіркою індексу, використовуючи для порівняння індексів та значень індивідуальні callback-функції
