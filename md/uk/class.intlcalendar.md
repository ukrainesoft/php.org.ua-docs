---
navigation:
  - messageformatter.setpattern.md: '« MessageFormatter::setPattern'
  - intlcalendar.add.md: 'IntlCalendar::add »'
  - index.md: PHP Manual
  - book.intl.md: intl
title: Клас IntlCalendar
---
# Клас IntlCalendar

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

## Вступ

## Огляд класів

```classsynopsis

     
    

    
     
      class IntlCalendar
     
     {

    /* Константы */
    
     const
     int
      FIELD_ERA = 0;

    const
     int
      FIELD_YEAR = 1;

    const
     int
      FIELD_MONTH = 2;

    const
     int
      FIELD_WEEK_OF_YEAR = 3;

    const
     int
      FIELD_WEEK_OF_MONTH = 4;

    const
     int
      FIELD_DATE = 5;

    const
     int
      FIELD_DAY_OF_YEAR = 6;

    const
     int
      FIELD_DAY_OF_WEEK = 7;

    const
     int
      FIELD_DAY_OF_WEEK_IN_MONTH = 8;

    const
     int
      FIELD_AM_PM = 9;

    const
     int
      FIELD_HOUR = 10;

    const
     int
      FIELD_HOUR_OF_DAY = 11;

    const
     int
      FIELD_MINUTE = 12;

    const
     int
      FIELD_SECOND = 13;

    const
     int
      FIELD_MILLISECOND = 14;

    const
     int
      FIELD_ZONE_OFFSET = 15;

    const
     int
      FIELD_DST_OFFSET = 16;

    const
     int
      FIELD_YEAR_WOY = 17;

    const
     int
      FIELD_DOW_LOCAL = 18;

    const
     int
      FIELD_EXTENDED_YEAR = 19;

    const
     int
      FIELD_JULIAN_DAY = 20;

    const
     int
      FIELD_MILLISECONDS_IN_DAY = 21;

    const
     int
      FIELD_IS_LEAP_MONTH = 22;

    const
     int
      FIELD_FIELD_COUNT  = 23;

    const
     int
      FIELD_DAY_OF_MONTH = 5;

    const
     int
      DOW_SUNDAY = 1;

    const
     int
      DOW_MONDAY = 2;

    const
     int
      DOW_TUESDAY = 3;

    const
     int
      DOW_WEDNESDAY = 4;

    const
     int
      DOW_THURSDAY = 5;

    const
     int
      DOW_FRIDAY = 6;

    const
     int
      DOW_SATURDAY = 7;

    const
     int
      DOW_TYPE_WEEKDAY = 0;

    const
     int
      DOW_TYPE_WEEKEND = 1;

    const
     int
      DOW_TYPE_WEEKEND_OFFSET = 2;

    const
     int
      DOW_TYPE_WEEKEND_CEASE = 3;

    const
     int
      WALLTIME_FIRST = 1;

    const
     int
      WALLTIME_LAST = 0;

    const
     int
      WALLTIME_NEXT_VALID = 2;


    /* Методы */
    
   private __construct()

    public add(int $field, int $value): bool
public after(IntlCalendar $other): bool
public before(IntlCalendar $other): bool
public clear(?int $field = null): bool
public static createInstance(IntlTimeZone|DateTimeZone|string|null $timezone = null, ?string $locale = null): ?IntlCalendar
public equals(IntlCalendar $other): bool
public fieldDifference(float $timestamp, int $field): int|false
public static fromDateTime(DateTime|string $datetime, ?string $locale = null): ?IntlCalendar
public get(int $field): int|false
public getActualMaximum(int $field): int|false
public getActualMinimum(int $field): int|false
public static getAvailableLocales(): array
public getDayOfWeekType(int $dayOfWeek): int|false
public getErrorCode(): int|false
public getErrorMessage(): string|false
public getFirstDayOfWeek(): int|false
public getGreatestMinimum(int $field): int|false
public static getKeywordValuesForLocale(string $keyword, string $locale, bool $onlyCommon): IntlIterator|false
public getLeastMaximum(int $field): int|false
public getLocale(int $type): string|false
public getMaximum(int $field): int|false
public getMinimalDaysInFirstWeek(): int|false
public getMinimum(int $field): int|false
public static getNow(): float
public getRepeatedWallTimeOption(): int
public getSkippedWallTimeOption(): int
public getTime(): float|false
public getTimeZone(): IntlTimeZone|false
public getType(): string
public getWeekendTransition(int $dayOfWeek): int|false
public inDaylightTime(): bool
public isEquivalentTo(IntlCalendar $other): bool
public isLenient(): bool
public isSet(int $field): bool
public isWeekend(?float $timestamp = null): bool
public roll(int $field, int|bool $value): bool
public set(int $field, int $value): bool
public set(    int $year,    int $month,    int $dayOfMonth = NULL,    int $hour = NULL,    int $minute = NULL,    int $second = NULL): bool
public setFirstDayOfWeek(int $dayOfWeek): bool
public setLenient(bool $lenient): bool
public setMinimalDaysInFirstWeek(int $days): bool
public setRepeatedWallTimeOption(int $option): bool
public setSkippedWallTimeOption(int $option): bool
public setTime(float $timestamp): bool
public setTimeZone(IntlTimeZone|DateTimeZone|string|null $timezone): bool
public toDateTime(): DateTime|false

   }
```

