- [«Арифметика дати/часу](datetime.examples-arithmetic.md)
- [DateTime::add »](datetime.add.md)

- [PHP Manual](index.md)
- [Дата/час](book.datetime.md)
- Клас DateTime

# Клас DateTime

(PHP 5 \>= 5.2.0, PHP 7, PHP 8)

## Вступ

Подання дати та часу.

Клас поводиться так само, як і
[DateTimeImmutable](class.datetimeimmutable.md), за винятком того,
що об'єкти модифікуються самі при виклику таких методів модифікації,
як [DateTime::modify()](datetime.modify.md).

Рекомендується використовувати клас
[DateTimeImmutable](class.datetimeimmutable.md) замість цього класу.

## Огляд класів

class **DateTime** implements
[DateTimeInterface](class.datetimeinterface.md) {

/\* Успадковані константи \*/

const string `DateTimeInterface::ATOM` = "Y-m-d\TH:i:sP";

const string `DateTimeInterface::COOKIE` = "l, d-M-Y H:i:s T";

const string `DateTimeInterface::ISO8601` = "Y-m-d\TH:i:sO";

const string `DateTimeInterface::RFC822` = "D, d M y H: i: s O";

const string `DateTimeInterface::RFC850` = "l, d-M-y H:i:s T";

const string `DateTimeInterface::RFC1036` = "D, d M y H: i: s O";

const string `DateTimeInterface::RFC1123` = "D, d MY H:i:s O";

const string `DateTimeInterface::RFC7231` = "D, d MY H:i:s \G\M\T";

const string `DateTimeInterface::RFC2822` = "D, d MY H:i:s O";

const string `DateTimeInterface::RFC3339` = "Y-m-d\TH:i:sP";

const string `DateTimeInterface::RFC3339_EXTENDED` = "Y-m-d\TH:i:s.vP";

const string `DateTimeInterface::RSS` = "D, d MY H:i:s O";

const string `DateTimeInterface::W3C` = "Y-m-d\TH:i:sP";

/\* Методи \*/

public [\_\_construct](datetime.construct.md)(string `$datetime` =
"now", ?[DateTimeZone](class.datetimezone.md) `$timezone` =
**`null`**)

public [add](datetime.add.md)([DateInterval](class.dateinterval.md)
`$interval`): [DateTime](class.datetime.md)

public static [createFromFormat](datetime.createfromformat.md)(string
`$format`, string `$datetime`, ?[DateTimeZone](class.datetimezone.md)
`$timezone` = **`null`**): [DateTime](class.datetime.md)\|false

public static
[createFromImmutable](datetime.createfromimmutable.md)([DateTimeImmutable](class.datetimeimmutable.md)
`$object`): [DateTime](class.datetime.md)

public static
[createFromInterface](datetime.createfrominterface.md)([DateTimeInterface](class.datetimeinterface.md)
`$object`): [DateTime](class.datetime.md)

public static [getLastErrors](datetime.getlasterrors.md)():
array\|false

public [modify](datetime.modify.md)(string `$modifier`):
[DateTime](class.datetime.md)\|false

public static [\_\_set_state](datetime.set-state.md)(array `$array`):
[DateTime](class.datetime.md)

public [setDate](datetime.setdate.md)(int `$year`, int `$month`, int
`$day`): [DateTime](class.datetime.md)

public [setISODate](datetime.setisodate.md)(int `$year`, int `$week`,
int `$dayOfWeek` = 1): [DateTime](class.datetime.md)

public [setTime](datetime.settime.md)(
int `$hour`,
int `$minute`,
int `$second` = 0,
int `$microsecond` = 0
): [DateTime](class.datetime.md)

public [setTimestamp](datetime.settimestamp.md)(int `$timestamp`):
[DateTime](class.datetime.md)

public
[setTimezone](datetime.settimezone.md)([DateTimeZone](class.datetimezone.md)
`$timezone`): [DateTime](class.datetime.md)

public [sub](datetime.sub.md)([DateInterval](class.dateinterval.md)
`$interval`): [DateTime](class.datetime.md)

public
[diff](datetime.diff.md)([DateTimeInterface](class.datetimeinterface.md)
`$targetObject`, bool `$absolute` = **`false`**):
[DateInterval](class.dateinterval.md)

public [format](datetime.format.md)(string `$format`): string

public [getOffset](datetime.getoffset.md)(): int

public [getTimestamp](datetime.gettimestamp.md)(): int

public [getTimezone](datetime.gettimezone.md)():
[DateTimeZone](class.datetimezone.md)\|false

public [\_\_wakeup](datetime.wakeup.md)(): void

}

## Список змін

| Версія | Опис                                                                                            |
| ------ | ----------------------------------------------------------------------------------------------- |
| 7.2.0  | Константи класу тепер **DateTime** визначені у [DateTimeInterface](class.datetimeinterface.md). |

## Зміст

- [DateTime::add](datetime.add.md) — Змінює об'єкт DateTime,
додаючи кількість днів, місяців, років, годин, хвилин та секунд
- [DateTime::\_\_construct](datetime.construct.md) - Конструктор
класу DateTime
- [DateTime::createFromFormat](datetime.createfromformat.md) -
Розбирає рядок з датою згідно з вказаним форматом
- [DateTime::createFromImmutable](datetime.createfromimmutable.md) -
Повертає об'єкт DateTime інкапсулюючий заданий об'єкт
DateTimeImmutable
- [DateTime::createFromInterface](datetime.createfrominterface.md) -
Повертає новий об'єкт DateTime, створений з переданого об'єкту,
реалізує інтерфейс DateTimeInterface
- [DateTime::getLastErrors](datetime.getlasterrors.md) — Повертає
попередження та помилки
- [DateTime::modify](datetime.modify.md) — Зміна тимчасової позначки
- [DateTime::\_\_set_state](datetime.set-state.md) - Обробник
\_\_set_state
- [DateTime::setDate](datetime.setdate.md) — Встановлює дату
- [DateTime::setISODate](datetime.setisodate.md) — Встановлює
дату у форматі ISO
- [DateTime::setTime](datetime.settime.md) — Встановлює час
- [DateTime::setTimestamp](datetime.settimestamp.md) — Встановлює
дату та час на основі мітки часу Unix
- [DateTime::setTimezone](datetime.settimezone.md) — Встановлює
часовий пояс для об'єкту класу DateTime
- [DateTime::sub](datetime.sub.md) — Віднімає задану кількість
днів, місяців, років, годин, хвилин та секунд з часу об'єкту
DateTime
