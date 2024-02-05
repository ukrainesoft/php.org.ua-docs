---
navigation:
  - dateperiod.construct.md: '« DatePeriod::\_\_construct'
  - dateperiod.getdateinterval.md: 'DatePeriod::getDateInterval »'
  - index.md: PHP Manual
  - class.dateperiod.md: DatePeriod
title: 'DatePeriod::createFromISO8601String'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DatePeriod::createFromISO8601String

(PHP 8 >= 8.3.0)

DatePeriod::createFromISO8601String — Створює новий об'єкт DatePeriod із рядка у форматі стандарту ISO8601

### Опис

```methodsynopsis
public static DatePeriod::createFromISO8601String(string $specification, int $options = 0): static
```

Створює новий об'єкт DatePeriod із рядка у форматі стандарту ISO8601, як зазначено у параметрі `specification`

### Список параметрів

`specification`

Подмножество[» специфікації повторюваних інтервалів стандарту ISO 8601](http://en.wikipedia.org/wiki/Iso8601#Repeating_intervals)

Приклад специфікації інтервалу стандарту ISO 8601, що приймається, — це рядок `R5/2008-03-01T13:00:00Z/P1Y2M10DT2H30M`, яка вказує:

-   5 повторень (`R5/`) .
-   Починати з`2008-03-01T13:00:00Z`
-   Кожне повторення дорівнює інтервалу в 1 рік 2 місяці 10 днів 2 години та 30 хвилин (`/P1Y2M10DT2H30M`

Приклади специфікації інтервалів стандарту ISO 8601, які PHP не підтримує:

1.  нуль разів (`R0/`) .
2.  зміщення часу, відмінні від UTC (`Z`), наприклад,`+02:00`

`options`

Бітове поле, яке можна вказувати для керування окремою поведінкою з початковими та кінцевими датами.

Константа\*\*`DatePeriod::EXCLUDE_START_DATE`\*\*исключает дату начала из набора повторяющихся дат в пределах периода.

Константа\*\*`DatePeriod::INCLUDE_END_DATE`\*\* включає дату закінчення набору повторюваних дат у межах періоду.

### Значення, що повертаються

Повертає створений об'єкт DatePeriod.

З об'єктом, створеним цим методом [DatePeriod](class.dateperiod.md), можна працювати як з ітератором, щоб створювати об'єкти [DateTimeImmutable](class.datetimeimmutable.md)

### Помилки

Викидає виняток [DateMalformedPeriodStringException](class.datemalformedperiodstringexception.md), если значение параметра`specification` не можна розібрати як допустиме значення періоду у форматі стандарту ISO 8601.

### Приклади

**Приклад #1 Приклад використання методу DatePeriod::createFromISO8601String**

```php
<?php
$iso = 'R4/2023-07-01T00:00:00Z/P7D';

$period = DatePeriod::createFromISO8601String($iso);

// При переборе объекта DatePeriod будут напечатаны
// повторяющиеся в пределах периода даты.
foreach ($period as $date) {
    echo $date->format('Y-m-d'), "\n";
}
?>
```

Результат виконання наведеного прикладу:

```
2023-07-01
2023-07-08
2023-07-15
2023-07-22
2023-07-29
```
