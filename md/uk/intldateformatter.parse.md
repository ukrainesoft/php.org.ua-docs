---
navigation:
  - intldateformatter.localtime.md: '« IntlDateFormatter::localtime'
  - intldateformatter.setcalendar.md: 'IntlDateFormatter::setCalendar »'
  - index.md: PHP Manual
  - class.intldateformatter.md: IntlDateFormatter
title: 'IntlDateFormatter::parse'
---
# IntlDateFormatter::parse

# datefmtparse

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

IntlDateFormatter::parse -- datefmtparse — Перетворює рядок на значення позначки часу

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlDateFormatter::parse(string $string, int &$offset = null): int|float|false
```

Процедурний стиль

```methodsynopsis
datefmt_parse(IntlDateFormatter $formatter, string $string, int &$offset = null): int|float|false
```

Перетворює `string` в інкрементне значення часу, починаючи з `offset` і використовуючи якомога більшу частину вхідного значення.

### Список параметрів

`formatter`

Ресурс засобу форматування.

`string`

Рядок для перетворення під час.

`offset`

Позиція, з якої слід розпочати синтаксичний аналіз у `string` (починаючи з нуля). Якщо до використання `string` помилки не виникає, `offset` міститиме -1, в іншому випадку він міститиме позицію, в якій закінчився синтаксичний аналіз (і відбулася помилка). Ця змінна міститиме кінцеву позицію, якщо при синтаксичному аналізі виникла помилка. Якщо `offset` > `strlen($string)`, аналіз негайно завершується помилкою.

### Значення, що повертаються

Позначка часу перетвореного значення або **`false`**, якщо значення не може бути перетворено.

### Приклади

**Приклад #1 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Первый преобразованный вывод: ' . $fmt->parse('Wednesday, December 20, 1989 4:00:00 PM PT');
$fmt = new IntlDateFormatter(
    'de-DE',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
?>
```

**Приклад #2 Приклад використання **datefmtparse()****

```php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Первый преобразованный вывод: ' . datefmt_parse($fmt, 'Wednesday, December 20, 1989 4:00:00 PM PT');
$fmt = datefmt_create(
    'de-DE',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Второй преобразованный вывод: ' . datefmt_parse($fmt, 'Mittwoch, 20. Dezember 1989 16:00 Uhr GMT-08:00');
?
```

Результат виконання цього прикладу:

```
Первый преобразованный вывод: 630201600
Второй преобразованный вывод: 630201600
```

### Дивіться також

-   [datefmtcreate()](intldateformatter.create.md) - Створює засіб форматування дати
-   [datefmtformat()](intldateformatter.format.md) - Форматує значення дати/часу у вигляді рядка
-   [datefmtlocaltime()](intldateformatter.localtime.md) - Перетворює рядок на значення часу на основі поля
-   [datefmtgeterrorcode()](intldateformatter.geterrorcode.md) - Отримує код помилки останньої операції
-   [datefmtgeterrormessage()](intldateformatter.geterrormessage.md) - Отримує текст помилки останньої операції
