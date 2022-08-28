Додає кількість (зі знаком) часу у полі

-   [« IntlCalendar](class.intlcalendar.html)
    
-   [IntlCalendar::after »](intlcalendar.after.html)
    
-   [PHP Manual](index.html)
    
-   [IntlCalendar](class.intlcalendar.html)
    
-   Додає кількість (зі знаком) часу у полі
    

# IntlCalendar::add

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::add — Додає кількість (зі знаком) часу у поле

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::add(int $field, int $value): bool
```

Процедурний стиль

```methodsynopsis
intlcal_add(IntlCalendar $calendar, int $field, int $value): bool
```

Додає кількість зі знаком у полі. Додавання позитивної суми дозволяє просуватися в часі, навіть якщо числове значення поля зменшується (наприклад, під час роботи з роками до нашої ери).

Інші поля можуть потребувати коригування, наприклад, додавання місяця до 31 січня призведе до 28 (або 29) лютого. На відміну від [IntlCalendar::roll()](intlcalendar.roll.html)Коли значення обертається, важливіші поля можуть змінитися. Наприклад, додавання 1 дня до 31 січня призведе до 1 лютого, а не до 1 січня.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.html)

`field`

Одна з представлених у класі [IntlCalendar](class.intlcalendar.html) [констант](class.intlcalendar.html#intlcalendar.constants) полів типу дата/час. Ціла кількість від `0` до **`IntlCalendar::FIELD_COUNT`**

`value`

Кількість зі знаком, що додається до поточного поля. Якщо сума позитивна, час буде переміщений вперед; якщо він негативний, час буде переміщений у минуле. Одиниця неявно пов'язана із типом поля. Наприклад, годинник для **`IntlCalendar::FIELD_HOUR_OF_DAY`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **IntlCalendar::add()****

```php
<?php
ini_set('intl.default_locale', 'fr_FR');
ini_set('date.timezone', 'UTC');

$cal = new IntlGregorianCalendar(2012, 0 /* January */, 31);
echo IntlDateFormatter::formatObject($cal), "\n";

$cal->add(IntlCalendar::FIELD_MONTH, 1);
echo IntlDateFormatter::formatObject($cal), "\n";

$cal->add(IntlCalendar::FIELD_DAY_OF_MONTH, 1);
echo IntlDateFormatter::formatObject($cal), "\n";
```

Результат виконання цього прикладу:

```
31 janv. 2012 00:00:00
29 févr. 2012 00:00:00
1 mars 2012 00:00:00
```