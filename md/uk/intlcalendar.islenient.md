Визначає, чи інтерпретація дати/часу є м'якою.

-   [« IntlCalendar::isEquivalentTo](intlcalendar.isequivalentto.html)
    
-   [IntlCalendar::isSet »](intlcalendar.isset.html)
    
-   [PHP Manual](index.html)
    
-   [IntlCalendar](class.intlcalendar.html)
    
-   Визначає, чи інтерпретація дати/часу є м'якою.
    

# IntlCalendar::isLenient

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::isLenient — Визначає, чи інтерпретація дати/часу є м'якою.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::isLenient(): bool
```

Процедурний стиль

```methodsynopsis
intlcal_is_lenient(IntlCalendar $calendar): bool
```

Повертає, чи є поточна інтерпретація дати та часу м'якою (за умовчанням). У цьому випадку деякі значення полів поза допустимим діапазоном будуть прийняті замість того, щоб викликати помилку.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.html)

### Значення, що повертаються

Логічне значення (bool), що вказує на те, чи в календарі встановлений м'який режим.

### Приклади

**Приклад #1 Приклад використання **IntlCalendar::isLenient()****

```php
<?php
ini_set('date.timezone', 'Europe/Lisbon');
ini_set('intl.default_locale', 'pt_PT');
ini_set('intl.use_exceptions', '1');

$cal = new IntlGregorianCalendar(2013, 6 /* Июль */, 1);
var_dump(IntlDateFormatter::formatObject($cal), // 01/07/2013, 00:00:00
$cal->isLenient()); // true

$cal->set(IntlCalendar::FIELD_DAY_OF_MONTH, 33);
var_dump(IntlDateFormatter::formatObject($cal)); // 02/08/2013, 00:00:00

$cal->setLenient(false);
var_dump($cal->isLenient()); // false
$cal->set(IntlCalendar::FIELD_DAY_OF_MONTH, 33);
var_dump(IntlDateFormatter::formatObject($cal)); // ошибка
```

Результат виконання цього прикладу:

```
string(20) "01/07/2013, 00:00:00"
bool(true)
string(20) "02/08/2013, 00:00:00"
bool(false)

Fatal error: Uncaught exception 'IntlException' with message 'datefmt_format_object: error obtaining instant from IntlCalendar' in /home/foobar/example.php:16
Stack trace:
#0 /home/foobar/example.php(16): IntlDateFormatter::formatObject(Object(IntlGregorianCalendar))
#1 {main}
  thrown in /home/foobar/example.php on line 16
```