## Обумовлені константи

**`IntlCalendar::FIELD_ERA`**

Поле календаря чисельно представляє епоху, наприклад `1` для "від Різдва Христового" та `0` для "до Різдва Христового" у Григоріанському та Юліанському календарях та `235` для періоду Хейсей в Японському календарі. Не всі календарі мають більше за одну епоху.

**`IntlCalendar::FIELD_YEAR`**

Поле календар для року. Не унікально у контексті кількох епох. Якщо календар містить більше однієї ери, то, як правило, мінімальне значення цього поля дорівнює `1`

**`IntlCalendar::FIELD_MONTH`**

Поле календар для місяця. Послідовність місяців починається з нуля, отже Janurary (Січень) (тут використовується для позначення першого місяця року, але за фактом може бути зовсім інше ім'я, наприклад Muharram для Ісламського календаря) буде представлено числом `0`, February (Лютий) числом `1`, …, December (Грудень) числом `11` і, для деяких календарів, 13-й або високосний місяць, значення дорівнюватиме `12`

**`IntlCalendar::FIELD_WEEK_OF_YEAR`**

Поле календар для номера тижня в році. Залежить від того, з [якого дня починається тиждень](intlcalendar.getfirstdayofweek.md) і [мінімальної кількості днів у тижні](intlcalendar.getminimaldaysinfirstweek.md)

**`IntlCalendar::FIELD_WEEK_OF_MONTH`**

Поле календар для номера тижня в місяці. Залежить від того, з [якого дня починається тиждень](intlcalendar.getfirstdayofweek.md) і [мінімальної кількості днів у тижні](intlcalendar.getminimaldaysinfirstweek.md)

**`IntlCalendar::FIELD_DATE`**

Поле календар для номера дня в місяці. Те саме, що й **`IntlCalendar::FIELD_DAY_OF_MONTH`**

**`IntlCalendar::FIELD_DAY_OF_YEAR`**

Поле календар для номера дня в році. Для Грегоріанського календаря знаходиться в діапазоні від **`1`** до **`365`** або **`366`**

**`IntlCalendar::FIELD_DAY_OF_WEEK`**

Поле календаря для номера дня тижня. Починається з `1` (Неділя, дивись [**`IntlCalendar::DOW_SUNDAY`**](class.intlcalendar.md#intlcalendar.constants.dow-sunday) і пов'язані константи) і закінчується 7 (субота).

**`IntlCalendar::FIELD_DAY_OF_WEEK_IN_MONTH`**

Номер дня тижня (Неділя, Понеділок, …) на місяць. Допустимо це значення одно `1`, а значення дня тижня рівне `2` (Понеділок), отже, це перший понеділок місяця. Максимальне значення дорівнює `5`

Також допустимі значення `0` та нижче (негативні). Значення `0` охоплює 7 днів безпосередньо перед початком місяця (перший відповідний день у місяці має значення `1`). Негативні значення відраховуються від кінця місяця. Так, значення `-1` вказує на останній відповідний день місяця, `-2` на другий з кінця і т.д.

На відміну від [**`IntlCalendar::FIELD_WEEK_OF_MONTH`**](class.intlcalendar.md#intlcalendar.constants.field-week-of-month) і [**`IntlCalendar::FIELD_WEEK_OF_YEAR`**](class.intlcalendar.md#intlcalendar.constants.field-week-of-year), це значення не залежить від [IntlCalendar::getFirstDayOfWeek()](intlcalendar.getfirstdayofweek.md) і [IntlCalendar::getMinimalDaysInFirstWeek()](intlcalendar.getminimaldaysinfirstweek.md). Перше середовище - це перше середовище, навіть якщо тиждень розпочався попереднього місяця.

**`IntlCalendar::FIELD_AM_PM`**

Поле календаря визначальний час до/після полудня. Відповідно `0` - до полудня, (`1`) - після. Північ вважається як "до полудня", опівдні як "після полудня".

**`IntlCalendar::FIELD_HOUR`**

Поле календаря для годинника, без вказівки до або після полудня. Допустимі значення в інтервалі від `0` до `11`

**`IntlCalendar::FIELD_HOUR_OF_DAY`**

Поле календаря для повного (24-годинного формату) годинника. Допустимі значення від `0` до `23`

**`IntlCalendar::FIELD_MINUTE`**

Поле календар для хвилин.

**`IntlCalendar::FIELD_SECOND`**

Поле календар для секунд.

**`IntlCalendar::FIELD_MILLISECOND`**

Поле календар для мілісекунд.

**`IntlCalendar::FIELD_ZONE_OFFSET`**

Поле календаря для «сирого» усунення часового поясу, в мілісекундах. "Сире" усунення не враховує переходи на літній/зимовий час.

**`IntlCalendar::FIELD_DST_OFFSET`**

Поле календаря для зміщення часового поясу в мілісекундах залежно від літнього/зимового часу, якщо застосовується до цього часового поясу.

**`IntlCalendar::FIELD_YEAR_WOY`**

Поле календаря являє собою рік для [недели года](class.intlcalendar.md#intlcalendar.constants.field-week-of-year)

**`IntlCalendar::FIELD_DOW_LOCAL`**

Поле календар для локалізованого дня тижня. Приймає значення в діапазоні від `1` до `7`. . `1` використовується для дня тижня відповідного значення повертається функцією [IntlCalendar::getFirstDayOfWeek()](intlcalendar.getfirstdayofweek.md)

**`IntlCalendar::FIELD_EXTENDED_YEAR`**

Поле календаря для представлення номера року у контексті забезпечення безперервності між епохами. Наприклад, для Грегоріанського календаря, це значення для епохи "після Різдва Христового" буде відповідати **`IntlCalendar::FIELD_YEAR`**, а для епохи "до Різдва Христового", рік `y` буде представлено як `-y + 1`

**`IntlCalendar::FIELD_JULIAN_DAY`**

Поле календар для модифікованих номерів днів Юліанського календаря. На відміну від стандартного Юліанського календаря, у ньому перехід відбувається опівночі за локальним часом, а не опівдні за UTC. Він однозначно ідентифікує дату.

**`IntlCalendar::FIELD_MILLISECONDS_IN_DAY`**

Поле календаря, що охоплює **`IntlCalendar::FIELD_HOUR_OF_DAY`** **`IntlCalendar::FIELD_MINUTE`** **`IntlCalendar::FIELD_SECOND`** і **`IntlCalendar::FIELD_MILLISECOND`**. Знаходиться в діапазоні від `0` до `24 * 3600 * 1000 - 1`. Це не кількість мілісекунд, що минула з півночі, тому що в моменти переходу на літній/зимовий час матиме розриви.

**`IntlCalendar::FIELD_IS_LEAP_MONTH`**

Поле календаря, що приймає значення `1` для високосного місяця та `0` для звичайного.

**`IntlCalendar::FIELD_FIELD_COUNT`**

Загальна кількість полів.

**`IntlCalendar::FIELD_DAY_OF_MONTH`**

Псевдонім для [**`IntlCalendar::FIELD_DATE`**](class.intlcalendar.md#intlcalendar.constants.field-date)

**`IntlCalendar::DOW_SUNDAY`**

Неділя.

**`IntlCalendar::DOW_MONDAY`**

Понеділок.

**`IntlCalendar::DOW_TUESDAY`**

Вівторок.

**`IntlCalendar::DOW_WEDNESDAY`**

Середа.

**`IntlCalendar::DOW_THURSDAY`**

Четвер.

**`IntlCalendar::DOW_FRIDAY`**

П'ятниця.

**`IntlCalendar::DOW_SATURDAY`**

Субота.

**`IntlCalendar::DOW_TYPE_WEEKDAY`**

Висновок [IntlCalendar::getDayOfWeekType()](intlcalendar.getdayofweektype.md) означає, що день буде.

**`IntlCalendar::DOW_TYPE_WEEKEND`**

Висновок [IntlCalendar::getDayOfWeekType()](intlcalendar.getdayofweektype.md) означає, що вихідний день.

**`IntlCalendar::DOW_TYPE_WEEKEND_OFFSET`**

Висновок [IntlCalendar::getDayOfWeekType()](intlcalendar.getdayofweektype.md) означає, що вихідні розпочинаються у цей день.

**`IntlCalendar::DOW_TYPE_WEEKEND_CEASE`**

Висновок [IntlCalendar::getDayOfWeekType()](intlcalendar.getdayofweektype.md) означає, що вихідні закінчуються у цей день.

**`IntlCalendar::WALLTIME_FIRST`**

Висновок [IntlCalendar::getSkippedWallTimeOption()](intlcalendar.getskippedwalltimeoption.md) означає, що час у пропущеному діапазоні має посилатися на час менший на одну годину і висновок [IntlCalendar::getRepeatedWallTimeOption()](intlcalendar.getrepeatedwalltimeoption.md) означає, що час у діапазоні, що повторюється, повинен ставитися до моменту першої появи такого часу.

**`IntlCalendar::WALLTIME_LAST`**

Висновок [IntlCalendar::getSkippedWallTimeOption()](intlcalendar.getskippedwalltimeoption.md) означає, що час у пропущеному діапазоні має посилатися на час більший на одну годину і висновок [IntlCalendar::getRepeatedWallTimeOption()](intlcalendar.getrepeatedwalltimeoption.md) означає, що час у діапазоні, що повторюється, повинен ставитися до моменту другої появи такого часу.

**`IntlCalendar::WALLTIME_NEXT_VALID`**

Висновок [IntlCalendar::getSkippedWallTimeOption()](intlcalendar.getskippedwalltimeoption.md) означає, що час у пропущеному діапазоні відноситься до моменту, коли стався перехід на зимовий/літній час.

## Зміст

-   [IntlCalendar::add](intlcalendar.add.md) - Додає кількість (зі знаком) часу в полі
-   [IntlCalendar::after](intlcalendar.after.md) - Визначає, час цього об'єкта пізніше часу переданого об'єкта
-   [IntlCalendar::before](intlcalendar.before.md) — Визначає, час цього об'єкта раніше переданого об'єкта
-   [IntlCalendar::clear](intlcalendar.clear.md) — Очищає поле чи всі поля
-   [IntlCalendar::construct](intlcalendar.construct.md) — Закритий конструктор для заборони створення екземплярів
-   [IntlCalendar::createInstance](intlcalendar.createinstance.md) — Створює новий об'єкт IntlCalendar
-   [IntlCalendar::equals](intlcalendar.equals.md) — Порівнює час двох об'єктів IntlCalendar щодо рівності
-   [IntlCalendar::fieldDifference](intlcalendar.fielddifference.md) — Обчислює різницю між заданим часом та часом об'єкта
-   [IntlCalendar::fromDateTime](intlcalendar.fromdatetime.md) — Створює IntlCalendar з об'єкта чи рядка DateTime
-   [IntlCalendar::get](intlcalendar.get.md) — Отримує значення поля
-   [IntlCalendar::getActualMaximum](intlcalendar.getactualmaximum.md) — Максимальне значення для поля з урахуванням поточного часу об'єкта
-   [IntlCalendar::getActualMinimum](intlcalendar.getactualminimum.md) — Мінімальне значення для поля з урахуванням поточного часу об'єкта
-   [IntlCalendar::getAvailableLocales](intlcalendar.getavailablelocales.md) — Отримує масив мовних стандартів, для яких є дані
-   [IntlCalendar::getDayOfWeekType](intlcalendar.getdayofweektype.md) — Повідомляє, чи день буде буднім, вихідним чи днем ​​з переходом між ними
-   [IntlCalendar::getErrorCode](intlcalendar.geterrorcode.md) — Отримує останній код помилки об'єкта
-   [IntlCalendar::getErrorMessage](intlcalendar.geterrormessage.md) — Отримує останнє повідомлення про помилку об'єкта
-   [IntlCalendar::getFirstDayOfWeek](intlcalendar.getfirstdayofweek.md) — отримує перший день тижня для мовного стандарту календаря
-   [IntlCalendar::getGreatestMinimum](intlcalendar.getgreatestminimum.md) — Отримує найбільше локальне мінімальне значення поля
-   [IntlCalendar::getKeywordValuesForLocale](intlcalendar.getkeywordvaluesforlocale.md) — Набір значень ключових слів мовного стандарту
-   [IntlCalendar::getLeastMaximum](intlcalendar.getleastmaximum.md) — Отримує найменший локальний максимум для поля
-   [IntlCalendar::getLocale](intlcalendar.getlocale.md) — Отримує мовний стандарт, пов'язаний із об'єктом
-   [IntlCalendar::getMaximum](intlcalendar.getmaximum.md) — Отримує глобальне максимальне значення поля
-   [IntlCalendar::getMinimalDaysInFirstWeek](intlcalendar.getminimaldaysinfirstweek.md) — Отримує мінімальну кількість днів, яка може бути у першому тижні на рік чи місяць
-   [IntlCalendar::getMinimum](intlcalendar.getminimum.md) — Отримує глобальне мінімальне значення поля
-   [IntlCalendar::getNow](intlcalendar.getnow.md) — Отримує число, що становить поточний час
-   [IntlCalendar::getRepeatedWallTimeOption](intlcalendar.getrepeatedwalltimeoption.md) — Отримує поведінку для обробки часу процесора, що повторюється.
-   [IntlCalendar::getSkippedWallTimeOption](intlcalendar.getskippedwalltimeoption.md) — Отримує поведінку для обробки пропущеного часу процесора
-   [IntlCalendar::getTime](intlcalendar.gettime.md) — Отримує час, представлений на даний момент об'єктом
-   [IntlCalendar::getTimeZone](intlcalendar.gettimezone.md) — Отримує часовий пояс об'єкту
-   [IntlCalendar::getType](intlcalendar.gettype.md) — Отримує тип календаря
-   [IntlCalendar::getWeekendTransition](intlcalendar.getweekendtransition.md) — Отримує час, коли вихідні починаються або закінчуються.
-   [IntlCalendar::inDaylightTime](intlcalendar.indaylighttime.md) — Визначає, чи час об'єкта переходить на літній час.
-   [IntlCalendar::isEquivalentTo](intlcalendar.isequivalentto.md) — Визначає, чи дорівнює інший календар, але для іншого часу
-   [IntlCalendar::isLenient](intlcalendar.islenient.md) — Визначає, чи інтерпретація дати/часу є м'якою.
-   [IntlCalendar::isSet](intlcalendar.isset.md) — Визначає, чи встановлено поле
-   [IntlCalendar::isWeekend](intlcalendar.isweekend.md) — Визначає, чи доводиться певна дата/час на вихідні
-   [IntlCalendar::roll](intlcalendar.roll.md) — Додає значення в поле без перенесення до найважливіших полів
-   [IntlCalendar::set](intlcalendar.set.md) — Встановлює поле часу або одразу кілька спільних полів
-   [IntlCalendar::setFirstDayOfWeek](intlcalendar.setfirstdayofweek.md) — Встановлює день, який є початком тижня
-   [IntlCalendar::setLenient](intlcalendar.setlenient.md) — Встановлює, чи інтерпретація дати/часу повинна бути м'якою.
-   [IntlCalendar::setMinimalDaysInFirstWeek](intlcalendar.setminimaldaysinfirstweek.md) — Встановлює мінімальну кількість днів, яка може бути у першому тижні на рік чи місяць
-   [IntlCalendar::setRepeatedWallTimeOption](intlcalendar.setrepeatedwalltimeoption.md) — Встановлює поведінку для обробки часу процесора, що повторюється, при негативних переходах зміщення часового поясу.
-   [IntlCalendar::setSkippedWallTimeOption](intlcalendar.setskippedwalltimeoption.md) — Встановлює поведінку для обробки пропущеного часу процесора при позитивних переходах усунення часового поясу
-   [IntlCalendar::setTime](intlcalendar.settime.md) — Встановлює календарний час у мілісекундах від початку епохи Unix
-   [IntlCalendar::setTimeZone](intlcalendar.settimezone.md) — Встановлює часовий пояс, який використовується календарем.
-   [IntlCalendar::toDateTime](intlcalendar.todatetime.md) — Перетворює IntlCalendar на об'єкт DateTime
