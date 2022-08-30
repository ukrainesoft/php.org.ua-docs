Форматує об'єкт

-   [« IntlDateFormatter::format](intldateformatter.format.html)
    
-   [IntlDateFormatter::getCalendar »](intldateformatter.getcalendar.html)
    
-   [PHP Manual](index.html)
    
-   [IntlDateFormatter](class.intldateformatter.html)
    
-   Форматує об'єкт
    

# IntlDateFormatter::formatObject

# datefmtformatobject

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL intl >= 3.0.0)

IntlDateFormatter::formatObject -- datefmtformatobject — Форматує об'єкт

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static IntlDateFormatter::formatObject(IntlCalendar|DateTimeInterface $datetime, array|int|string|null $format = null, ?string $locale = null): string|false
```

Процедурний стиль

```methodsynopsis
datefmt_format_object(IntlCalendar|DateTimeInterface $datetime, array|int|string|null $format = null, ?string $locale = null): string|false
```

Функція дозволяє форматувати об'єкт [IntlCalendar](class.intlcalendar.html) або [DateTime](class.datetime.html) без попереднього явного створення об'єкта [IntlDateFormatter](class.intldateformatter.html)

Тимчасовий [IntlDateFormatter](class.intldateformatter.html), який буде створено, приймає часовий пояс із переданого об'єкта. База даних часових поясів, пов'язана з PHP, не використовуватиметься - замість неї використовуватиметься ICU. Отже, ідентифікатор часового поясу, який використовується в об'єктах [DateTime](class.datetime.html), також має існувати у базі даних ICU.

### Список параметрів

`datetime`

Об'єкт типу [IntlCalendar](class.intlcalendar.html) або [DateTime](class.datetime.html). Використовуватиметься інформація про часовий пояс в об'єкті.

`format`

Як відформатувати дату/час. Можливо або масив (array) з двома елементами (спочатку стиль дати, потім стиль часу, може бути одна з констант: **`IntlDateFormatter::NONE`** **`IntlDateFormatter::SHORT`** **`IntlDateFormatter::MEDIUM`** **`IntlDateFormatter::LONG`** **`IntlDateFormatter::FULL`**), ціле число (int) зі значенням однієї з цих констант (у цьому випадку воно буде використовуватися як для часу, так і для дати) або рядок (string) у форматі, описаному в [» документации ICU](https://unicode-org.github.io/icu/userguide/format_parse/datetime/#datetime-format-syntax). Якщо вказано значення **`null`**, використовуватиметься стиль за замовчуванням.

`locale`

Використовуваний мовний стандарт або **`null`** для використання [значения по умолчанию](intl.configuration.html#ini.intl.default-locale)

### Значення, що повертаються

Рядок з результатом або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **IntlDateFormatter::formatObject()****

```php
<?php
/* часовой пояс по умолчанию не имеет значения; часовой пояс взят из объекта */
ini_set('date.timezone', 'UTC');
/* языковой стандарт по умолчанию берётся из этой настройки ini */
ini_set('intl.default_locale', 'fr_FR');

$cal = IntlCalendar::fromDateTime("2013-06-06 17:05:06 Europe/Dublin");
echo "По умолчанию:\n\t",
        IntlDateFormatter::formatObject($cal),
        "\n";

echo "Полная запись: \$format (full):\n\t",
        IntlDateFormatter::formatObject($cal, IntlDateFormatter::FULL),
        "\n";

echo "Масив: \$format (none, full):\n\t",
        IntlDateFormatter::formatObject($cal, array(
                IntlDateFormatter::NONE,
                IntlDateFormatter::FULL)),
        "\n";

echo "Строка: \$format (d 'of' MMMM y):\n\t",
        IntlDateFormatter::formatObject($cal, "d 'of' MMMM y", 'en_US'),
        "\n";

echo "Объект DateTime:\n\t",
        IntlDateFormatter::formatObject(
                new DateTime("2013-09-09 09:09:09 Europe/Madrid"),
                IntlDateFormatter::FULL,
                'es_ES'),
        "\n";
```

Результат виконання цього прикладу:

```
По умолчанию:
    6 juin 2013 17:05:06
Полная запись: $format (full):
    jeudi 6 juin 2013 17:05:06 heure d’été irlandaise
Масив: $format (none, full):
    17:05:06 heure d’été irlandaise
Строка: $format (d 'of' MMMM y):
    6 of June 2013
Объект DateTime:
    lunes, 9 de septiembre de 2013 09:09:09 Hora de verano de Europa central
```