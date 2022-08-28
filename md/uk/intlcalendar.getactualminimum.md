Мінімальне значення для поля з урахуванням поточного часу об'єкта

-   [« IntlCalendar::getActualMaximum](intlcalendar.getactualmaximum.html)
    
-   [IntlCalendar::getAvailableLocales »](intlcalendar.getavailablelocales.html)
    
-   [PHP Manual](index.html)
    
-   [IntlCalendar](class.intlcalendar.html)
    
-   Мінімальне значення для поля з урахуванням поточного часу об'єкта
    

# IntlCalendar::getActualMinimum

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::getActualMinimum — Мінімальне значення для поля з урахуванням поточного часу об'єкта

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::getActualMinimum(int $field): int|false
```

Процедурний стиль

```methodsynopsis
intlcal_get_actual_minimum(IntlCalendar $calendar, int $field): int|false
```

Повертає відносне мінімальне значення поля з урахуванням поточного часу. Точна семантика залежить від поля, але в загальному випадку це значення, яке можна було б отримати, якби встановити значення поля на [наибольший относительный минимум](intlcalendar.getgreatestminimum.html) для поля і зменшувати його до тих пір, поки не буде досягнуто [глобальный минимум](intlcalendar.getminimum.html) або значення поля буде обернуте навколо, в якому значення, що повертається, буде глобальним мінімумом або значенням до перенесення, відповідно.

Для григоріанського календаря це завжди те саме, що й [IntlCalendar::getMinimum()](intlcalendar.getminimum.html)

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.html)

`field`

Одна з представлених у класі [IntlCalendar](class.intlcalendar.html) [констант](class.intlcalendar.html#intlcalendar.constants) полів типу дата/час. Ціла кількість від `0` до **`IntlCalendar::FIELD_COUNT`**

### Значення, що повертаються

Ціле число (int), що представляє значення поля або **`false`** у разі виникнення помилки.

### Дивіться також

-   [IntlCalendar::getMinimum()](intlcalendar.getminimum.html) - Отримує глобальне мінімальне значення поля
-   [IntlCalendar::getGreatestMinimum()](intlcalendar.getgreatestminimum.html) - Отримує найбільше локальне мінімальне значення поля
-   [IntlCalendar::getActualMaximum()](intlcalendar.getactualmaximum.html) - Максимальне значення для поля з урахуванням поточного часу об'єкта