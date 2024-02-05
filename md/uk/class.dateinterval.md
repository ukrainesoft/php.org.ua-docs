---
navigation:
  - datetimezone.listidentifiers.md: '« DateTimeZone::listIdentifiers'
  - dateinterval.construct.md: 'DateInterval::\_\_construct »'
  - index.md: PHP Manual
  - book.datetime.md: Дата час
title: Клас DateInterval
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас DateInterval

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

## Вступ

Подає інтервали дат.

Інтервал дат зберігає або певний фіксований час (у роках, місяцях, днях, годинах тощо) або відносний рядок часу у форматі, який підтримує конструктор [DateTimeImmutable](class.datetimeimmutable.md) і [DateTime](class.datetime.md)

Більш конкретно, інформація в об'єкті класу **DateInterval** є інструкцією для переходу від однієї дати/часу до іншої дати/часу. Цей процес не завжди оборотний.

Найпоширенішим способом створення об'єкта **DateInterval** є обчислення різниці між двома об'єктами дати/часу за допомогою [DateTimeInterface::diff()](datetime.diff.md)

Оскільки не існує чітко визначеного способу порівняння інтервалів дат, екземпляри **DateInterval**являются[незрівнянними](language.operators.comparison.md#language.operators.comparison.incomparable)

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

**Увага**

Доступні властивості, наведені нижче, залежать від версії PHP і повинні розглядатися як *доступні лише для читання*

y

Кількість років.

m

Кількість місяців.

d

Кількість днів.

h

Кількість годин.

i

Кількість хвилин.

s

Кількість секунд.

f

Кількість мікросекунд у вигляді часток секунди.

invert

Приймає , якщо інтервал представляє негативний період часу та в іншому випадку. Дивіться [DateInterval::format()](dateinterval.format.md)

days

Якщо об'єкт DateInterval створено методом [DateTimeImmutable::diff()](datetime.diff.md) або [DateTime::diff()](datetime.diff.md), то це загальна кількість повних днів між початковою та кінцевою датами В іншому випадку days прийме значення **`false`**

from\_string

Якщо об'єкт DateInterval був створений методом [DateInterval::createFromDateString()](dateinterval.createfromdatestring.md), то значение свойства будет\*\*`true`**и свойство date\_string будет заполнено. В противном случае значение свойства будет**`false`\*\* та властивості від y до f, invert та days будуть заповнені.

date\_string

Строка, используемая в качестве аргумента метода[DateInterval::createFromDateString()](dateinterval.createfromdatestring.md)

## список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Додані властивості from\_string та date\_string для екземплярів **DateInterval**, які були створені за допомогою методу [DateInterval::createFromDateString()](dateinterval.createfromdatestring.md) |
| 8.2.0 | Буде видно тільки значення від `y`до`f` `invert`и`days` |
| 7.4.0 | Примірники **DateInterval** тепер незрівнянні; раніше всі екземпляри **DateInterval** вважалися рівними. |
| 7.1.0 | Додано властивість f. |

## Зміст

-   [DateInterval::\_\_construct](dateinterval.construct.md)— Створює новий об'єкт DateInterval
-   [DateInterval::createFromDateString](dateinterval.createfromdatestring.md)— Створює об'єкт класу DateInterval із дати у відносному форматі
-   [DateInterval::format](dateinterval.format.md) \- Форматує інтервал
