---
navigation:
  - class.dateperiod.md: « DatePeriod
  - dateperiod.createfromiso8601string.md: 'DatePeriod::createFromISO8601String »'
  - index.md: PHP Manual
  - class.dateperiod.md: DatePeriod
title: 'DatePeriod::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DatePeriod::\_\_construct

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

DatePeriod::\_\_construct — Створює новий об'єкт DatePeriod

### Опис

public**DatePeriod::\_\_construct**  
[DateTimeInterface](class.datetimeinterface.md) `$start`,  
[DateInterval](class.dateinterval.md) `$interval`,  
int`$recurrences`,  
int`$options`  
) .

public**DatePeriod::\_\_construct**  
[DateTimeInterface](class.datetimeinterface.md) `$start`,  
[DateInterval](class.dateinterval.md) `$interval`,  
[DateTimeInterface](class.datetimeinterface.md) `$end`,  
int`$options`  
) .

**Увага**

public**DatePeriod::\_\_construct**(string`$isostr`, int`$options`

Цей варіант конструктора застарів, використовуйте замість нього метод [DatePeriod::createFromISO8601String()](dateperiod.createfromiso8601string.md)

Створює новий об'єкт DatePeriod.

Об'єкти [DatePeriod](class.dateperiod.md) можна використовувати як ітератор для генерації ряду об'єктів [DateTimeImmutable](class.datetimeimmutable.md) або [DateTime](class.datetime.md) з дати `start` `interval`и`end` або числа `recurrences`

Клас об'єктів, що повертаються, еквівалентний класу-батькові [DateTimeImmutable](class.datetimeimmutable.md) або [DateTime](class.datetime.md) об'єкта `start`

### Список параметрів

`start`

Початкова дата. За замовчуванням включається до набору результатів.

`interval`

Інтервал.

`recurrences`

Кількість повторень. Число результатів, що повертаються на одиницю більше цього, так як дата початку включається в набір результатів за замовчуванням. Має бути більше, ніж

`end`

Кінцева дата. За замовчуванням виключається із набору результатів.

`isostr`

Подмножество, содержащее интервал согласно[» спеціфікації ISO 8601](http://en.wikipedia.org/wiki/Iso8601#Repeating_intervals)

Прикладами деяких особливостей специфікації інтервалів ISO 8601, які не підтримує PHP, є:

1.  нульові входження (`R0/`) .
2.  зсув часу, відмінне від UTC (`Z`), наприклад,`+02:00`

`options`

Бітове поле, яке можна використовувати для керування певною поведінкою з початковою та кінцевою датами.

Виключити початкову дату всередині періоду з набору дат, що повторюються, можна за допомогою константи **`DatePeriod::EXCLUDE_START_DATE`**

Включити кінцеву дату всередині періоду в набір дат, що повторюються, можна за допомогою константи **`DatePeriod::INCLUDE_END_DATE`**

### Помилки

Когда значение параметра`isostr` не може бути розібрано аналізатором як допустимий стандартом ISO 8601 формат, викидається виняток [DateMalformedPeriodStringException](class.datemalformedperiodstringexception.md). До PHP 8.3 викидався виняток [Exception](class.exception.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Тепер замість винятку [Exception](class.exception.md) викидається виняток [DateMalformedPeriodStringException](class.datemalformedperiodstringexception.md) |
| 8.2.0 | Добавлена константа\*\*`DatePeriod::INCLUDE_END_DATE`\*\* |
| 7.2.19, 7.3.6, 7.4.0 | `recurrences` має бути більше |

### Приклади

**Приклад #1 Приклад використання DatePeriod**

```php
<?php
$start = new DateTime('2012-07-01');
$interval = new DateInterval('P7D');
$end = new DateTime('2012-07-31');
$recurrences = 4;
$iso = 'R4/2012-07-01T00:00:00Z/P7D';

// Эти периоды эквивалентны.
$period = new DatePeriod($start, $interval, $recurrences);
$period = new DatePeriod($start, $interval, $end);
$period = new DatePeriod($iso);

// При переборе экземпляра DatePeriod в цикле будут отображены все отобранные даты
// периода.
foreach ($period as $date) {
    echo $date->format('Y-m-d')."\n";
}
?>
```

Результат виконання наведеного прикладу:

```
2012-07-01
2012-07-08
2012-07-15
2012-07-22
2012-07-29
```

**Пример #2 Пример использования DatePeriod с**`DatePeriod::EXCLUDE_START_DATE`\*\*\*\*

```php
<?php
$start = new DateTime('2012-07-01');
$interval = new DateInterval('P7D');
$end = new DateTime('2012-07-31');

$period = new DatePeriod($start, $interval, $end,
                         DatePeriod::EXCLUDE_START_DATE);

// При переборе экземпляра DatePeriod в цикле будут отображены все отобранные даты
// периода.
// Однако в этом случае 2012-07-01 не будет отображена.
foreach ($period as $date) {
    echo $date->format('Y-m-d')."\n";
}
?>
```

Результат виконання наведеного прикладу:

```
2012-07-08
2012-07-15
2012-07-22
2012-07-29
```

**Приклад #3 Приклад використання DatePeriod, що показує всі останні четверги на рік**

```php
<?php
$begin = new DateTime('2021-12-31');
$end = new DateTime('2022-12-31 23:59:59');

$interval = DateInterval::createFromDateString('last thursday of next month');
$period = new DatePeriod($begin, $interval, $end, DatePeriod::EXCLUDE_START_DATE);

foreach ($period as $dt) {
    echo $dt->format('l Y-m-d'), "\n";
}
?>
```

Результат виконання наведеного прикладу:

```
Thursday 2022-01-27
Thursday 2022-02-24
Thursday 2022-03-31
Thursday 2022-04-28
Thursday 2022-05-26
Thursday 2022-06-30
Thursday 2022-07-28
Thursday 2022-08-25
Thursday 2022-09-29
Thursday 2022-10-27
Thursday 2022-11-24
Thursday 2022-12-29
```

### Примітки

Незв'язкова кількість повторень, визначених у секції 4.5 ISO 8601 "Recurring time interval", не підтримується, тобто ні передача `"R/..."`в`isostr`, ни\*\*`null`\*\*в`end`, не працюватимуть.
