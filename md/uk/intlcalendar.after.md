Визначає час цього об'єкта пізніше часу переданого об'єкта

-   [« IntlCalendar::add](intlcalendar.add.html)
    
-   [IntlCalendar::before »](intlcalendar.before.html)
    
-   [PHP Manual](index.html)
    
-   [IntlCalendar](class.intlcalendar.html)
    
-   Визначає час цього об'єкта пізніше часу переданого об'єкта
    

# IntlCalendar::after

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::after — Визначає час цього об'єкта пізніше часу переданого об'єкта

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::after(IntlCalendar $other): bool
```

Процедурний стиль

```methodsynopsis
intlcal_after(IntlCalendar $calendar, IntlCalendar $other): bool
```

Повертає, чи відповідає час об'єкта часу аргументу.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.html)

`other`

Календар, час якого порівнюватиметься з часом основного об'єкта.

### Значення, що повертаються

Повертає **`true`**, якщо поточний час цього об'єкта пізніше часу аргументу `calendar`. В іншому випадку повертає **`false`**

У разі виникнення помилки також повертається **`false`**. Для виявлення умов помилки використовуйте [intl\_get\_error\_code()](function.intl-get-error-code.html) або настройте викидання [исключений](intl.configuration.html#ini.intl.use-exceptions) в Intl.

### Приклади

**Приклад #1 Приклад використання **IntlCalendar::after()****

```php
<?php
$cal1 = IntlCalendar::createInstance();
$cal2 = clone $cal1;

var_dump($cal1->after($cal2), //false
        $cal2->after($cal1)); //false

$cal1->roll(IntlCalendar::FIELD_MILLISECOND, true);

var_dump($cal1->after($cal2), //true
        $cal2->after($cal1)); //false
```