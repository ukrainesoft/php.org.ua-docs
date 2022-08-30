Клас DateInterval

-   [« DateTimeZone::listIdentifiers](datetimezone.listidentifiers.html)
    
-   [DateInterval::construct »](dateinterval.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Дата/время](book.datetime.html)
    
-   Клас DateInterval
    

# Клас DateInterval

(PHP 5> = 5.3.0, PHP 7, PHP 8)

## Вступ

Надає інтервали дат.

Інтервал дат зберігає або певний фіксований час (у роках, місяцях, днях, годинах тощо) або відносний рядок часу у форматі, який підтримує конструктор [DateTimeImmutable](class.datetimeimmutable.html) і [DateTime](class.datetime.html)

Більш конкретно, інформація в об'єкті класу **DateInterval** є інструкцією для переходу від однієї дати/часу до іншої дати/часу. Цей процес не завжди оборотний.

Найпоширенішим способом створення об'єкта **DateInterval** є обчислення різниці між двома об'єктами дати/часу за допомогою [DateTimeInterface::diff()](datetime.diff.html)

Оскільки не існує чітко визначеного способу порівняння інтервалів дат, екземпляри **DateInterval** є [несравнимыми](language.operators.comparison.html#language.operators.comparison.incomparable)

## Огляд класів

```classsynopsis

     
    

    
     
      class DateInterval
     
     {

    /* Свойства */
    
     public
     int
      $y;

    public
     int
      $m;

    public
     int
      $d;

    public
     int
      $h;

    public
     int
      $i;

    public
     int
      $s;

    public
     float
      $f;

    public
     int
      $invert;

    public
     mixed
      $days;

    public
     bool
      $from_string;

    public
     string
      $date_string;


    /* Методы */
    
   public __construct(string $duration)

    public static createFromDateString(string $datetime): DateInterval|false
public format(string $format): string

   }
```

## Властивості

і

Кількість років.

м

Кількість місяців.

д

Кількість днів.

х

Кількість годин.

і

Кількість хвилин.

з

Кількість секунд.

ф

Кількість мікросекунд у вигляді часток секунди.

invert

Приймає `1`, якщо інтервал представляє негативний період часу та `0` в іншому випадку. Дивіться [DateInterval::format()](dateinterval.format.html)

days

Якщо об'єкт DateInterval створено методом [DateTimeImmutable::diff()](datetime.diff.html) або [DateTime::diff()](datetime.diff.html), то це сумарне число днів між початковою та кінцевою датами. В іншому випадку days прийме значення **`false`**

fromstring

Якщо об'єкт DateInterval був створений методом [DateInterval::createFromDateString()](dateinterval.createfromdatestring.html), то значення властивості буде **`true`** і властивість datestring буде заповнено. В іншому випадку значення властивості буде **`false`** та властивості від y до f, invert та days будуть заповнені.

datestring

Рядок, що використовується як аргумент методу [DateInterval::createFromDateString()](dateinterval.createfromdatestring.html)

## список змін

| Версия | Описание                                                                                                                                                                                           |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Додані властивості fromstring та datestring для екземплярів **DateInterval**, які були створені за допомогою методу [DateInterval::createFromDateString()](dateinterval.createfromdatestring.html) |
|        | Примірники **DateInterval** тепер незрівнянні; раніше всі екземпляри **DateInterval** вважалися рівними.                                                                                           |
|        | Додано властивість f.                                                                                                                                                                              |

## Зміст

-   [DateInterval::construct](dateinterval.construct.html) — Створює новий об'єкт DateInterval
-   [DateInterval::createFromDateString](dateinterval.createfromdatestring.html) — Створює об'єкт класу DateInterval із дати у відносному форматі
-   [DateInterval::format](dateinterval.format.html) - Форматує інтервал