Очищає поле чи всі поля

-   [« IntlCalendar::before](intlcalendar.before.md)
    
-   [IntlCalendar::construct »](intlcalendar.construct.md)
    
-   [PHP Manual](index.md)
    
-   [IntlCalendar](class.intlcalendar.md)
    
-   Очищає поле чи всі поля
    

# IntlCalendar::clear

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::clear — Очищає поле чи всі поля

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::clear(?int $field = null): bool
```

Процедурний стиль

```methodsynopsis
intlcal_clear(IntlCalendar $calendar, ?int $field = null): bool
```

Очищає всі поля, або певне поле. Очищене поле позначається як не задане, що дає йому найнижчий пріоритет щодо перевизначальних полів або навіть за замовчуванням при обчисленні часу. Крім того, його значення встановлено на `0`, хоча, враховуючи низький пріоритет поля, його значення могло бути внутрішньо встановлено інше значення на момент завершення запиту поля.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

`field`

Одна з представлених у класі [IntlCalendar](class.intlcalendar.md) [констант](class.intlcalendar.html#intlcalendar.constants) полів типу дата/час. Ціла кількість від `0` до **`IntlCalendar::FIELD_COUNT`**

### Значення, що повертаються

Функція завжди повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **IntlCalendar::clear()****

```php
<?php
ini_set('intl.default_locale', 'es_ES');
ini_set('date.timezone', 'UTC');

$fields = array(
    'FIELD_ERA'                  => 0,
    'FIELD_YEAR'                 => 1,
    'FIELD_MONTH'                => 2,
    'FIELD_WEEK_OF_YEAR'         => 3,
    'FIELD_WEEK_OF_MONTH'        => 4,
    'FIELD_DATE'                 => 5,
    'FIELD_DAY_OF_YEAR'          => 6,
    'FIELD_DAY_OF_WEEK'          => 7,
    'FIELD_DAY_OF_WEEK_IN_MONTH' => 8,
    'FIELD_AM_PM'                => 9,
    'FIELD_HOUR'                 => 10,
    'FIELD_HOUR_OF_DAY'          => 11,
    'FIELD_MINUTE'               => 12,
    'FIELD_SECOND'               => 13,
    'FIELD_MILLISECOND'          => 14,
    'FIELD_ZONE_OFFSET'          => 15,
    'FIELD_DST_OFFSET'           => 16,
    'FIELD_YEAR_WOY'             => 17,
    'FIELD_DOW_LOCAL'            => 18,
    'FIELD_EXTENDED_YEAR'        => 19,
    'FIELD_JULIAN_DAY'           => 20,
    'FIELD_MILLISECONDS_IN_DAY'  => 21,
    'FIELD_IS_LEAP_MONTH'        => 22,
    'FIELD_FIELD_COUNT'          => 23,
);
function getSetFields(IntlCalendar $cal) {
    global $fields;
    $ret = array();
    foreach ($fields as $name => $value) {
        if ($cal->isSet($value)) {
            $ret[] = $name;
        }
    }
    return $ret;
}

$cal = new IntlGregorianCalendar(2013, 2 /* Март */, 15);
echo "После создания григорианского календаря\n";
print_r(getSetFields($cal));
echo "\n";

echo IntlDateFormatter::formatObject($cal), "\n";
echo "После того, как средство форматирования запросило поле EXTENDED_YEAR\n";
print_r(getSetFields($cal));
echo "\n";

$cal->clear(IntlCalendar::FIELD_YEAR);
echo "После того, как год будет очищен, дата останется прежней\n";
echo IntlDateFormatter::formatObject($cal), "\n";
echo "Потому что FIELD_EXTENDED_YEAR все ещё установлен\n";
print_r(getSetFields($cal));
echo "\n";

var_dump($cal->clear(IntlCalendar::FIELD_EXTENDED_YEAR));
echo "После того, как поле EXTENDED_YEAR было очищено\n";
print_r(getSetFields($cal));
echo IntlDateFormatter::formatObject($cal), "\n";
echo "\n";

echo "После пересчёта полей,\n"
        . " снова установлено поле EXTENDED_YEAR (до 1970 г.)\n";
print_r(getSetFields($cal));
echo "\n";

$cal->clear();
echo "После вызова варианта без аргументов\n";
print_r(getSetFields($cal));
echo IntlDateFormatter::formatObject($cal), "\n";
```

Результат виконання цього прикладу:

```
После создания григорианского календаря
Array
(
    [0] => FIELD_ERA
    [1] => FIELD_YEAR
    [2] => FIELD_MONTH
    [3] => FIELD_DATE
)

15/03/2013 00:00:00
После того, как средство форматирования запросило поле EXTENDED_YEAR
Array
(
    [0] => FIELD_ERA
    [1] => FIELD_YEAR
    [2] => FIELD_MONTH
    [3] => FIELD_DATE
    [4] => FIELD_EXTENDED_YEAR
)

После того, как год будет очищен, дата останется прежней
15/03/2013 00:00:00
Потому что FIELD_EXTENDED_YEAR все ещё установлен
Array
(
    [0] => FIELD_ERA
    [1] => FIELD_MONTH
    [2] => FIELD_DATE
    [3] => FIELD_EXTENDED_YEAR
)

bool(true)
После того, как поле EXTENDED_YEAR было очищено
Array
(
    [0] => FIELD_ERA
    [1] => FIELD_MONTH
    [2] => FIELD_DATE
)
15/03/1970 00:00:00

После пересчёта полей,
 снова установлено поле EXTENDED_YEAR (до 1970 г.)
Array
(
    [0] => FIELD_ERA
    [1] => FIELD_MONTH
    [2] => FIELD_DATE
    [3] => FIELD_EXTENDED_YEAR
)

После вызова варианта без аргументов
Array
(
)
01/01/1970 00:00:00
```