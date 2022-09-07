---
navigation:
  - intltimezone.usedaylighttime.md: '« IntlTimeZone::useDaylightTime'
  - intldateformatter.create.md: 'IntlDateFormatter::create »'
  - index.md: PHP Manual
  - book.intl.md: intl
title: Клас IntlDateFormatter
---
# Клас IntlDateFormatter

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

## Вступ

Це клас, який дозволяє форматувати/розбирати дати відповідно до налаштувань локалі, використовуючи рядкові та/або бібліотечні шаблони.

Клас надає функціональність форматування дат ICU. Він дозволяє користувачам відображати дати у форматі, прийнятому в їхній локалі. Або розбирати значення дат, використовуючи рядкові та/або бібліотечні шаблони.

## Синопсис класу

```classsynopsis

     
    

    
     
      class IntlDateFormatter
     
     {

    /* Методы */
    
   public __construct(    ?string $locale,    int $dateType = IntlDateFormatter::FULL,    int $timeType = IntlDateFormatter::FULL,    IntlTimeZone|DateTimeZone|string|null $timezone = null,    IntlCalendar|int|null $calendar = null,    ?string $pattern = null)

    public static create(    ?string $locale,    int $dateType = IntlDateFormatter::FULL,    int $timeType = IntlDateFormatter::FULL,    IntlTimeZone|DateTimeZone|string|null $timezone = null,    IntlCalendar|int|null $calendar = null,    ?string $pattern = null): ?IntlDateFormatter
public format(IntlCalendar|DateTimeInterface|array|string|int|float $datetime): string|false
public static formatObject(IntlCalendar|DateTimeInterface $datetime, array|int|string|null $format = null, ?string $locale = null): string|false
public getCalendar(): int|false
public getDateType(): int|false
public getErrorCode(): int
public getErrorMessage(): string
public getLocale(int $type = ULOC_ACTUAL_LOCALE): string|false
public getPattern(): string|false
public getTimeType(): int|false
public getTimeZoneId(): string|false
public getCalendarObject(): IntlCalendar|false|null
public getTimeZone(): IntlTimeZone|false
public isLenient(): bool
public localtime(string $string, int &$offset = null): array|false
public parse(string $string, int &$offset = null): int|float|false
public setCalendar(IntlCalendar|int|null $calendar): bool
public setLenient(bool $lenient): void
public setPattern(string $pattern): bool
public setTimeZone(IntlTimeZone|DateTimeZone|string|null $timezone): ?bool

   }
```

## Дивіться також

