---
navigation:
  - class.intldateformatter.md: « IntlDateFormatter
  - intldateformatter.format.md: 'IntlDateFormatter::format »'
  - index.md: PHP Manual
  - class.intldateformatter.md: IntlDateFormatter
title: 'IntlDateFormatter::create'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlDateFormatter::create

# datefmt\_create

# IntlDateFormatter::\_\_construct

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

IntlDateFormatter::create -- datefmt\_create -- IntlDateFormatter::\_\_construct — Створює засіб форматування дати

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static IntlDateFormatter::create(    ?string $locale,    int $dateType = IntlDateFormatter::FULL,    int $timeType = IntlDateFormatter::FULL,    IntlTimeZone|DateTimeZone|string|null $timezone = null,    IntlCalendar|int|null $calendar = null,    ?string $pattern = null): ?IntlDateFormatter
```

Об'єктно-орієнтований стиль (конструктор)

public **IntlDateFormatter::\_\_construct**  
?string`$locale`,  
int`$dateType`\= IntlDateFormatter::FULL,  
int`$timeType`\= IntlDateFormatter::FULL,  
[IntlTimeZone](class.intltimezone.md) [DateTimeZone](class.datetimezone.md)|string|null`$timezone` **`null`**,  
[IntlCalendar](class.intlcalendar.md)|int|null`$calendar` **`null`**,  
?string`$pattern` **`null`**  
) .

Процедурний стиль

```methodsynopsis
datefmt_create(    ?string $locale,    int $dateType,    int $timeType,    IntlTimeZone|DateTimeZone|string|null $timezone = null,    IntlCalendar|int|null $calendar = null,    string $pattern = ""): ?IntlDateFormatter
```

Створює засіб форматування дати.

### Список параметрів

`locale`

Мовний стандарт, який буде використаний для форматування або синтаксичного аналізу, або **`null`** для вибору значення, заданого в ini-налаштуванні [intl.default\_locale](intl.configuration.md#ini.intl.default-locale)

`dateType`

Формат дати, визначений однією [з констант IntlDateFormatter](class.intldateformatter.md#intl.intldateformatter-constants)Значение по умолчанию\*\*`IntlDateFormatter::FULL`\*\*

`timeType`

Формат часу, який був визначений однією [з констант IntlDateFormatter](class.intldateformatter.md#intl.intldateformatter-constants)Значение по умолчанию\*\*`IntlDateFormatter::FULL`\*\*

`timezone`

Ідентифікатор часового поясу. За замовчуванням (і той, який використовується, якщо вказано **`null`**) - це той, який повертається [date\_default\_timezone\_get()](function.date-default-timezone-get.md) або, якщо застосовно, об'єкт [IntlCalendar](class.intlcalendar.md), вказаний у параметрі `calendar`. Цей ідентифікатор має бути коректним ідентифікатором у базі даних ICU або ідентифікатором, який представляє явне зміщення, наприклад, `GMT-05:30`

Також може бути об'єкт [IntlTimeZone](class.intltimezone.md) або [DateTimeZone](class.datetimezone.md)

`calendar`

Календар для форматування чи аналізу. Значення за замовчуванням - **`null`**, що відповідає **`IntlDateFormatter::GREGORIAN`**. Можливо одна з [констант IntlDateFormatter](class.intldateformatter.md#intl.intldateformatter-constants.calendartypes) або об'єкт [IntlCalendar](class.intlcalendar.md). Будь-який переданий об'єкт [IntlCalendar](class.intlcalendar.md) буде клоновано; він не буде змінено [IntlDateFormatter](class.intldateformatter.md). Це визначить тип календаря, що використовується (григоріанський, ісламський, перський і т.д.) і, якщо в параметрі `timezone`указано значение\*\*`null`\*\*, також визначить часовий пояс, що використовується.

`pattern`

Необов'язковий шаблон для використання під час форматування або аналізу. Можливі шаблони документовані за адресою [» https://unicode-org.github.io/icu/userguide/format\_parse/datetime/](https://unicode-org.github.io/icu/userguide/format_parse/datetime/)

### Значення, що повертаються

Створений об'єкт [IntlDateFormatter](class.intldateformatter.md)или\*\*`null`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 |  |
| Тепер параметри `dateType`и`timeType` необов'язкові. |  |

### Приклади

**Приклад #1 Приклад використання** datefmt\_create()\*\*\*\*

```php
<?php
$fmt = datefmt_create( "en_US" ,IntlDateFormatter::FULL, IntlDateFormatter::FULL,
    'America/Los_Angeles', IntlDateFormatter::GREGORIAN  );
