---
navigation:
  - intldateformatter.format.md: '« IntlDateFormatter::format'
  - intldateformatter.getcalendar.md: 'IntlDateFormatter::getCalendar »'
  - index.md: PHP Manual
  - class.intldateformatter.md: IntlDateFormatter
title: 'IntlDateFormatter::formatObject'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlDateFormatter::formatObject

# datefmt\_format\_object

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL intl >= 3.0.0)

IntlDateFormatter::formatObject -- datefmt\_format\_object — Форматує об'єкт

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static IntlDateFormatter::formatObject(IntlCalendar|DateTimeInterface $datetime, array|int|string|null $format = null, ?string $locale = null): string|false
```

Процедурний стиль

```methodsynopsis
datefmt_format_object(IntlCalendar|DateTimeInterface $datetime, array|int|string|null $format = null, ?string $locale = null): string|false
```

Функція дозволяє форматувати об'єкт [IntlCalendar](class.intlcalendar.md) або [DateTime](class.datetime.md) без попереднього явного створення об'єкта [IntlDateFormatter](class.intldateformatter.md)

Тимчасовий [IntlDateFormatter](class.intldateformatter.md), який буде створено, приймає часовий пояс із переданого об'єкта. База даних часових поясів, пов'язана з PHP, не використовуватиметься - замість неї використовуватиметься ICU. Отже, ідентифікатор часового поясу, який використовується в об'єктах [DateTime](class.datetime.md), також має існувати у базі даних ICU.

### Список параметрів

`datetime`

Об'єкт типу [IntlCalendar](class.intlcalendar.md) або [DateTime](class.datetime.md). Використовуватиметься інформація про часовий пояс в об'єкті.

`format`

Як відформатувати дату/час. Можливо або масив (array) з двома елементами (спочатку стиль дати, потім стиль часу, може бути одна з констант: **`IntlDateFormatter::NONE`** **`IntlDateFormatter::SHORT`** **`IntlDateFormatter::MEDIUM`** **`IntlDateFormatter::LONG`** **`IntlDateFormatter::FULL`**), ціле число (int) зі значенням однієї з цих констант (у цьому випадку воно буде використовуватися як для часу, так і для дати) або рядок (string) у форматі, описаному в [» документації ICU](https://unicode-org.github.io/icu/userguide/format_parse/datetime/#datetime-format-syntax)Если указано значение\*\*`null`\*\*, використовуватиметься стиль за замовчуванням.

`locale`

Використовуваний мовний стандарт або \*\*`null`\*\*для использования[значення за замовчуванням](intl.configuration.md#ini.intl.default-locale)

### Значення, що повертаються

Строка с результатом или\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**IntlDateFormatter::formatObject()\*\*\*\*

```php
<?php
/* часовой пояс по умолчанию не имеет значения; часовой пояс взят из объекта */
ini_set('date.timezone', 'UTC');
/* языковой стандарт по умолчанию берётся из этой настройки ini */
ini_set('intl.default_locale', 'fr_FR');

$cal = IntlCalendar::fromDateTime("2013-06-06 17:05:06 Europe/Dublin");
echo "По умолчанию:\n\t",
        IntlDateFormatter::formatObject($cal),
        "\n";

echo "Полная запись: \$format (full):\n\t",
        IntlDateFormatter::formatObject($cal, IntlDateFormatter::FULL),
        "\n";

echo "Массив: \$format (none, full):\n\t",
        IntlDateFormatter::formatObject($cal, array(
                IntlDateFormatter::NONE,
                IntlDateFormatter::FULL)),
        "\n";

echo "Строка: \$format (d 'of' MMMM y):\n\t",
        IntlDateFormatter::formatObject($cal, "d 'of' MMMM y", 'en_US'),
        "\n";

echo "Объект DateTime:\n\t",
        IntlDateFormatter::formatObject(
                new DateTime("2013-09-09 09:09:09 Europe/Madrid"),
                IntlDateFormatter::FULL,
                'es_ES'),
        "\n";
```

Результат виконання наведеного прикладу:

```
По умолчанию:
    6 juin 2013 17:05:06
Полная запись: $format (full):
    jeudi 6 juin 2013 17:05:06 heure d’été irlandaise
Массив: $format (none, full):
    17:05:06 heure d’été irlandaise
Строка: $format (d 'of' MMMM y):
    6 of June 2013
Объект DateTime:
    lunes, 9 de septiembre de 2013 09:09:09 Hora de verano de Europa central
```
