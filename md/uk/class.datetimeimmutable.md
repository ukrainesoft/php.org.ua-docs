Клас DateTimeImmutable

-   [« DateTime::sub](datetime.sub.html)
    
-   [DateTimeImmutable::add »](datetimeimmutable.add.html)
    
-   [PHP Manual](index.html)
    
-   [Дата/время](book.datetime.html)
    
-   Клас DateTimeImmutable
    

# Клас DateTimeImmutable

(PHP 5> = 5.5.0, PHP 7, PHP 8)

## Вступ

Подання дати та часу.

Цей клас поводиться так само, як і клас [DateTime](class.datetime.html), за винятком того, що при виклику методів зміни, таких як [DateTime::modify()](datetime.modify.html)повертаються нові об'єкти.

## Огляд класів

```classsynopsis

     
    

    
     
      class DateTimeImmutable
     

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

    public add(DateInterval $interval): DateTimeImmutable
public static createFromFormat(string $format, string $datetime, ?DateTimeZone $timezone = null): DateTimeImmutable|false
public static createFromInterface(DateTimeInterface $object): DateTimeImmutable
public static createFromMutable(DateTime $object): DateTimeImmutable
public static getLastErrors(): array|false
public modify(string $modifier): DateTimeImmutable|false
public static __set_state(array $array): DateTimeImmutable
public setDate(int $year, int $month, int $day): DateTimeImmutable
public setISODate(int $year, int $week, int $dayOfWeek = 1): DateTimeImmutable
public setTime(    int $hour,    int $minute,    int $second = 0,    int $microsecond = 0): DateTimeImmutable
public setTimestamp(int $timestamp): DateTimeImmutable
public setTimezone(DateTimeZone $timezone): DateTimeImmutable
public sub(DateInterval $interval): DateTimeImmutable

    public diff(DateTimeInterface $targetObject, bool $absolute = false): DateInterval
public format(string $format): string
public getOffset(): int
public getTimestamp(): int
public getTimezone(): DateTimeZone|false
public __wakeup(): void

   }
```

## список змін

| Версия | Описание                                                                                                                                    |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------|
|        | Конструктор класу **DateTimeImmutable** тепер включає поточні мікросекунди. До цього він завжди ініціалізував мікросекунди зі значенням `0` |

## Зміст

-   [DateTimeImmutable::add](datetimeimmutable.add.html) — Повертає новий об'єкт із доданою кількістю днів, місяців, років, годин, хвилин та секунд
-   [DateTimeImmutable::construct](datetimeimmutable.construct.html) — Повертає новий об'єкт DateTimeImmutable
-   [DateTimeImmutable::createFromFormat](datetimeimmutable.createfromformat.html) — Розбирає рядок із датою згідно з вказаним форматом
-   [DateTimeImmutable::createFromInterface](datetimeimmutable.createfrominterface.html) — Повертає новий об'єкт DateTimeImmutable, створений із переданого об'єкта, що реалізує інтерфейс DateTimeInterface
-   [DateTimeImmutable::createFromMutable](datetimeimmutable.createfrommutable.html) — Повертає новий об'єкт DateTimeImmutable, що містить заданий об'єкт DateTime
-   [DateTimeImmutable::getLastErrors](datetimeimmutable.getlasterrors.html) — Повертає попередження та помилки
-   [DateTimeImmutable::modify](datetimeimmutable.modify.html) — Створює новий об'єкт із зміненою тимчасовою міткою
-   [DateTimeImmutable::setstate](datetimeimmutable.set-state.html) - Обробник setstate
-   [DateTimeImmutable::setDate](datetimeimmutable.setdate.html) - Встановлює дату
-   [DateTimeImmutable::setISODate](datetimeimmutable.setisodate.html) — Встановлює дату ISO
-   [DateTimeImmutable::setTime](datetimeimmutable.settime.html) - Встановлює час
-   [DateTimeImmutable::setTimestamp](datetimeimmutable.settimestamp.html) — Встановлює дату та час на основі мітки часу Unix
-   [DateTimeImmutable::setTimezone](datetimeimmutable.settimezone.html) - Встановлює часовий пояс
-   [DateTimeImmutable::sub](datetimeimmutable.sub.html) — Віднімає передану кількість днів, місяців, років, годин, хвилин та секунд