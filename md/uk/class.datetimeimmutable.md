- [« DateTime::sub](datetime.sub.md)
- [DateTimeImmutable::add »](datetimeimmutable.add.md)

- [PHP Manual](index.md)
- [Дата/час](book.datetime.md)
- Клас DateTimeImmutable

# Клас DateTimeImmutable

(PHP 5 \>= 5.5.0, PHP 7, PHP 8)

## Вступ

Подання дати та часу.

Цей клас поводиться так само, як і клас
[DateTime](class.datetime.md), за винятком того, що під час виклику
методів зміни, таких як [DateTime::modify()](datetime.modify.md),
повертаються нові об'єкти.

## Огляд класів

class **DateTimeImmutable** implements
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

public [\_\_construct](datetimeimmutable.construct.md)(string
`$datetime` = "now", ?[DateTimeZone](class.datetimezone.md)
`$timezone` = **`null`**)

public
[add](datetimeimmutable.add.md)([DateInterval](class.dateinterval.md)
`$interval`): [DateTimeImmutable](class.datetimeimmutable.md)

public static
[createFromFormat](datetimeimmutable.createfromformat.md)(string
`$format`, string `$datetime`, ?[DateTimeZone](class.datetimezone.md)
`$timezone` = **`null`**):
[DateTimeImmutable](class.datetimeimmutable.md)\|false

public static
[createFromInterface](datetimeimmutable.createfrominterface.md)([DateTimeInterface](class.datetimeinterface.md)
`$object`): [DateTimeImmutable](class.datetimeimmutable.md)

public static
[createFromMutable](datetimeimmutable.createfrommutable.md)([DateTime](class.datetime.md)
`$object`): [DateTimeImmutable](class.datetimeimmutable.md)

public static [getLastErrors](datetimeimmutable.getlasterrors.md)():
array\|false

public [modify](datetimeimmutable.modify.md)(string `$modifier`):
[DateTimeImmutable](class.datetimeimmutable.md)\|false

public static [\_\_set_state](datetimeimmutable.set-state.md)(array
`$array`): [DateTimeImmutable](class.datetimeimmutable.md)

public [setDate](datetimeimmutable.setdate.md)(int `$year`, int
`$month`, int `$day`): [DateTimeImmutable](class.datetimeimmutable.md)

public [setISODate](datetimeimmutable.setisodate.md)(int `$year`, int
`$week`, int `$dayOfWeek` = 1):
[DateTimeImmutable](class.datetimeimmutable.md)

public [setTime](datetimeimmutable.settime.md)(
int `$hour`,
int `$minute`,
int `$second` = 0,
int `$microsecond` = 0
): [DateTimeImmutable](class.datetimeimmutable.md)

public [setTimestamp](datetimeimmutable.settimestamp.md)(int
`$timestamp`): [DateTimeImmutable](class.datetimeimmutable.md)

public
[setTimezone](datetimeimmutable.settimezone.md)([DateTimeZone](class.datetimezone.md)
`$timezone`): [DateTimeImmutable](class.datetimeimmutable.md)

public
[sub](datetimeimmutable.sub.md)([DateInterval](class.dateinterval.md)
`$interval`): [DateTimeImmutable](class.datetimeimmutable.md)

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

## Зміст

- [DateTimeImmutable::add](datetimeimmutable.add.md) — Повертає
новий об'єкт з доданою кількістю днів, місяців, років, годин,
хвилин та секунд
- [DateTimeImmutable::\_\_construct](datetimeimmutable.construct.md)
— Повертає новий об'єкт DateTimeImmutable
- [DateTimeImmutable::createFromFormat](datetimeimmutable.createfromformat.md)
— Розбирає рядок із датою згідно з вказаним форматом
- [DateTimeImmutable::createFromInterface](datetimeimmutable.createfrominterface.md)
— Повертає новий об'єкт DateTimeImmutable, створений з
переданого об'єкта, що реалізує інтерфейс DateTimeInterface
- [DateTimeImmutable::createFromMutable](datetimeimmutable.createfrommutable.md)
— Повертає новий об'єкт DateTimeImmutable, що містить заданий
об'єкт DateTime
- [DateTimeImmutable::getLastErrors](datetimeimmutable.getlasterrors.md)
— Повертає попередження та помилки
- [DateTimeImmutable::modify](datetimeimmutable.modify.md) — Створює
новий об'єкт із зміненою тимчасовою міткою
- [DateTimeImmutable::\_\_set_state](datetimeimmutable.set-state.md)
- Обробник \_\_set_state
- [DateTimeImmutable::setDate](datetimeimmutable.setdate.md) -
Встановлює дату
- [DateTimeImmutable::setISODate](datetimeimmutable.setisodate.md) -
Встановлює дату у форматі ISO
- [DateTimeImmutable::setTime](datetimeimmutable.settime.md) -
Встановлює час
- [DateTimeImmutable::setTimestamp](datetimeimmutable.settimestamp.md)
— Встановлює дату та час на основі позначки часу Unix
- [DateTimeImmutable::setTimezone](datetimeimmutable.settimezone.md)
- Встановлює часовий пояс
- [DateTimeImmutable::sub](datetimeimmutable.sub.md) — Віднімає
передана кількість днів, місяців, років, годин, хвилин та секунд
