---
navigation:
  - dateinterval.format.md: '« DateInterval::format'
  - dateperiod.construct.md: 'DatePeriod::\_\_construct »'
  - index.md: PHP Manual
  - book.datetime.md: Дата час
title: Клас DatePeriod
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас DatePeriod

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

## Вступ

Представляє тимчасовий період.

Дозволяє переміщатися в заданому часовому інтервалі на рівні проміжки часу.

## Огляд класів

```classsynopsis

    
     class DatePeriod
    

    
     implements
      IteratorAggregate {

    /* Константы */
    
     public
     const
     int
      EXCLUDE_START_DATE;

    public
     const
     int
      INCLUDE_END_DATE;


    /* Свойства */
    public
     readonly
     ?DateTimeInterface
      $start;

    public
     readonly
     ?DateTimeInterface
      $current;

    public
     readonly
     ?DateTimeInterface
      $end;

    public
     readonly
     ?DateInterval
      $interval;

    public
     readonly
     int
      $recurrences;

    public
     readonly
     bool
      $include_start_date;

    public
     readonly
     bool
      $include_end_date;


    /* Методы */
    
   public __construct(    DateTimeInterface $start,    DateInterval $interval,    int $recurrences,    int $options = 0)
public __construct(    DateTimeInterface $start,    DateInterval $interval,    DateTimeInterface $end,    int $options = 0)
public __construct(string $isostr, int $options = 0)

    public static createFromISO8601String(string $specification, int $options = 0): static
public getDateInterval(): DateInterval
public getEndDate(): ?DateTimeInterface
public getRecurrences(): ?int
public getStartDate(): DateTimeInterface

   }
```

## Обумовлені константи

**`DatePeriod::EXCLUDE_START_DATE`**

Виключає початкову дату, використовується в [DatePeriod::\_\_construct()](dateperiod.construct.md)

**`DatePeriod::INCLUDE_END_DATE`**

Включає дату закінчення, використовується в [DatePeriod::\_\_construct()](dateperiod.construct.md)

## Властивості

recurrences

Мінімальна кількість екземплярів, що повертається ітератором.

Якщо кількість повторень була явно передана за допомогою параметра recurrences конструктор екземпляра **DatePeriod**, то ця властивість містить це значення, *плюс* один, якщо дата початку не була відключена за допомогою константи **`DatePeriod::EXCLUDE_START_DATE`** *плюс* один, якщо дата закінчення була включена за допомогою константи **`DatePeriod::INCLUDE_END_DATE`**

Якщо кількість повторень не було передано явно, то ця властивість містить мінімальну кількість повернутих екземплярів. Це буде *плюс* один, якщо дата початку не вимкнена за допомогою константи **`DatePeriod::EXCLUDE_START_DATE`** *плюс* один, якщо дата закінчення була включена за допомогою константи **`DatePeriod::INCLUDE_END_DATE`**

```php
<?php
$start = new DateTime('2018-12-31 00:00:00');
$end   = new DateTime('2021-12-31 00:00:00');
$interval = new DateInterval('P1M');
$recurrences = 5;

// повторения явно задаются в конструкторе
$period = new DatePeriod($start, $interval, $recurrences, DatePeriod::EXCLUDE_START_DATE);
echo $period->recurrences, "\n";

$period = new DatePeriod($start, $interval, $recurrences);
echo $period->recurrences, "\n";

$period = new DatePeriod($start, $interval, $recurrences, DatePeriod::INCLUDE_END_DATE);
echo $period->recurrences, "\n";

// повторения не заданы в конструкторе
$period = new DatePeriod($start, $interval, $end);
echo $period->recurrences, "\n";

$period = new DatePeriod($start, $interval, $end, DatePeriod::EXCLUDE_START_DATE);
echo $period->recurrences, "\n";
?>
```

Результат виконання наведеного прикладу:

5  
6  
7

Смотрите также описание метода[DatePeriod::getRecurrences()](dateperiod.getrecurrences.md)

include\_end\_date

Включати дату закінчення в набір дат, що повторюються, чи ні.

include\_start\_date

Включати початкову дату в набір дат чи ні.

start

Дата початку періоду.

current

У процесі ітерації міститиме поточну дату періоду.

end

Кінцева дата періоду.

interval

Специфікація інтервалу, що повторюється згідно ISO 8601.

## список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Були додані константа **`DatePeriod::INCLUDE_END_DATE`** та властивість include\_end\_date. |
| 8.0.0 | Класс**DatePeriod** тепер реалізує інтерфейс [IteratorAggregate](class.iteratoraggregate.md). . Раніше натомість було реалізовано інтерфейс [Traversable](class.traversable.md) |

## Зміст

-   [DatePeriod::\_\_construct](dateperiod.construct.md)— Створює новий об'єкт DatePeriod
-   [DatePeriod::createFromISO8601String](dateperiod.createfromiso8601string.md)— Створює новий об'єкт DatePeriod із рядка у форматі стандарту ISO8601
-   [DatePeriod::getDateInterval](dateperiod.getdateinterval.md) \- Повертає інтервал
-   [DatePeriod::getEndDate](dateperiod.getenddate.md)— Повертає кінцеву дату періоду
-   [DatePeriod::getRecurrences](dateperiod.getrecurrences.md)— Отримує кількість повторів
-   [DatePeriod::getStartDate](dateperiod.getstartdate.md)— Повертає початкову дату періоду