-   [» Форматирование дат ICU](http://www.icu-project.org/apiref/icu4c/udat_8h.md#details)
    
-   [» Формати дат ICU](https://unicode-org.github.io/icu/userguide/format_parse/datetime/#datetime-format-syntax)
    

## Обумовлені константи

Ці константи використовуються для завдання формату в конструкторах DateType та TimeType.

**`IntlDateFormatter::NONE`** (int)

Не вмикати цей елемент

**`IntlDateFormatter::FULL`** (int)

Повний формат (Tuesday, April 12, 1952 AD or 3:30:42pm PST)

**`IntlDateFormatter::LONG`** (int)

Довгий формат (January 12, 1952 or 3:30:32pm)

**`IntlDateFormatter::MEDIUM`** (int)

Середній формат (Jan 12, 1952)

**`IntlDateFormatter::SHORT`** (int)

Найбільш скорочений формат, тільки найнеобхідніші дані (12/13/52 або 3:30pm)

**`IntlDateFormatter::RELATIVE_FULL`** (int)

Те саме, що і **`IntlDateFormatter::FULL`**, але "вчора", "сьогодні" та "завтра" виводяться як `yesterday` `today` і `tomorrow`. Доступно з PHP 8.0.0 тільки для `dateType`

**`IntlDateFormatter::RELATIVE_LONG`** (int)

Те саме, що і **`IntlDateFormatter::LONG`**, але "вчора", "сьогодні" та "завтра" виводяться як `yesterday` `today` і `tomorrow`. Доступно з PHP 8.0.0 тільки для `dateType`

**`IntlDateFormatter::RELATIVE_MEDIUM`** (int)

Те саме, що і **`IntlDateFormatter::MEDIUM`**, але "вчора", "сьогодні" та "завтра" виводяться як `yesterday` `today` і `tomorrow`. Доступно з PHP 8.0.0 тільки для `dateType`

**`IntlDateFormatter::RELATIVE_SHORT`** (int)

Те саме, що і **`IntlDateFormatter::SHORT`**, але "вчора", "сьогодні" та "завтра" виводяться як `yesterday` `today` і `tomorrow`. Доступно з PHP 8.0.0 тільки для `dateType`

Наступні константи використовуються для завдання типу календаря. Ці календарі зав'язані прямо на Григоріанський календар. Не Григоріанський календар має бути заданий у локалі. Наприклад, locale="hi@calendar=BUDDHIST".

**`IntlDateFormatter::TRADITIONAL`** (int)

Чи не Григоріанський календар

**`IntlDateFormatter::GREGORIAN`** (int)

Григоріанський календар

## Зміст

-   [IntlDateFormatter::create](intldateformatter.create.md) — Створює засіб форматування дати
-   [IntlDateFormatter::format](intldateformatter.format.md) — Форматує значення дати/часу у вигляді рядка
-   [IntlDateFormatter::formatObject](intldateformatter.formatobject.md) - Форматує об'єкт
-   [IntlDateFormatter::getCalendar](intldateformatter.getcalendar.md) — Отримує тип календаря, який використовується IntlDateFormatter
-   [IntlDateFormatter::getDateType](intldateformatter.getdatetype.md) — Отримує тип дати, який використовується IntlDateFormatter
-   [IntlDateFormatter::getErrorCode](intldateformatter.geterrorcode.md) — Отримує код помилки останньої операції
-   [IntlDateFormatter::getErrorMessage](intldateformatter.geterrormessage.md) — Отримує текст помилки останньої операції
-   [IntlDateFormatter::getLocale](intldateformatter.getlocale.md) — Отримує мовний стандарт, який використовується засобом форматування
-   [IntlDateFormatter::getPattern](intldateformatter.getpattern.md) — Отримує шаблон, який використовується IntlDateFormatter
-   [IntlDateFormatter::getTimeType](intldateformatter.gettimetype.md) — Отримує тип часу, який використовується IntlDateFormatter
-   [IntlDateFormatter::getTimeZoneId](intldateformatter.gettimezoneid.md) — Отримує ідентифікатор часового поясу, який використовується IntlDateFormatter
-   [IntlDateFormatter::getCalendarObject](intldateformatter.getcalendarobject.md) — Отримує копію об'єкта календаря засобу форматування
-   [IntlDateFormatter::getTimeZone](intldateformatter.gettimezone.md) — Отримує часовий пояс засобу форматування
-   [IntlDateFormatter::isLenient](intldateformatter.islenient.md) — Отримує поблажливість, яка використовується для IntlDateFormatter
-   [IntlDateFormatter::localtime](intldateformatter.localtime.md) — Перетворює рядок на значення часу на основі поля
-   [IntlDateFormatter::parse](intldateformatter.parse.md) — Перетворює рядок на значення позначки часу
-   [IntlDateFormatter::setCalendar](intldateformatter.setcalendar.md) — Встановлює тип календаря за допомогою форматування.
-   [IntlDateFormatter::setLenient](intldateformatter.setlenient.md) - Встановлює м'який режим аналізатора
-   [IntlDateFormatter::setPattern](intldateformatter.setpattern.md) — Встановлює шаблон, який використовується IntlDateFormatter
-   [IntlDateFormatter::setTimeZone](intldateformatter.settimezone.md) — Встановлює часовий пояс засобу форматування
