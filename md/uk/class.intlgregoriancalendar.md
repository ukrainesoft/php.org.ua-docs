- [« IntlCalendar::toDateTime](intlcalendar.todatetime.md)
- [IntlGregorianCalendar::\_\_construct »](intlgregoriancalendar.construct.md)

- [PHP Manual](index.md)
- [intl](book.intl.md)
- Клас IntlGregorianCalendar

# Клас IntlGregorianCalendar

(PHP 5 \>= 5.5.0, PHP 7, PHP 8)

## Вступ

## Огляд класів

class **IntlGregorianCalendar** extends
[IntlCalendar](class.intlcalendar.md) {

/\* Успадковані константи \*/

const int `IntlCalendar::FIELD_ERA` = 0;

const int `IntlCalendar::FIELD_YEAR` = 1;

const int `IntlCalendar::FIELD_MONTH` = 2;

const int `IntlCalendar::FIELD_WEEK_OF_YEAR` = 3;

const int `IntlCalendar::FIELD_WEEK_OF_MONTH` = 4;

const int `IntlCalendar::FIELD_DATE` = 5;

const int `IntlCalendar::FIELD_DAY_OF_YEAR` = 6;

const int `IntlCalendar::FIELD_DAY_OF_WEEK` = 7;

const int `IntlCalendar::FIELD_DAY_OF_WEEK_IN_MONTH` = 8;

const int `IntlCalendar::FIELD_AM_PM` = 9;

const int `IntlCalendar::FIELD_HOUR` = 10;

const int `IntlCalendar::FIELD_HOUR_OF_DAY` = 11;

const int `IntlCalendar::FIELD_MINUTE` = 12;

const int `IntlCalendar::FIELD_SECOND` = 13;

const int `IntlCalendar::FIELD_MILLISECOND` = 14;

const int `IntlCalendar::FIELD_ZONE_OFFSET` = 15;

const int `IntlCalendar::FIELD_DST_OFFSET` = 16;

const int `IntlCalendar::FIELD_YEAR_WOY` = 17;

const int `IntlCalendar::FIELD_DOW_LOCAL` = 18;

const int `IntlCalendar::FIELD_EXTENDED_YEAR` = 19;

const int `IntlCalendar::FIELD_JULIAN_DAY` = 20;

const int `IntlCalendar::FIELD_MILLISECONDS_IN_DAY` = 21;

const int `IntlCalendar::FIELD_IS_LEAP_MONTH` = 22;

const int `IntlCalendar::FIELD_FIELD_COUNT` = 23;

const int `IntlCalendar::FIELD_DAY_OF_MONTH` = 5;

const int `IntlCalendar::DOW_SUNDAY` = 1;

const int `IntlCalendar::DOW_MONDAY` = 2;

const int `IntlCalendar::DOW_TUESDAY` = 3;

const int `IntlCalendar::DOW_WEDNESDAY` = 4;

const int `IntlCalendar::DOW_THURSDAY` = 5;

const int `IntlCalendar::DOW_FRIDAY` = 6;

const int `IntlCalendar::DOW_SATURDAY` = 7;

const int `IntlCalendar::DOW_TYPE_WEEKDAY` = 0;

const int `IntlCalendar::DOW_TYPE_WEEKEND` = 1;

const int `IntlCalendar::DOW_TYPE_WEEKEND_OFFSET` = 2;

const int `IntlCalendar::DOW_TYPE_WEEKEND_CEASE` = 3;

const int `IntlCalendar::WALLTIME_FIRST` = 1;

const int `IntlCalendar::WALLTIME_LAST` = 0;

const int `IntlCalendar::WALLTIME_NEXT_VALID` = 2;

/\* Методи \*/

public
[\_\_construct](intlgregoriancalendar.construct.md)([IntlTimeZone](class.intltimezone.md)
`$tz` = ?, string `$locale` = ?)

public [\_\_construct](intlgregoriancalendar.construct.md)(int
`$timeZoneOrYear`, int `$localeOrMonth`, int `$dayOfMonth`)

public [\_\_construct](intlgregoriancalendar.construct.md)(
int `$timeZoneOrYear`,
int `$localeOrMonth`,
int `$dayOfMonth`,
int `$hour`,
int `$minute`,
int `$second` = ?
)

public
[getGregorianChange](intlgregoriancalendar.getgregorianchange.md)():
float

public [isLeapYear](intlgregoriancalendar.isleapyear.md)(int `$year`):
bool

public
[setGregorianChange](intlgregoriancalendar.setgregorianchange.md)(float
`$timestamp`): bool

/\* Наслідувані методи \*/

public [IntlCalendar::add](intlcalendar.add.md)(int `$field`, int
`$value`): bool

public
[IntlCalendar::after](intlcalendar.after.md)([IntlCalendar](class.intlcalendar.md)
`$other`): bool

public
[IntlCalendar::before](intlcalendar.before.md)([IntlCalendar](class.intlcalendar.md)
`$other`): bool

public [IntlCalendar::clear](intlcalendar.clear.md)(?int `$field` =
**`null`**): bool

public static
[IntlCalendar::createInstance](intlcalendar.createinstance.md)([IntlTimeZone](class.intltimezone.md)\|[DateTimeZone](class.datetimezone.md)\|string\|null
`$timezone` = **`null`**, ?string `$locale` = **`null`**):
?[IntlCalendar](class.intlcalendar.md)

public
[IntlCalendar::equals](intlcalendar.equals.md)([IntlCalendar](class.intlcalendar.md)
`$other`): bool

public
[IntlCalendar::fieldDifference](intlcalendar.fielddifference.md)(float
`$timestamp`, int `$field`): int\|false

public static
[IntlCalendar::fromDateTime](intlcalendar.fromdatetime.md)([DateTime](class.datetime.md)\|string
`$datetime`, ?string `$locale` = **`null`**):
?[IntlCalendar](class.intlcalendar.md)

public [IntlCalendar::get](intlcalendar.get.md)(int `$field`):
int\|false

public
[IntlCalendar::getActualMaximum](intlcalendar.getactualmaximum.md)(int
`$field`): int\|false

public
[IntlCalendar::getActualMinimum](intlcalendar.getactualminimum.md)(int
`$field`): int\|false

public static
[IntlCalendar::getAvailableLocales](intlcalendar.getavailablelocales.md)():
array

public
[IntlCalendar::getDayOfWeekType](intlcalendar.getdayofweektype.md)(int
`$dayOfWeek`): int\|false

public [IntlCalendar::getErrorCode](intlcalendar.geterrorcode.md)():
int\|false

public
[IntlCalendar::getErrorMessage](intlcalendar.geterrormessage.md)():
string\|false

public
[IntlCalendar::getFirstDayOfWeek](intlcalendar.getfirstdayofweek.md)():
int\|false

public
[IntlCalendar::getGreatestMinimum](intlcalendar.getgreatestminimum.md)(int
`$field`): int\|false

public static
[IntlCalendar::getKeywordValuesForLocale](intlcalendar.getkeywordvaluesforlocale.md)(string
`$keyword`, string `$locale`, bool `$onlyCommon`):
[IntlIterator](class.intliterator.md)\|false

public
[IntlCalendar::getLeastMaximum](intlcalendar.getleastmaximum.md)(int
`$field`): int\|false

public [IntlCalendar::getLocale](intlcalendar.getlocale.md)(int
`$type`): string\|false

public [IntlCalendar::getMaximum](intlcalendar.getmaximum.md)(int
`$field`): int\|false

public
[IntlCalendar::getMinimalDaysInFirstWeek](intlcalendar.getminimaldaysinfirstweek.md)():
int\|false

public [IntlCalendar::getMinimum](intlcalendar.getminimum.md)(int
`$field`): int\|false

public static [IntlCalendar::getNow](intlcalendar.getnow.md)(): float

public
[IntlCalendar::getRepeatedWallTimeOption](intlcalendar.getrepeatedwalltimeoption.md)():
int

public
[IntlCalendar::getSkippedWallTimeOption](intlcalendar.getskippedwalltimeoption.md)():
int

public [IntlCalendar::getTime](intlcalendar.gettime.md)():
float\|false

public [IntlCalendar::getTimeZone](intlcalendar.gettimezone.md)():
[IntlTimeZone](class.intltimezone.md)\|false

public [IntlCalendar::getType](intlcalendar.gettype.md)(): string

public
[IntlCalendar::getWeekendTransition](intlcalendar.getweekendtransition.md)(int
`$dayOfWeek`): int\|false

public
[IntlCalendar::inDaylightTime](intlcalendar.indaylighttime.md)(): bool

public
[IntlCalendar::isEquivalentTo](intlcalendar.isequivalentto.md)([IntlCalendar](class.intlcalendar.md)
`$other`): bool

public [IntlCalendar::isLenient](intlcalendar.islenient.md)(): bool

public [IntlCalendar::isSet](intlcalendar.isset.md)(int `$field`):
bool

public [IntlCalendar::isWeekend](intlcalendar.isweekend.md)(?float
`$timestamp` = **`null`**): bool

public [IntlCalendar::roll](intlcalendar.roll.md)(int `$field`,
int\|bool `$value`): bool

public [IntlCalendar::set](intlcalendar.set.md)(int `$field`, int
`$value`): bool

public [IntlCalendar::set](intlcalendar.set.md)(
int `$year`,
int `$month`,
int `$dayOfMonth` = NULL,
int `$hour` = NULL,
int `$minute` = NULL,
int `$second` = NULL
): bool

public
[IntlCalendar::setFirstDayOfWeek](intlcalendar.setfirstdayofweek.md)(int
`$dayOfWeek`): bool

public [IntlCalendar::setLenient](intlcalendar.setlenient.md)(bool
`$lenient`): bool

public
[IntlCalendar::setMinimalDaysInFirstWeek](intlcalendar.setminimaldaysinfirstweek.md)(int
`$days`): bool

public
[IntlCalendar::setRepeatedWallTimeOption](intlcalendar.setrepeatedwalltimeoption.md)(int
`$option`): bool

public
[IntlCalendar::setSkippedWallTimeOption](intlcalendar.setskippedwalltimeoption.md)(int
`$option`): bool

public [IntlCalendar::setTime](intlcalendar.settime.md)(float
`$timestamp`): bool

public
[IntlCalendar::setTimeZone](intlcalendar.settimezone.md)([IntlTimeZone](class.intltimezone.md)\|[DateTimeZone](class.datetimezone.md)\|string\|null
`$timezone`): bool

public [IntlCalendar::toDateTime](intlcalendar.todatetime.md)():
[DateTime](class.datetime.md)\|false

}

## Зміст

- [IntlGregorianCalendar::\_\_construct](intlgregoriancalendar.construct.md)
- Конструктор класу григоріанського календаря
- [IntlGregorianCalendar::getGregorianChange](intlgregoriancalendar.getgregorianchange.md)
— Отримує дату зміни григоріанського календаря
- [IntlGregorianCalendar::isLeapYear](intlgregoriancalendar.isleapyear.md)
— Визначає, чи цей рік є високосним.
- [IntlGregorianCalendar::setGregorianChange](intlgregoriancalendar.setgregorianchange.md)
— Встановлює дату зміни у григоріанському календарі