echo "First Formatted output is ".datefmt_format( $fmt , 0);
$fmt = datefmt_create( "de-DE" ,IntlDateFormatter::FULL, IntlDateFormatter::FULL,
    'America/Los_Angeles',IntlDateFormatter::GREGORIAN  );
echo "Second Formatted output is ".datefmt_format( $fmt , 0);

$fmt = datefmt_create( "en_US" ,IntlDateFormatter::FULL, IntlDateFormatter::FULL,
     'America/Los_Angeles',IntlDateFormatter::GREGORIAN  ,"MM/dd/yyyy");
echo "First Formatted output with pattern is ".datefmt_format( $fmt , 0);
$fmt = datefmt_create( "de-DE" ,IntlDateFormatter::FULL, IntlDateFormatter::FULL,
     'America/Los_Angeles',IntlDateFormatter::GREGORIAN  ,"MM/dd/yyyy");
echo "Second Formatted output with pattern is ".datefmt_format( $fmt , 0);
?>
```

**Приклад #2 OO example**

```php
<?php
$fmt = new IntlDateFormatter( "en_US" ,IntlDateFormatter::FULL, IntlDateFormatter::FULL,
    'America/Los_Angeles',IntlDateFormatter::GREGORIAN  );
echo "Первый форматированный вывод: ".$fmt->format(0);
$fmt = new IntlDateFormatter( "de-DE" ,IntlDateFormatter::FULL, IntlDateFormatter::FULL,
    'America/Los_Angeles',IntlDateFormatter::GREGORIAN  );
echo "Второй форматированный вывод: ".$fmt->format(0);

$fmt = new IntlDateFormatter( "en_US" ,IntlDateFormatter::FULL, IntlDateFormatter::FULL,
     'America/Los_Angeles',IntlDateFormatter::GREGORIAN  ,"MM/dd/yyyy");
echo "Первый форматированный вывод с шаблоном: ".$fmt->format(0);
$fmt = new IntlDateFormatter( "de-DE" ,IntlDateFormatter::FULL, IntlDateFormatter::FULL,
      'America/Los_Angeles',IntlDateFormatter::GREGORIAN , "MM/dd/yyyy");
echo "Второй форматированный вывод с шаблоном: ".$fmt->format(0);
?>
```

**Приклад #3 Приклад обробки неправильного значення мовного стандарту**

```php
<?php
try {
    $fmt = new IntlDateFormatter(
        'invalid_locale',
        IntlDateFormatter::FULL,
        IntlDateFormatter::FULL,
        'dunno',
        IntlDateFormatter::GREGORIAN,
    );
} catch (\Error $e) {
    // ...
}
?>
```

Результат виконання наведеного прикладу:

```
Первый форматированный вывод: Wednesday, December 31, 1969 4:00:00 PM PT
Второй форматированный вывод: Mittwoch, 31. Dezember 1969 16:00 Uhr GMT-08:00
Первый форматированный вывод с шаблоном: 12/31/1969
Второй форматированный вывод с шаблоном: 12/31/1969
```

### Дивіться також

-   [datefmt\_format()](intldateformatter.format.md) \- Форматує значення дати/часу у вигляді рядка
-   [datefmt\_parse()](intldateformatter.parse.md) \- Перетворює рядок на значення позначки часу
-   [datefmt\_get\_error\_code()](intldateformatter.geterrorcode.md) \- Отримує код помилки останньої операції
-   [datefmt\_get\_error\_message()](intldateformatter.geterrormessage.md) \- Отримує текст помилки останньої операції
