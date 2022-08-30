Клас DatePeriod

-   [« DateInterval::format](dateinterval.format.html)
    
-   [DatePeriod::construct »](dateperiod.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Дата/время](book.datetime.html)
    
-   Клас DatePeriod
    

# Клас DatePeriod

(PHP 5> = 5.3.0, PHP 7, PHP 8)

## Вступ

Представляє тимчасовий період.

Дозволяє переміщатися в заданому часовому інтервалі на рівні проміжки часу.

## Огляд класів

```classsynopsis

     
    

    
     
      class DatePeriod
     

     implements 
       IteratorAggregate {

    /* Константы */
    
     const
     int
      EXCLUDE_START_DATE = 1;


    /* Свойства */
    public
     int
      $recurrences;

    public
     bool
      $include_start_date;

    public
     DateTimeInterface
      $start;

    public
     DateTimeInterface
      $current;

    public
     DateTimeInterface
      $end;

    public
     DateInterval
      $interval;


    /* Методы */
    
   public __construct(    DateTimeInterface $start,    DateInterval $interval,    int $recurrences,    int $options = 0)
public __construct(    DateTimeInterface $start,    DateInterval $interval,    DateTimeInterface $end,    int $options = 0)
public __construct(string $isostr, int $options = 0)

    public getDateInterval(): DateInterval
public getEndDate(): ?DateTimeInterface
public getRecurrences(): ?int
public getStartDate(): DateTimeInterface

   }
```

## Обумовлені константи

**`DatePeriod::EXCLUDE_START_DATE`**

Виключає початкову дату, використовується в [DatePeriod::construct()](dateperiod.construct.html)

## Властивості

recurrences

Число повторів, якщо об'єкт **DatePeriod** створювався з явною вказівкою `$recurrences`. Дивіться [DatePeriod::getRecurrences()](dateperiod.getrecurrences.html)

includestartdate

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

| Версия | Описание |
| --- | --- |
|  | Клас **DatePeriod** тепер реалізує інтерфейс [IteratorAggregate](class.iteratoraggregate.html). Раніше натомість було реалізовано інтерфейс [Traversable](class.traversable.html) |

## Зміст

-   [DatePeriod::construct](dateperiod.construct.html) — Створює новий об'єкт DatePeriod
-   [DatePeriod::getDateInterval](dateperiod.getdateinterval.html) - Повертає інтервал
-   [DatePeriod::getEndDate](dateperiod.getenddate.html) — Повертає кінцеву дату періоду
-   [DatePeriod::getRecurrences](dateperiod.getrecurrences.html) — Отримує кількість повторів
-   [DatePeriod::getStartDate](dateperiod.getstartdate.html) — Повертає початкову дату періоду