Клас IntlGregorianCalendar

-   [« IntlCalendar::toDateTime](intlcalendar.todatetime.md)
    
-   [IntlGregorianCalendar::construct »](intlgregoriancalendar.construct.md)
    
-   [PHP Manual](index.md)
    
-   [intl](book.intl.md)
    
-   Клас IntlGregorianCalendar
    

# Клас IntlGregorianCalendar

(PHP 5> = 5.5.0, PHP 7, PHP 8)

## Вступ

## Огляд класів

```classsynopsis

     
    

    
     
      class IntlGregorianCalendar
     

     
      extends
       IntlCalendar
     
     {

    /* Наследуемые константы */
    
     const
     int
      IntlCalendar::FIELD_ERA = 0;
const
     int
      IntlCalendar::FIELD_YEAR = 1;
const
     int
      IntlCalendar::FIELD_MONTH = 2;
const
     int
      IntlCalendar::FIELD_WEEK_OF_YEAR = 3;
const
     int
      IntlCalendar::FIELD_WEEK_OF_MONTH = 4;
const
     int
      IntlCalendar::FIELD_DATE = 5;
const
     int
      IntlCalendar::FIELD_DAY_OF_YEAR = 6;
const
     int
      IntlCalendar::FIELD_DAY_OF_WEEK = 7;
const
     int
      IntlCalendar::FIELD_DAY_OF_WEEK_IN_MONTH = 8;
const
     int
      IntlCalendar::FIELD_AM_PM = 9;
const
     int
      IntlCalendar::FIELD_HOUR = 10;
const
     int
      IntlCalendar::FIELD_HOUR_OF_DAY = 11;
const
     int
      IntlCalendar::FIELD_MINUTE = 12;
const
     int
      IntlCalendar::FIELD_SECOND = 13;
const
     int
      IntlCalendar::FIELD_MILLISECOND = 14;
const
     int
      IntlCalendar::FIELD_ZONE_OFFSET = 15;
const
     int
      IntlCalendar::FIELD_DST_OFFSET = 16;
const
     int
      IntlCalendar::FIELD_YEAR_WOY = 17;
const
     int
      IntlCalendar::FIELD_DOW_LOCAL = 18;
const
     int
      IntlCalendar::FIELD_EXTENDED_YEAR = 19;
const
     int
      IntlCalendar::FIELD_JULIAN_DAY = 20;
const
     int
      IntlCalendar::FIELD_MILLISECONDS_IN_DAY = 21;
const
     int
      IntlCalendar::FIELD_IS_LEAP_MONTH = 22;
const
     int
      IntlCalendar::FIELD_FIELD_COUNT  = 23;
const
     int
      IntlCalendar::FIELD_DAY_OF_MONTH = 5;
const
     int
      IntlCalendar::DOW_SUNDAY = 1;
const
     int
      IntlCalendar::DOW_MONDAY = 2;
const
     int
      IntlCalendar::DOW_TUESDAY = 3;
const
     int
      IntlCalendar::DOW_WEDNESDAY = 4;
const
     int
      IntlCalendar::DOW_THURSDAY = 5;
const
     int
      IntlCalendar::DOW_FRIDAY = 6;
const
     int
      IntlCalendar::DOW_SATURDAY = 7;
const
     int
      IntlCalendar::DOW_TYPE_WEEKDAY = 0;
const
     int
      IntlCalendar::DOW_TYPE_WEEKEND = 1;
const
     int
      IntlCalendar::DOW_TYPE_WEEKEND_OFFSET = 2;
const
     int
      IntlCalendar::DOW_TYPE_WEEKEND_CEASE = 3;
const
     int
      IntlCalendar::WALLTIME_FIRST = 1;
const
     int
      IntlCalendar::WALLTIME_LAST = 0;
const
     int
      IntlCalendar::WALLTIME_NEXT_VALID = 2;


    /* Методы */
    
   public __construct(IntlTimeZone $tz = ?, string $locale = ?)
public __construct(int $timeZoneOrYear, int $localeOrMonth, int $dayOfMonth)
public __construct(    int $timeZoneOrYear,    int $localeOrMonth,    int $dayOfMonth,    int $hour,    int $minute,    int $second = ?)

    public getGregorianChange(): float
public isLeapYear(int $year): bool
public setGregorianChange(float $timestamp): bool


    /* Наследуемые методы */
    public IntlCalendar::add(int $field, int $value): bool
public IntlCalendar::after(IntlCalendar $other): bool
public IntlCalendar::before(IntlCalendar $other): bool
public IntlCalendar::clear(?int $field = null): bool
public static IntlCalendar::createInstance(IntlTimeZone|DateTimeZone|string|null $timezone = null, ?string $locale = null): ?IntlCalendar
public IntlCalendar::equals(IntlCalendar $other): bool
public IntlCalendar::fieldDifference(float $timestamp, int $field): int|false
public static IntlCalendar::fromDateTime(DateTime|string $datetime, ?string $locale = null): ?IntlCalendar
public IntlCalendar::get(int $field): int|false
public IntlCalendar::getActualMaximum(int $field): int|false
public IntlCalendar::getActualMinimum(int $field): int|false
public static IntlCalendar::getAvailableLocales(): array
public IntlCalendar::getDayOfWeekType(int $dayOfWeek): int|false
public IntlCalendar::getErrorCode(): int|false
public IntlCalendar::getErrorMessage(): string|false
public IntlCalendar::getFirstDayOfWeek(): int|false
public IntlCalendar::getGreatestMinimum(int $field): int|false
public static IntlCalendar::getKeywordValuesForLocale(string $keyword, string $locale, bool $onlyCommon): IntlIterator|false
public IntlCalendar::getLeastMaximum(int $field): int|false
public IntlCalendar::getLocale(int $type): string|false
public IntlCalendar::getMaximum(int $field): int|false
public IntlCalendar::getMinimalDaysInFirstWeek(): int|false
public IntlCalendar::getMinimum(int $field): int|false
public static IntlCalendar::getNow(): float
public IntlCalendar::getRepeatedWallTimeOption(): int
public IntlCalendar::getSkippedWallTimeOption(): int
public IntlCalendar::getTime(): float|false
public IntlCalendar::getTimeZone(): IntlTimeZone|false
public IntlCalendar::getType(): string
public IntlCalendar::getWeekendTransition(int $dayOfWeek): int|false
public IntlCalendar::inDaylightTime(): bool
public IntlCalendar::isEquivalentTo(IntlCalendar $other): bool
public IntlCalendar::isLenient(): bool
public IntlCalendar::isSet(int $field): bool
public IntlCalendar::isWeekend(?float $timestamp = null): bool
public IntlCalendar::roll(int $field, int|bool $value): bool
public IntlCalendar::set(int $field, int $value): bool
public IntlCalendar::set(    int $year,    int $month,    int $dayOfMonth = NULL,    int $hour = NULL,    int $minute = NULL,    int $second = NULL): bool
public IntlCalendar::setFirstDayOfWeek(int $dayOfWeek): bool
public IntlCalendar::setLenient(bool $lenient): bool
public IntlCalendar::setMinimalDaysInFirstWeek(int $days): bool
public IntlCalendar::setRepeatedWallTimeOption(int $option): bool
public IntlCalendar::setSkippedWallTimeOption(int $option): bool
public IntlCalendar::setTime(float $timestamp): bool
public IntlCalendar::setTimeZone(IntlTimeZone|DateTimeZone|string|null $timezone): bool
public IntlCalendar::toDateTime(): DateTime|false

   }
```

## Зміст

-   [IntlGregorianCalendar::construct](intlgregoriancalendar.construct.md) - Конструктор класу григоріанського календаря
-   [IntlGregorianCalendar::getGregorianChange](intlgregoriancalendar.getgregorianchange.md) — Отримує дату зміни григоріанського календаря
-   [IntlGregorianCalendar::isLeapYear](intlgregoriancalendar.isleapyear.md) — Визначає, чи цей рік є високосним.
-   [IntlGregorianCalendar::setGregorianChange](intlgregoriancalendar.setgregorianchange.md) — Встановлює дату зміни у григоріанському календарі