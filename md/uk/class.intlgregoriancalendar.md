---
navigation:
  - intlcalendar.todatetime.md: '« IntlCalendar::toDateTime'
  - intlgregoriancalendar.construct.md: 'IntlGregorianCalendar::\_\_construct »'
  - index.md: PHP Manual
  - book.intl.md: intl
title: Клас IntlGregorianCalendar
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас IntlGregorianCalendar

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

## Вступ

## Огляд класів

```classsynopsis

    
     class IntlGregorianCalendar
    

    
     extends
      IntlCalendar
     {

    /* Наследуемые константы */
    
     public
     const
     int
      IntlCalendar::FIELD_ERA;
public
     const
     int
      IntlCalendar::FIELD_YEAR;
public
     const
     int
      IntlCalendar::FIELD_MONTH;
public
     const
     int
      IntlCalendar::FIELD_WEEK_OF_YEAR;
public
     const
     int
      IntlCalendar::FIELD_WEEK_OF_MONTH;
public
     const
     int
      IntlCalendar::FIELD_DATE;
public
     const
     int
      IntlCalendar::FIELD_DAY_OF_YEAR;
public
     const
     int
      IntlCalendar::FIELD_DAY_OF_WEEK;
public
     const
     int
      IntlCalendar::FIELD_DAY_OF_WEEK_IN_MONTH;
public
     const
     int
      IntlCalendar::FIELD_AM_PM;
public
     const
     int
      IntlCalendar::FIELD_HOUR;
public
     const
     int
      IntlCalendar::FIELD_HOUR_OF_DAY;
public
     const
     int
      IntlCalendar::FIELD_MINUTE;
public
     const
     int
      IntlCalendar::FIELD_SECOND;
public
     const
     int
      IntlCalendar::FIELD_MILLISECOND;
public
     const
     int
      IntlCalendar::FIELD_ZONE_OFFSET;
public
     const
     int
      IntlCalendar::FIELD_DST_OFFSET;
public
     const
     int
      IntlCalendar::FIELD_YEAR_WOY;
public
     const
     int
      IntlCalendar::FIELD_DOW_LOCAL;
public
     const
     int
      IntlCalendar::FIELD_EXTENDED_YEAR;
public
     const
     int
      IntlCalendar::FIELD_JULIAN_DAY;
public
     const
     int
      IntlCalendar::FIELD_MILLISECONDS_IN_DAY;
public
     const
     int
      IntlCalendar::FIELD_IS_LEAP_MONTH;
public
     const
     int
      IntlCalendar::FIELD_FIELD_COUNT;
public
     const
     int
      IntlCalendar::FIELD_DAY_OF_MONTH;
public
     const
     int
      IntlCalendar::DOW_SUNDAY;
public
     const
     int
      IntlCalendar::DOW_MONDAY;
public
     const
     int
      IntlCalendar::DOW_TUESDAY;
public
     const
     int
      IntlCalendar::DOW_WEDNESDAY;
public
     const
     int
      IntlCalendar::DOW_THURSDAY;
public
     const
     int
      IntlCalendar::DOW_FRIDAY;
public
     const
     int
      IntlCalendar::DOW_SATURDAY;
public
     const
     int
      IntlCalendar::DOW_TYPE_WEEKDAY;
public
     const
     int
      IntlCalendar::DOW_TYPE_WEEKEND;
public
     const
     int
      IntlCalendar::DOW_TYPE_WEEKEND_OFFSET;
public
     const
     int
      IntlCalendar::DOW_TYPE_WEEKEND_CEASE;
public
     const
     int
      IntlCalendar::WALLTIME_FIRST;
public
     const
     int
      IntlCalendar::WALLTIME_LAST;
public
     const
     int
      IntlCalendar::WALLTIME_NEXT_VALID;


    /* Методы */
    
   public __construct(IntlTimeZone $tz = ?, string $locale = ?)
public __construct(int $timeZoneOrYear, int $localeOrMonth, int $dayOfMonth)
public __construct(    int $timeZoneOrYear,    int $localeOrMonth,    int $dayOfMonth,    int $hour,    int $minute,    int $second = ?)

    public createFromDate(int $year, int $month, int $dayOfMonth): static
public createFromDateTime(    int $year,    int $month,    int $dayOfMonth,    int $hour,    int $minute,    int $second = null): static
public getGregorianChange(): float
public isLeapYear(int $year): bool
public setGregorianChange(float $timestamp): bool


    /* Наследуемые методы */
    public IntlCalendar::add(int $field, int $value): bool
public IntlCalendar::after(IntlCalendar $other): bool
public IntlCalendar::before(IntlCalendar $other): bool
public IntlCalendar::clear(?int $field = null): true
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
public IntlCalendar::set(int $field, int $value): true
public IntlCalendar::set(    int $year,    int $month,    int $dayOfMonth = NULL,    int $hour = NULL,    int $minute = NULL,    int $second = NULL): true
public IntlCalendar::setDate(int $year, int $month, int $dayOfMonth): void
public IntlCalendar::setDateTime(    int $year,    int $month,    int $dayOfMonth,    int $hour,    int $minute,    int $second = null): void
public IntlCalendar::setFirstDayOfWeek(int $dayOfWeek): true
public IntlCalendar::setLenient(bool $lenient): true
public IntlCalendar::setMinimalDaysInFirstWeek(int $days): true
public IntlCalendar::setRepeatedWallTimeOption(int $option): true
public IntlCalendar::setSkippedWallTimeOption(int $option): true
public IntlCalendar::setTime(float $timestamp): bool
public IntlCalendar::setTimeZone(IntlTimeZone|DateTimeZone|string|null $timezone): bool
public IntlCalendar::toDateTime(): DateTime|false

   }
```

## Зміст

-   [IntlGregorianCalendar::\_\_construct](intlgregoriancalendar.construct.md) \- Конструктор класу григоріанського календаря
-   [IntlGregorianCalendar::createFromDate](intlgregoriancalendar.createfromdate.md)— Створює новий екземпляр Intel GregorianCalendar із дати
-   [IntlGregorianCalendar::createFromDateTime](intlgregoriancalendar.createfromdatetime.md)— Створює новий екземпляр Intel GregorianCalendar із дати та часу
-   [IntlGregorianCalendar::getGregorianChange](intlgregoriancalendar.getgregorianchange.md)— Отримує дату зміни григоріанського календаря
-   [IntlGregorianCalendar::isLeapYear](intlgregoriancalendar.isleapyear.md)— Визначає, чи цей рік є високосним.
-   [IntlGregorianCalendar::setGregorianChange](intlgregoriancalendar.setgregorianchange.md)— Встановлює дату зміни у григоріанському календарі
