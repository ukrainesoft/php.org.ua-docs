Встановлює, чи інтерпретація дати/часу повинна бути м'якою.

-   [« IntlCalendar::setFirstDayOfWeek](intlcalendar.setfirstdayofweek.html)
    
-   [IntlCalendar::setMinimalDaysInFirstWeek »](intlcalendar.setminimaldaysinfirstweek.html)
    
-   [PHP Manual](index.html)
    
-   [IntlCalendar](class.intlcalendar.html)
    
-   Встановлює, чи інтерпретація дати/часу повинна бути м'якою.
    

# IntlCalendar::setLenient

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlCalendar::setLenient — Встановлює, чи інтерпретація дати/часу повинна бути м'якою.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public IntlCalendar::setLenient(bool $lenient): bool
```

Процедурний стиль

```methodsynopsis
intlcal_set_lenient(IntlCalendar $calendar, bool $lenient): bool
```

Визначає, чи календар "м'яким" режимом. У такому режимі приймаються деякі з значень, що виходять за кордон для деяких полів, поведінка аналогічна поведінці [IntlCalendar::add()](intlcalendar.add.html) (тобто значення переноситься щоразу на більш важливі поля). Якщо м'який режим вимкнено, такі значення викликатимуть помилку.

### Список параметрів

`calendar`

Екземпляр [IntlCalendar](class.intlcalendar.html)

`lenient`

Використовуйте **`true`** для активації м'якого режиму; **`false`** для вимикання.

### Значення, що повертаються

Функція завжди повертає **`true`**

### Приклади

Дивіться приклад в описі методу [IntlCalendar::isLenient()](intlcalendar.islenient.html)