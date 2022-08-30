Створює засіб форматування дати

-   [« IntlDateFormatter](class.intldateformatter.md)
    
-   [IntlDateFormatter::format »](intldateformatter.format.md)
    
-   [PHP Manual](index.md)
    
-   [IntlDateFormatter](class.intldateformatter.md)
    
-   Створює засіб форматування дати
    

# IntlDateFormatter::create

# datefmtcreate

# IntlDateFormatter::construct

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

IntlDateFormatter::create -- datefmtcreate -- IntlDateFormatter::construct — Створює засіб форматування дати

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static IntlDateFormatter::create(    ?string $locale,    int $dateType = IntlDateFormatter::FULL,    int $timeType = IntlDateFormatter::FULL,    IntlTimeZone|DateTimeZone|string|null $timezone = null,    IntlCalendar|int|null $calendar = null,    ?string $pattern = null): ?IntlDateFormatter
```

Об'єктно-орієнтований стиль (конструктор)

public **IntlDateFormatter::construct**  
?string `$locale`  
int `$dateType` = IntlDateFormatter::FULL,  
int `$timeType` = IntlDateFormatter::FULL,  
[IntlTimeZone](class.intltimezone.md)[DateTimeZone](class.datetimezone.md)|string|null `$timezone` **`null`**  
[IntlCalendar](class.intlcalendar.md)| int | null `$calendar` **`null`**  
?string `$pattern` **`null`**

Процедурний стиль

```methodsynopsis
datefmt_create(    ?string $locale,    int $dateType,    int $timeType,    IntlTimeZone|DateTimeZone|string|null $timezone = null,    IntlCalendar|int|null $calendar = null,    string $pattern = ""): ?IntlDateFormatter
```

Створює засіб форматування дати.

### Список параметрів

`locale`

Мовний стандарт, який використовується при форматуванні або синтаксичному аналізі або **`null`** для використання значення, вказаного в ini-налаштуванні [intl.defaultlocale](intl.configuration.html#ini.intl.default-locale)

`dateType`

Тип дати (**`none`** **`short`** **`medium`** **`long`** **`full`**). Одна з [констант IntlDateFormatter](class.intldateformatter.html#intl.intldateformatter-constants)

`timeType`

Тип часу (**`none`** **`short`** **`medium`** **`long`** **`full`**). Одна з [констант IntlDateFormatter](class.intldateformatter.html#intl.intldateformatter-constants)

`timezone`

Ідентифікатор часового поясу. За замовчуванням (і той, який використовується, якщо вказано **`null`**) - це той, який повертається [datedefaulttimezoneget()](function.date-default-timezone-get.html) або, якщо застосовно, об'єкт [IntlCalendar](class.intlcalendar.md), вказаний у параметрі `calendar`. Цей ідентифікатор повинен бути коректним ідентифікатором у базі даних ICU або ідентифікатором, який представляє явне зміщення, наприклад, `GMT-05:30`

Також може бути об'єкт [IntlTimeZone](class.intltimezone.md) або [DateTimeZone](class.datetimezone.md)

`calendar`

Календар для форматування чи аналізу. Значення за замовчуванням - **`null`**, що відповідає **`IntlDateFormatter::GREGORIAN`**. Можливо одна з [констант IntlDateFormatter](class.intldateformatter.html#intl.intldateformatter-constants.calendartypes) або об'єкт [IntlCalendar](class.intlcalendar.md). Будь-який переданий об'єкт [IntlCalendar](class.intlcalendar.md) буде клоновано; він не буде змінений [IntlDateFormatter](class.intldateformatter.md). Це визначить тип календаря, що використовується (григоріанський, ісламський, перський і т.д.) і, якщо в параметрі `timezone` вказано значення **`null`**, також визначить часовий пояс, що використовується.

`pattern`

Необов'язковий шаблон для використання під час форматування або аналізу. Можливі шаблони документовані за адресою [» https://unicode-org.github.io/icu/userguide/formatparse/datetime/](https://unicode-org.github.io/icu/userguide/format_parse/datetime/)

### Значення, що повертаються

Створений об'єкт [IntlDateFormatter](class.intldateformatter.md) або **`null`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| 5.5.0/PECL 3.0.0 |  |
| Об'єкт [IntlCalendar](class.intlcalendar.md) допускається у параметрі `calendar` |  |

Об'єкти [IntlTimeZone](class.intltimezone.md) і [DateTimeZone](class.datetimezone.md) допускаються у параметрі `timezone`

Неприпустимі ідентифікатори часового поясу (включаючи порожні рядки) більше не допускаються у параметрі `timezone`

Якщо у параметрі `timezone` вказано значення **`null`**, ідентифікатор часового поясу, заданий [datedefaulttimezoneget()](function.date-default-timezone-get.html), використовуватиметься замість значення ICU за замовчуванням.

### Приклади

**Приклад #1 Приклад використання **datefmtcreate()****

```php
<?php
$fmt = datefmt_create( "en_US" ,IntlDateFormatter::FULL, IntlDateFormatter::FULL,
    'America/Los_Angeles', IntlDateFormatter::GREGORIAN  );
