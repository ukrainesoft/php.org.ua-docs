Визначає час цього об'єкта раніше часу переданого об'єкта

-   [« IntlCalendar::after](intlcalendar.after.md)
    
-   [IntlCalendar::clear »](intlcalendar.clear.md)
    
-   [PHP Manual](index.md)
    
-   [IntlCalendar](class.intlcalendar.md)
    
-   Визначає час цього об'єкта раніше часу переданого об'єкта
    

# IntlCalendar::before

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::before — Визначає час цього об'єкта раніше часу переданого об'єкта

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::before(IntlCalendar $other): bool
```

Процедурний стиль

```methodsynopsis
intlcal_before(IntlCalendar $calendar, IntlCalendar $other): bool
```

Повертає, чи час цього об'єкта передує часу аргументу.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.md)

`other`

Календар, час якого порівнюватиметься з часом основного об'єкта.

### Значення, що повертаються

Повертає **`true`**, якщо поточний час цього об'єкта раніше аргументу `calendar`. В іншому випадку повертає **`false`**

У разі виникнення помилки також повертається **`false`**. Для виявлення умов помилки використовуйте [intlgeterrorcode()](function.intl-get-error-code.html) або настройте викидання [исключений](intl.configuration.html#ini.intl.use-exceptions) в Intl.