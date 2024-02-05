---
navigation:
  - datetime.sub.md: '« DateTime::sub'
  - datetimeimmutable.add.md: 'DateTimeImmutable::add »'
  - index.md: PHP Manual
  - book.datetime.md: Дата час
title: Клас DateTimeImmutable
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас DateTimeImmutable

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

## Вступ

Подання дати та часу.

Цей клас поводиться так само, як і клас [DateTime](class.datetime.md), за винятком того, що при виклику методів зміни, таких як [DateTime::modify()](datetime.modify.md)повертаються нові об'єкти.

## Огляд класів

```classsynopsis

    
     class DateTimeImmutable
    

    
     implements
      DateTimeInterface {

    /* Наследуемые константы */
    
     public
     const
     string
      DateTimeInterface::ATOM = "Y-m-d\\TH:i:sP";
public
     const
     string
      DateTimeInterface::COOKIE = "l, d-M-Y H:i:s T";
public
     const
     string
      DateTimeInterface::ISO8601 = "Y-m-d\\TH:i:sO";
public
     const
     string
      DateTimeInterface::ISO8601_EXPANDED = "X-m-d\\TH:i:sP";
public
     const
     string
      DateTimeInterface::RFC822 = "D, d M y H:i:s O";
public
     const
     string
      DateTimeInterface::RFC850 = "l, d-M-y H:i:s T";
public
     const
     string
      DateTimeInterface::RFC1036 = "D, d M y H:i:s O";
public
     const
     string
      DateTimeInterface::RFC1123 = "D, d M Y H:i:s O";
public
     const
     string
      DateTimeInterface::RFC7231 = "D, d M Y H:i:s \\G\\M\\T";
public
     const
     string
      DateTimeInterface::RFC2822 = "D, d M Y H:i:s O";
public
     const
     string
      DateTimeInterface::RFC3339 = "Y-m-d\\TH:i:sP";
public
     const
     string
      DateTimeInterface::RFC3339_EXTENDED = "Y-m-d\\TH:i:s.vP";
public
     const
     string
      DateTimeInterface::RSS = "D, d M Y H:i:s O";
public
     const
     string
      DateTimeInterface::W3C = "Y-m-d\\TH:i:sP";


    /* Методы */
    
   public __construct(string $datetime = "now", ?DateTimeZone $timezone = null)

    public add(DateInterval $interval): DateTimeImmutable
public static createFromFormat(string $format, string $datetime, ?DateTimeZone $timezone = null): DateTimeImmutable|false
public static createFromInterface(DateTimeInterface $object): DateTimeImmutable
public static createFromMutable(DateTime $object): static
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

| Версия | Опис |
| --- | --- |
| 7.1.0 | Конструктор класу **DateTimeImmutable** тепер включає поточні мікросекунди. До цього він завжди ініціалізував мікросекунди зі значенням |

## Зміст

-   [DateTimeImmutable::add](datetimeimmutable.add.md)— Повертає новий об'єкт із доданою кількістю днів, місяців, років, годин, хвилин та секунд
-   [DateTimeImmutable::\_\_construct](datetimeimmutable.construct.md)— Повертає новий об'єкт DateTimeImmutable
-   [DateTimeImmutable::createFromFormat](datetimeimmutable.createfromformat.md)— Розбирає рядок із датою згідно з вказаним форматом
-   [DateTimeImmutable::createFromInterface](datetimeimmutable.createfrominterface.md)— Повертає новий об'єкт DateTimeImmutable, створений із переданого об'єкта, що реалізує інтерфейс DateTimeInterface
-   [DateTimeImmutable::createFromMutable](datetimeimmutable.createfrommutable.md)— Повертає новий екземпляр DateTimeImmutable, що містить заданий об'єкт DateTime
-   [DateTimeImmutable::getLastErrors](datetimeimmutable.getlasterrors.md)— Повертає попередження та помилки
-   [DateTimeImmutable::modify](datetimeimmutable.modify.md)— Створює новий об'єкт із зміненою тимчасовою міткою
-   [DateTimeImmutable::\_\_set\_state](datetimeimmutable.set-state.md) \- Обробник\_\_set\_state
-   [DateTimeImmutable::setDate](datetimeimmutable.setdate.md) \- Встановлює дату
-   [DateTimeImmutable::setISODate](datetimeimmutable.setisodate.md)— Встановлює дату ISO
-   [DateTimeImmutable::setTime](datetimeimmutable.settime.md) \- Встановлює час
-   [DateTimeImmutable::setTimestamp](datetimeimmutable.settimestamp.md)— Встановлює дату та час на основі мітки часу Unix
-   [DateTimeImmutable::setTimezone](datetimeimmutable.settimezone.md) \- Встановлює часовий пояс
-   [DateTimeImmutable::sub](datetimeimmutable.sub.md)— Віднімає передану кількість днів, місяців, років, годин, хвилин та секунд