echo "First Formatted output is ".datefmt_format( $fmt , 0);
$fmt = datefmt_create( "de-DE" ,IntlDateFormatter::FULL, IntlDateFormatter::FULL,
    'America/Los_Angeles',IntlDateFormatter::GREGORIAN  );
echo "Second Formatted output is ".datefmt_format( $fmt , 0);

$fmt = datefmt_create( "en_US" ,IntlDateFormatter::FULL, IntlDateFormatter::FULL,
     'America/Los_Angeles',IntlDateFormatter::GREGORIAN  ,"MM/dd/yyyy");
echo "First Formatted output with pattern is ".datefmt_format( $fmt , 0);
$fmt = datefmt_create( "de-DE" ,IntlDateFormatter::FULL, IntlDateFormatter::FULL,
     'America/Los_Angeles',IntlDateFormatter::GREGORIAN  ,"MM/dd/yyyy");
echo "Second Formatted output with pattern is ".datefmt_format( $fmt , 0);
?>
```

**Приклад #2 OO example**

```php
<?php
$fmt = new IntlDateFormatter( "en_US" ,IntlDateFormatter::FULL, IntlDateFormatter::FULL,
    'America/Los_Angeles',IntlDateFormatter::GREGORIAN  );
echo "Первый форматированный вывод: ".$fmt->format(0);
$fmt = new IntlDateFormatter( "de-DE" ,IntlDateFormatter::FULL, IntlDateFormatter::FULL,
    'America/Los_Angeles',IntlDateFormatter::GREGORIAN  );
echo "Второй форматированный вывод: ".$fmt->format(0);

$fmt = new IntlDateFormatter( "en_US" ,IntlDateFormatter::FULL, IntlDateFormatter::FULL,
     'America/Los_Angeles',IntlDateFormatter::GREGORIAN  ,"MM/dd/yyyy");
echo "Первый форматированный вывод с шаблоном: ".$fmt->format(0);
$fmt = new IntlDateFormatter( "de-DE" ,IntlDateFormatter::FULL, IntlDateFormatter::FULL,
      'America/Los_Angeles',IntlDateFormatter::GREGORIAN , "MM/dd/yyyy");
echo "Второй форматированный вывод с шаблоном: ".$fmt->format(0);
?>
```

Результат виконання цього прикладу:

```
Первый форматированный вывод: Wednesday, December 31, 1969 4:00:00 PM PT
Второй форматированный вывод: Mittwoch, 31. Dezember 1969 16:00 Uhr GMT-08:00
Первый форматированный вывод с шаблоном: 12/31/1969
Второй форматированный вывод с шаблоном: 12/31/1969
```

### Дивіться також

-   [datefmtformat()](intldateformatter.format.md) - Форматує значення дати/часу у вигляді рядка
-   [datefmtparse()](intldateformatter.parse.md) - Перетворює рядок на значення позначки часу
-   [datefmtgeterrorcode()](intldateformatter.geterrorcode.md) - Отримує код помилки останньої операції
-   [datefmtgeterrormessage()](intldateformatter.geterrormessage.md) - Отримує текст помилки останньої операції