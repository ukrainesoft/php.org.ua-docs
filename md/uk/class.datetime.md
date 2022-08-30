Клас DateTime

-   [« Арифметика дати/часу](datetime.examples-arithmetic.html)
    
-   [DateTime::add »](datetime.add.md)
    
-   [PHP Manual](index.md)
    
-   [Дата/время](book.datetime.md)
    
-   Клас DateTime
    

# Клас DateTime

(PHP 5> = 5.2.0, PHP 7, PHP 8)

## Вступ

Подання дати та часу.

Клас поводиться так само, як і [DateTimeImmutable](class.datetimeimmutable.md), крім того, що об'єкти модифікуються самі під час виклику таких методів модифікації, як [DateTime::modify()](datetime.modify.md)

**Увага**

Виклик методів для об'єктів класу **DateTime** змінить інформацію, укладену в цих об'єктах, якщо ви хочете запобігти цьому, вам доведеться використовувати оператор `clone` створення нового об'єкта. Використовуйте клас [DateTimeImmutable](class.datetimeimmutable.md) замість **DateTime**, щоб отримати рекомендовану поведінку за промовчанням.

## Огляд класів

```classsynopsis

     
    

    
     
      class DateTime
     

     implements 
       DateTimeInterface {

    /* Наследуемые константы */
    
     const
     string
      DateTimeInterface::ATOM = "Y-m-d\TH:i:sP";
const
     string
      DateTimeInterface::COOKIE = "l, d-M-Y H:i:s T";
const
     string
      DateTimeInterface::ISO8601 = "Y-m-d\TH:i:sO";
const
     string
      DateTimeInterface::ISO8601_EXPANDED = "X-m-d\TH:i:sP";
const
     string
      DateTimeInterface::RFC822 = "D, d M y H:i:s O";
const
     string
      DateTimeInterface::RFC850 = "l, d-M-y H:i:s T";
const
     string
      DateTimeInterface::RFC1036 = "D, d M y H:i:s O";
const
     string
      DateTimeInterface::RFC1123 = "D, d M Y H:i:s O";
const
     string
      DateTimeInterface::RFC7231 = "D, d M Y H:i:s \G\M\T";
const
     string
      DateTimeInterface::RFC2822 = "D, d M Y H:i:s O";
const
     string
      DateTimeInterface::RFC3339 = "Y-m-d\TH:i:sP";
const
     string
      DateTimeInterface::RFC3339_EXTENDED = "Y-m-d\TH:i:s.vP";
const
     string
      DateTimeInterface::RSS = "D, d M Y H:i:s O";
const
     string
      DateTimeInterface::W3C = "Y-m-d\TH:i:sP";


    /* Методы */
    
   public __construct(string $datetime = "now", ?DateTimeZone $timezone = null)

    public add(DateInterval $interval): DateTime
public static createFromFormat(string $format, string $datetime, ?DateTimeZone $timezone = null): DateTime|false
public static createFromImmutable(DateTimeImmutable $object): DateTime
public static createFromInterface(DateTimeInterface $object): DateTime
public static getLastErrors(): array|false
public modify(string $modifier): DateTime|false
public static __set_state(array $array): DateTime
public setDate(int $year, int $month, int $day): DateTime
public setISODate(int $year, int $week, int $dayOfWeek = 1): DateTime
public setTime(    int $hour,    int $minute,    int $second = 0,    int $microsecond = 0): DateTime
public setTimestamp(int $timestamp): DateTime
public setTimezone(DateTimeZone $timezone): DateTime
public sub(DateInterval $interval): DateTime

    public diff(DateTimeInterface $targetObject, bool $absolute = false): DateInterval
public format(string $format): string
public getOffset(): int
public getTimestamp(): int
public getTimezone(): DateTimeZone|false
public __wakeup(): void

  }
```

## список змін

| Версия | Описание                                                                                                                           |
|--------|------------------------------------------------------------------------------------------------------------------------------------|
|        | Константи класу тепер **DateTime** визначено в [DateTimeInterface](class.datetimeinterface.md)                                     |
|        | Конструктор класу **DateTime** тепер включає поточні мікросекунди. До цього він завжди ініціалізував мікросекунди зі значенням `0` |

## Зміст

-   [DateTime::add](datetime.add.md) — Змінює об'єкт DateTime, додаючи кількість днів, місяців, років, годин, хвилин та секунд
-   [DateTime::construct](datetime.construct.md) - Конструктор класу DateTime
-   [DateTime::createFromFormat](datetime.createfromformat.md) — Розбирає рядок із датою згідно з вказаним форматом
-   [DateTime::createFromImmutable](datetime.createfromimmutable.md) — Повертає об'єкт DateTime інкапсулюючий заданий об'єкт DateTimeImmutable
-   [DateTime::createFromInterface](datetime.createfrominterface.md) — Повертає новий об'єкт DateTime, створений із переданого об'єкта, який реалізує інтерфейс DateTimeInterface
-   [DateTime::getLastErrors](datetime.getlasterrors.md) — Повертає попередження та помилки
-   [DateTime::modify](datetime.modify.md) - Зміна тимчасової мітки
-   [DateTime::setstate](datetime.set-state.html) - Обробник setstate
-   [DateTime::setDate](datetime.setdate.md) - Встановлює дату
-   [DateTime::setISODate](datetime.setisodate.md) — Встановлює дату ISO
-   [DateTime::setTime](datetime.settime.md) - Встановлює час
-   [DateTime::setTimestamp](datetime.settimestamp.md) — Встановлює дату та час на основі мітки часу Unix
-   [DateTime::setTimezone](datetime.settimezone.md) — Встановлює часовий пояс для об'єкта класу DateTime
-   [DateTime::sub](datetime.sub.md) — Змінює вказаний об'єкт DateTime, віднімаючи вказаний об'єкт DateInterval.