Форматує значення дати/часу у вигляді рядка

-   [« IntlDateFormatter::create](intldateformatter.create.html)
    
-   [IntlDateFormatter::formatObject »](intldateformatter.formatobject.html)
    
-   [PHP Manual](index.html)
    
-   [IntlDateFormatter](class.intldateformatter.html)
    
-   Форматує значення дати/часу у вигляді рядка
    

# IntlDateFormatter::format

# datefmtformat

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL intl >= 1.0.0)

IntlDateFormatter::format -- datefmtformat — Форматує значення дати/часу у вигляді рядка

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlDateFormatter::format(IntlCalendar|DateTimeInterface|array|string|int|float $datetime): string|false
```

Процедурний стиль

```methodsynopsis
datefmt_format(IntlDateFormatter $formatter, IntlCalendar|DateTimeInterface|array|string|int|float $datetime): string|false
```

Форматує значення дати/часу у вигляді рядка.

### Список параметрів

`formatter`

Ресурс засобу форматування дати.

`datetime`

Значення форматування. Це може бути об'єкт [DateTimeInterface](class.datetimeinterface.html), об'єкт [IntlCalendar](class.intlcalendar.html), тип numeric, що представляє (можливо, дробову) кількість секунд від початку епохи Unix або масив (array) у форматі, що виводиться функцією [localtime()](function.localtime.html)

Якщо передається об'єкт [DateTime](class.datetime.html) або [IntlCalendar](class.intlcalendar.html), його часовий пояс не враховується. Об'єкт буде відформатований за допомогою часового поясу засобу форматування. Якщо хтось хоче використовувати часовий пояс об'єкта, який потрібно відформатувати, потрібно викликати функцію [IntlDateFormatter::setTimeZone()](intldateformatter.settimezone.html) з часового поясу об'єкта. Як альтернативу замість неї може використовуватися статична функція [IntlDateFormatter::formatObject()](intldateformatter.formatobject.html)

### Значення, що повертаються

Відформатований рядок або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Додано підтримку надання спільних об'єктів [DateTimeInterface](class.datetimeinterface.html) для параметра `datetime`. Раніше підтримувалися лише об'єкти [DateTime](class.datetime.html) |
| PECL 3.0.0 | Додано підтримку надання об'єктів [IntlCalendar](class.intlcalendar.html) для параметра `datetime` |

### Приклади

**Приклад #1 Приклад використання **datefmtformat()****

```php
<?php
$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Первый форматированный вывод: ' . datefmt_format($fmt, 0);

$fmt = datefmt_create(
    'de-DE',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Второй форматированный вывод: ' . datefmt_format($fmt, 0);

$fmt = datefmt_create(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN,
    'MM/dd/yyyy'
);
echo 'Первый форматированный вывод с шаблоном: ' . datefmt_format($fmt, 0);

$fmt = datefmt_create(
    'de-DE',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN,
    'MM/dd/yyyy'
);
echo "Второй форматированный вывод с шаблоном: " . datefmt_format($fmt, 0);
?>
```

**Приклад #2 Приклад використання в об'єктно-орієнтованому стилі**

```php
<?php
$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Первый форматированный вывод: ' . $fmt->format(0);

$fmt = new IntlDateFormatter(
    'de-DE',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN
);
echo 'Второй форматированный вывод: ' . $fmt->format(0);

$fmt = new IntlDateFormatter(
    'en_US',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN,
    'MM/dd/yyyy'
);
echo 'Первый форматированный вывод с шаблоном: ' . $fmt->format(0);

$fmt = new IntlDateFormatter(
    'de-DE',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    'America/Los_Angeles',
    IntlDateFormatter::GREGORIAN,
    'MM/dd/yyyy'
);
echo 'Второй форматированный вывод с шаблоном: ' . $fmt->format(0);
?>
```

Результат виконання цього прикладу:

```
Первый форматированный вывод: Wednesday, December 31, 1969 4:00:00 PM PT
Второй форматированный вывод: Mittwoch, 31. Dezember 1969 16:00 Uhr GMT-08:00
Первый форматированный вывод с шаблоном: 12/31/1969
Второй форматированный вывод с шаблоном: 12/31/1969
```

**Приклад #3 Приклад використання об'єкта [IntlCalendar](class.intlcalendar.html)**

```php
<?php
$tz = reset(iterator_to_array(IntlTimeZone::createEnumeration('FR')));
$formatter = IntlDateFormatter::create(
    'fr_FR',
    IntlDateFormatter::FULL,
    IntlDateFormatter::FULL,
    $tz,
    IntlDateFormatter::GREGORIAN
);

$cal = IntlCalendar::createInstance($tz, '@calendar=islamic-civil');
$cal->set(IntlCalendar::FIELD_MONTH, 8); //9-й месяц, Рамадан
$cal->set(IntlCalendar::FIELD_DAY_OF_MONTH, 1); //Первый день
$cal->clear(IntlCalendar::FIELD_HOUR_OF_DAY);
$cal->clear(IntlCalendar::FIELD_MINUTE);
$cal->clear(IntlCalendar::FIELD_SECOND);
$cal->clear(IntlCalendar::FIELD_MILLISECOND);

echo "В этом исламском году Рамадан начался/начнётся:\n\t",
        $formatter->format($cal), "\n";

//Это часовой пояс используемого средства форматирования:
$formatter->setTimeZone('Asia/Tokyo');
echo "После изменения часового пояса:\n\t",
        $formatter->format($cal), "\n";
```

Результат виконання цього прикладу:

```
В этом исламском году Рамадан начался/начнётся:
    mardi 9 juillet 2013 19:00:00 heure avancée d’Europe centrale
После изменения часового пояса:
    mercredi 10 juillet 2013 02:00:00 heure normale du Japon
```

### Дивіться також

-   [datefmt\_create()](intldateformatter.create.html) - Створює засіб форматування дати
-   [datefmt\_parse()](intldateformatter.parse.html) - Перетворює рядок на значення позначки часу
-   [datefmt\_get\_error\_code()](intldateformatter.geterrorcode.html) - Отримує код помилки останньої операції
-   [datefmt\_get\_error\_message()](intldateformatter.geterrormessage.html) - Отримує текст помилки останньої операції
-   [datefmt\_format\_object()](intldateformatter.formatobject.html) - Форматує об'єкт